FROM node:14

ARG DEFAULT_PORT=80

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

ENV PORT=$DEFAULT_PORT

EXPOSE $PORT

# VOLUME [ "/app/node_modules" ]

#VOLUME [ "/temp" ]

CMD [ "npm", "start" ]

#RUN docker with volume mapping
#docker run -d --rm -p 3000:80 --name feedback-app -v feedback:/app/feedback -v "/home/bejnack/repo/docker_kubernetes/3_Managing_Data_n_Volumes/3_data-volumes-04-added-nodemon:/app:ro" -v /app/temp -v /app/node_modules node-app:volumes .

#RUN docker with ENVar specified in command
#docker run -d --rm -p 3000:80 --env PORT=8000 --name feedback-app -v feedback:/app/feedback -v "/home/bejnack/repo/docker_kubernetes/3_Managing_Data_n_Volumes/3_data-volumes-04-added-nodemon:/app:ro" -v /app/temp

#RUN docker with ENVar specified in .env file
#docker run -d --rm -p 3000:80 --env-file ./.env --name feedback-app -v feedback:/app/feedback -v "/home/bejnack/repo/docker_kubernetes/3_Managing_Data_n_Volumes/3_data-volumes-04-added-nodemon:/app:ro" -v /app/temp -v /app/node_modules feedback-node:env
#USE THIS FOR PASSWORDS - Security

#DOCKER BUILD with specific ARGument
#docker build -t feedback-node:dev --build-arg DEFAULT_PORT=8000 .