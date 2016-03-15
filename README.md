# Semana da Computação 2016 - Inatel - Segurança em dispositivos Android
Slides e ferramentas utilizadas na apresentação do Inatel

Para acessar alguns tutoriais feitos por mim acesse : http://www.prisciladev.com

Pré requisito:
- Android SDK (stand-alone): http://developer.android.com/intl/pt-br/sdk/installing/index.html 
- Java JDK: http://www.oracle.com/technetwork/pt/java/javase/downloads/jdk8-downloads-2133151.html

Algumas ferramentas úteis para android assessment:
- Drozer : https://labs.mwrinfosecurity.com/tools/drozer/
- Androbugs : https://github.com/AndroBugs/AndroBugs_Framework
- MobSF: https://github.com/ajinabraham/Mobile-Security-Framework-MobSF

Drozer utilizado nesta apresentação:

Instale o agent.apk no celular desejado:

> adb install agent.apk

Depois: Abrir o app agent no celular e ligar o server

Lista de comandos:

Conectar o server com o adb:
> adb forward tcp:31415 tcp:31415

Iniciar o console do drozer:
> drozer console connect

Lista todos os apps:
> run app.package.list

Para descobrir o nome do pacote da aplicação desejada:
> run app.package.list -f testapp

Para saber mais informações sobre o app
> run app.package.info -a com.isi.testapp

Verificar se o app possui alguma superficie de ataque
> run app.package.attacksurface com.isi.testapp

Para descobrir o nome das Activities exportadas
> run app.activity.info -a com.isi.testapp

Comando para chamar uma Activity
> run app.activity.start –component com.isi.testapp com.isi.testapp.Welcome


