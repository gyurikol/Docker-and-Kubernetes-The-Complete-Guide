# Start with node image for build phase
FROM node:alpine

WORKDIR '/app'

COPY package.json .
RUN npm install
COPY . .

RUN npm run build

# Add nginx image and copy from first build phase
FROM nginx
COPY --from=0 /app/build /usr/share/nginx/html