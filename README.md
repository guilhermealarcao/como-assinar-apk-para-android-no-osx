# como-assinar-apk-para-android-no-osx
Como assinar APK para android no OSX


Para criação de APKs com assinatura é necessário a criação de uma chave ( key ) de identificação essa servirá para identificações futuras do proprietário do APP.

Para gerar essa key utilize o comando a seguir no seu terminal  , lembrando que será gerada a chave (key ) aonde o comando for executado:

<pre>
keytool -genkey -v -keystore example.keystore -alias example -keyalg RSA -keysize 2048 -validity 10000
</pre>

O cordova "builda" as APKs por 2 formas diferentes uma utilizando o <b>Gradle Build Tool</b> e o <b>Apache Ant</b>


