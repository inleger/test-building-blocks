# Simple Kubernetes workload

Felelős: Kákonyi István

A blokk tartalmazza, hogy egy image-et hogyan lehet kubernetes által kezelt konténerként futtatni. Az alábbi példákat tartalmazza:

- Deployment típusú workload


## Felhasznált anyagok

- https://kubernetes.io/docs/concepts/workloads/controllers/deployment/  


## Verziók

- min.: OKD 4.12


## Magyarázat

A Deployment egy vagy több konténer életciklusának kezelésére való. Alapvetően arra szolgál, hogy a konténereket futtassa. A futtatás alapesetben állapotmentes. A Deployment leíróban meg kell adni a kívánt állapotot, aminek hatására a kubernetes a tényleges állapotot a kívánt állapotra változtatja.

A Kubernetes Deployment leírók tipikus használati esetei a következők:
- Alkalmazás frissítése (Rolling updates)
- Automatikus helyreállítás (Self-healing)
- Skálázás (Scaling)
- Környezetek közötti különbségek kezelése
- Verziókövetés és visszagörgetés
- Több alkalmazásverzió kezelése
- Különböző konfigurációk kezelése


## Függőségek

- Nincsenek 


## Kipróbáláshoz szükséges technikai infók (Pl. hozzáférések beállítása, manuális telepítési lépések, stb...)

- legalább admin szintű hozzáférés az OKD T11-T14 klaszter valamelyik namespace-éhez.


## Telepítés

Az OKD T11-T14 clusterbe telepíthető az alábbi parancsot kiadva a gyökér könyvtárból:

kubectl kustomize -k samples/kustomize/overlays/g3nonprod-t11-t14

## Állapot

- [x] Dokumentáció
- [~] Rererencia kód 
- [x] Referencia leíró
- [~] Kódváz
- [~] Komponens
- [x] Telepíthető, működőképes
- [~] HA megvalósítás
- [~] Security ellenőrzött megvalósítás
- [~] Adatot perzisztál PVC-re

## Confluence link

https://alerant.atlassian.net/wiki/spaces/~6155690b72f6970069123cc1/pages/6539149321/kubernetes-workload

## Továbbfejlesztési lehetőség

- StatefulSet típusú workload bemutatása
- DaemonSet típusú workload bemutatása
- Job típusú workload bemutatása
- CronJob típusú workload bemutatása

## További kapcsolódó blokkok

- 