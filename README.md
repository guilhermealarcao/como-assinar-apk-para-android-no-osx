# como-assinar-apk-para-android-no-osx
Como assinar APK para android no OSX


Para criação de APKs com assinatura é necessário a criação de uma chave ( key ) de identificação essa servirá para identificações futuras do proprietário do APP.

Para gerar essa key utilize o comando a seguir no seu terminal  , lembrando que será gerada a chave (key ) aonde o comando for executado:

<pre>
keytool -genkey -v -keystore example.keystore -alias example -keyalg RSA -keysize 2048 -validity 10000
</pre>

O cordova "builda" as APKs por duas formas diferentes uma utilizando o <b>Gradle Build Tool</b> e o <b>Apache Ant</b>

As versões mais recentes do cordova estão utilizando <b>Gradle Build Tool</b> porém irei mostrar as duas formas caso alguém precise.

<h2>Utilizando <b>Gradle Build Tool</b> </h2>
Quando utilizamos o <b>Gradle</b> precisaremos criar um arquivo chamado <b>build.json</b> com seguinte codigo:
<pre>
{
 "android": {
     "release": {
         "keystore":"c:\\my-release-key.keystore",
         "storePassword":"pwd123",
         "alias":"johnS",
         "password":"pwd123",
         "keystoreType":""
       }
   }
}
</pre>
O arquivo deve ser criado preferencialmente no mesmo diretorio que a chave(key) foi criado
<h2>Utilizando <b>Apache Ant</b></h2>
Quando utilizamos o <b>Ant</b> para realizar a build precisaremos criar um arquivo chamado <b>ant.properties</b> com seguinte codigo:
<pre>
key.store=example.keystore
key.alias=example
</pre>
