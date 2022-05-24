# FROM openjdk:11-alpine
# ENTRYPOINT ["/usr/bin/${{values.artifact_id}}.sh"]

# COPY ${{values.artifact_id}}.sh /usr/bin/${{values.artifact_id}}.sh
# COPY target/${{values.artifact_id}}.jar /usr/share/${{values.artifact_id}}/${{values.artifact_id}}.jar

FROM nginx:1.21-alpine
RUN rm -rf /usr/share/nginx/html
COPY html/ /usr/share/nginx/html
COPY nginx.conf /etc/nginx/conf.d/default.conf
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
