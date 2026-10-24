# MinDag – offentliga, krypterade uppdateringar

Det här repot innehåller enbart **krypterade uppdateringsfiler** för MinDag och
en liten versionslista. Ingen installations-ZIP, källkod, lösenordsfil,
familjeschema, personbild eller säkerhetskopia finns här.

Första installationen lämnas privat till varje användare. Då väljer de samma
uppdateringslösenord på sin Raspberry Pi. Från MinDag 1.45.0 kontrollerar
webbredigeraren `latest.json` högst en gång per dygn och erbjuder uppdatering
först när en nyare version finns. Installationen kräver ett aktivt val och
uppdateringslösenordet. En säkerhetskopia tas före bytet.

En `.mdu`-fil är krypterad med AES-256-GCM och ett nyckelvärde härlett från
det gemensamma lösenordet. Det skyddar mot vanlig nedladdning, men är inte ett
kopieringsskydd mot någon som har full tillgång till en installerad Pi.

Senaste filen: [MMM-MinDag-1.45.3.mdu](MMM-MinDag-1.45.3.mdu). Kontrollera
nedladdningen med `sha256sum -c MMM-MinDag-1.45.3.mdu.sha256` innan manuell
installation. Pi:ns uppdaterare kontrollerar dessutom filen automatiskt.

Äldre `.mdu`-filer ingår inte längre i den aktuella grenen. Tidigare Git-commits
kan fortfarande innehålla dem; ett lösenordsbyte kan inte göra redan publicerade
filer hemliga i efterhand.
