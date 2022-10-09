# sensors-checker-service

Сервис агрегатор, собирающие данные с различных сервисов датчиков.

### Немного о реализации

Чтобы каждый раз не прослушивать данные с сервисов, было решено реализовать простенькое in memory хранилище данных, данные в этом хранилище будут обновляться с определенным промежутком времени.  
Когда другие сервисы будут обращаться к сервису-агрегатору, он будет лезть в это in memory хранилище и будет доставать данные от туда. Это эффективнее, чем каждый раз по новому опрашивать сервисы датчики.  
