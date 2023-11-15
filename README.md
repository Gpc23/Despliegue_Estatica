# Despliegue_Estatica

SCRIPT AUTOMATIZACIÓN 

```

#! bin/sh

commit=$(git commit -am 'nuevo' | egrep 'content/')
touch ../nuevo.txt
echo $commit > ../nuevo.txt

git add $(cat ../nuevo.txt)
git commit -m 'añado'
git push

rm ../nuevo.txt

hugo
surge public/ gonzalopcblog.surge.sh

```
