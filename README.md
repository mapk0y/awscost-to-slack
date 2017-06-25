Lambda で AWS の料金を Slack に通知する奴

[LambdaでAWSの料金を毎日Slackに通知する（Python3） - Qiita](http://qiita.com/tomohiko_isobe/items/88e8e0dcb0ee224a31e4) を参考に設定。コードはそのまま使わせていただいた。


```
$ cp lambda.json.sample lambda.json
$ vi lambda.json
$ # slack の posturl や channel、lambda function の role の設定
  
$ # lambda function をアップロードするアカウントの設定をする
$ docker-compose run upload bash
# aws configure
# exit
# # setup credentials in ./aws/

$ docker-compose up
$ # Fin となったら CTRL-C で中断
```

lambda-uploader の variables 設定は config と option の両方を設定した場合に option で config が上書きされます。
