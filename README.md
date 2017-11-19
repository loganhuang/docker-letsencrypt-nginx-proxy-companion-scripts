
1. 在docker-run.sh 中替换VIRTUAL_HOST, LETSENCRYPT_HOST, LETSENCRYPT_EMAIL
docker run -d \
    --name simple-site \
    -e "VIRTUAL_HOST=git2.top" \
    -e "LETSENCRYPT_HOST=git2.top" \
    -e "LETSENCRYPT_EMAIL=huangzhouwu@163.com" \
    -v $(pwd)/../../volumes/examples/simple-site/conf.d/:/etc/nginx/conf.d \
    nginx
2. sh setup.sh
3. sh docker-run.sh
