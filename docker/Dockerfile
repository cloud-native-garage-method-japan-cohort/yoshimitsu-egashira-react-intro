FROM quay.io/jeffdean/node-alpine as build
WORKDIR /app
COPY . .
RUN yarn --frozen-lockfile && \
    yarn build

FROM quay.io/jeffdean/nginx-unprivileged

COPY --from=build /app/build /usr/share/nginx/html

COPY --from=build /app/docker/nginx/*.conf /etc/nginx/conf.d/