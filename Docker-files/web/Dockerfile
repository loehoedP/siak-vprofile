FROM nginx:latest
LABEL project="chelsea"
LABEL app="vprofile"
LABEL author="loehoedp"

RUN rm -rf /etc/nginx/conf.d/default.conf
COPY nginvproapp.conf /etc/nginx/conf.d/nginvproapp.conf