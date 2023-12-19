# I used the path "/usr/src/app" as it is a commonly used path within the container

# Step 1
FROM node:19-alpine AS build

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

# Step 2
FROM nginx:1.23.3-alpine

COPY --from=build /usr/src/app/dist /usr/share/nginx/html

# CMD instruction wopuld not be required, the default CMD of the nginx image would be enough