# nginx  

#### Content-Typeで制限をかける方法  
docker exec -it コンテナ名 bashでコンテナに入る  
etc/nginx/conf.dにあるdefault.confのserverディレクティブにて、指定したContent-Type以外はエラーを返すよう記述する  
if ($content_type !~ ^(application/json)$ ){
    return 415;
}