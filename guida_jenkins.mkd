#Configurazione Ambiente per testing C.I. con Jenkins ,server Appium ,Cucumber-Jvm,Applicazioni mobile, con repositories Git.
Con il seguente documento vogliamo aiutare chi si avvicina al mondo del testing C.I(continuous integration) con le applicazioni mobile.
Di seguito i software e i framework che utilizzeremo:

* [Jenkins](http://jenkins-ci.org/) 
* [Cucumber](http://cukes.info/)
* [Appium](http://appium.io/)



Una delle applicazioni più utilizzate nel mondo del C.I. è [Jenkins](http://jenkins-ci.org/)
 
##Installare *Jenkins*
E' possibile installare Jenkins sia in modo nativo
sia come applicativo .war. (Al link iniziale *Jenkins* c'è un tutorial molto esaustivo)


Una volta installato jenkins bisogna creare le utenze e configurarlo.

Iniziamo con l'aggiungere a Jenkins i plugin che servono.

Cliccare su configura Jenkins(per chi ha le versione inglese andare sulla voce di menù corrispettiva figura sottostante)


![Configurazione Job](file:///home/nicola/Immagini/Schermata%20del%202014-03-17%2014:19:58.png "Configurazione Job")

Nella pagina che si ottiene cliccare su gestisci plugin come nella figura seguente

![Configurazione Job](file:///home/nicola/Immagini/Schermata%20del%202014-03-17%2014:19:58.png "Configurazione Job")

nell'attuale pagina clicca su aggiornamenti disponibili e cercare gli aggiornamenti a cui siamo interessati, selezioniamoli e installiamoli.

Gli aggiornamenti che noi abbiamo installato sono i seguenti:

* Android Emulator Plugin
* Credentials Plugin
* Cucumber Plugin
* Git Server 
* GitHub
* GIT Client
* GIT Plugin
* Gradle Plugin
* Redmine plugin
* SSH Slaves plugin(se si vogliono utilizzare macchine in slave)
* Xvnc plugin
* SSH Credentials Plugin
* Matrix Authorization Plugin

alla fine ne saranno di più perchè alcuni hanno dipendenze da altri.
(se lavoriamo sotto proxy non dimentichiamo di configurarlo)

Dopo aver installato i plugin c'è una voce che permette il riavvio automatico di jenkins selezioniamola e jenkins sarà riavviato

Dopo aver riavviato Jenkins aggiungiamo le utenze, 
cliccando sulla voce *Configure Global Security*,
nella nuova pagina selezioniamo Enable security e decidiamo come autenticarci noi ambiamo fatto come di seguito:

![Configurazione Job](file:///home/nicola/Immagini/Schermata%20del%202014-03-17%2014:19:58.png "Configurazione Job")



**<span style="color:red"> Non dimentichiamo di settare i permessi e le password</span>**

Dopo aver aggiunto e settato le nuove utenze configuriamo l'ambiente Jenkins; settando le variabili globali, il path del sdk android, Xvnc, Git, Gradle, Maven, ecc di seguito un esempio della nostra configuralzione:

![Configurazione Job](file:///home/nicola/Immagini/Schermata%20del%202014-03-17%2014:19:58.png "Configurazione Job")

una volta configurato l'ambiente passiamo a configurare i job.



#Configurazione Jenkins Jobs
---
Loggarsi inserendo *__Username__* e *__Password__*

Cliccare su *__Nuovo Job__*

Selezionare il tipo di Job che si vuole creare, dargli un nome e premere **OK**

esempio:
![Configurazione Job](file:///home/nicola/Immagini/Schermata%20del%202014-03-17%2014:19:58.png "Configurazione Job")


