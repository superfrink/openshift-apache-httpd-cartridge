# OpenShift Apache Httpd Cartridge

= 使い方


== Gear の作成
rhc create-app <APP_NAME> https://raw.githubusercontent.com/akubicharm/openshift-apache-httpd-cartridge/master/metadata/manifest.yml


== Gear の動作確認
ブラウザでGearのURLにアクセスし
Hello World!
と表示されれば、アプリケーションの作成成功です。

== ファイルの確認
* ログファイル
<ギアのトップディレクトリ＞/httpd/logs
# httpd.conf の確認
<ギアのトップディレクトリ>/etc/httpd.conf

== httpd.conf
httpd.conf ファイルは <GIT_REPOSITORY>/etc/httpd.conf.erb をベースにGear作成時に生成される。
生成されるファイルを確認するには、必要な環境変数を設定し
erb httpd.conf.erb
を実行する。　

= その他のTips
git push したときに Fobidden となって、反映できない場合
git remote set-url origin https://[username]@github.com/[username]/[appname]
git config -list
git push -u origin master

例)
git remote set-url origin https://akubicharm@github.com/akubicharm/openshift-apache-httpd-cartridge.git


= 参照ドキュメント
https://blogs.openshift.com/new-openshift-cartridge-format-part-1/
https://blogs.openshift.com/new-openshift-cartridge-format-part-2/
http://openshift.github.io/documentation/oo_cartridge_developers_guide.html
