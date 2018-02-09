FROM node:carbon

COPY ./docker/entrypoint.sh /entrypoint/

RUN ["chmod", "+x", "entrypoint/entrypoint.sh"]

# Copy or mount node app here
WORKDIR /data/

EXPOSE 8081

ENTRYPOINT ["/entrypoint/entrypoint.sh"]

CMD ["npm", "start"]

