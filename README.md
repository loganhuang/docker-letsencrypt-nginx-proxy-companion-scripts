

1. 把脚本拷到需要绑定域名的机器上，并在域名管理界面绑定机器外网地址。
2. 在docker-run.sh 中替换VIRTUAL_HOST, LETSENCRYPT_HOST, LETSENCRYPT_EMAIL


docker run -d \
    --name simple-site \
    -e "VIRTUAL_HOST=git2.top" \
    -e "LETSENCRYPT_HOST=git2.top" \
    -e "LETSENCRYPT_EMAIL=huangzhouwu@163.com" \
    -v $(pwd)/../../volumes/examples/simple-site/conf.d/:/etc/nginx/conf.d \
    nginx
3. sh setup.sh
4. sh docker-run.sh
