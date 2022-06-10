FROM python:3-alpine
ARG USER=app
ARG UID=1001
ARG GID=1001
RUN addgroup --gid $GID -S ${USER} \
    && adduser -u $UID -S ${USER} -g ${USER} \
    && mkdir -p /app \
    && chown -R ${USER}:${USER} /app
USER ${USER}
COPY --chown=$USER:$USER . /app
WORKDIR /app
EXPOSE 8000

CMD python -m http.server 8000