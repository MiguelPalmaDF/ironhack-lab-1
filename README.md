# ironhack-lab-1
Repositorio de Laboratorio 1 de IronHack

## 1.- Branch Strategy Simulation

Esta seccion demuestra 2 procesos de estrategia de ramas para desarrollo.

Para este laboratorio se crea un repositorio para demostrar los cambios.


![LABORATORIO 1 - SCREENSHOTS](https://github.com/MiguelPalmaDF/ironhack-lab-1/assets/129919164/27e2b7e8-c47e-4d0b-b3af-c5fdea61edd3)


- ### Trunk Based Development:
  - Se realizan commits pequeños directos en la rama main o se crean ramas temporales de features las cuales al ser integradas a main deberian borrarse.
  - git add lab.info
  - git commit -m "First commit TBD"
  - git push origin main

  ![LABORATORIO 1 - SCREENSHOTS](https://github.com/MiguelPalmaDF/ironhack-lab-1/assets/129919164/03073f8e-1eee-4d66-9df9-7f062d8e5aa0)

  ![LABORATORIO 1 - SCREENSHOTS](https://github.com/MiguelPalmaDF/ironhack-lab-1/assets/129919164/8014894a-24c9-47b6-8f4d-8497306c4602)

  ![LABORATORIO 1 - SCREENSHOTS](https://github.com/MiguelPalmaDF/ironhack-lab-1/assets/129919164/d0bfb897-8ba8-4b51-bf23-bb2939ff1f51)


  
- ### GitFlow:
  - Se implementa una rama de develop, esta rama incorporará los cambios previos a enviarse a la rama main
  - De igual forma se implementan ramas de features para nuevas implementaciones, las cuales deben ser mergeadas a develop y consecuentemente a una rama de release para ser implementado a main.

  - Se implementa rama de Develop
    - git checkout -b develop

    ![Nueva nota](https://github.com/MiguelPalmaDF/ironhack-lab-1/assets/129919164/c8eaf5c5-49c7-45f1-a5b3-5b7a30c9a2a2)

  - Se implementa rama de feature para implementar cambios a partir de develop
    - git checkout -b feature/lab-1 develop

    ![featurelab-1](https://github.com/MiguelPalmaDF/ironhack-lab-1/assets/129919164/5ad721a9-84b5-422e-9bdc-429188557714)
 
    - git add feature.info
    - git commit -m "Feature branch info"
    - git push -u origin feature/lab-1
    
    ![Nueva nota](https://github.com/MiguelPalmaDF/ironhack-lab-1/assets/129919164/72f39bae-4fa5-439d-8ee8-a29b2c7d4a25)


  - Se mergean los features/cambios de la rama feature/lab-1 a develop
    - git checkout develop
    - git merge feature/lab-1
    - git push origin develop
    
    ![Nueva nota](https://github.com/MiguelPalmaDF/ironhack-lab-1/assets/129919164/42c00f2c-e801-40bf-8ad9-09a4dd598f74)

  - Se implementa rama de release para enviar los cambios de develop a main
    - git checkout -b release/1.0 develop
    - git merge develop
    - git add release.info
    - git commit -m "First release"
    - git push -u origin release/1.0

    ![Nueva nota](https://github.com/MiguelPalmaDF/ironhack-lab-1/assets/129919164/51b34227-d906-4c48-927c-8188f8e7a65c)

  - Se mergean los cambios de release/1.0 a main
    - git checkout main
    - git merge release/1.0
    - git push origin main

    ![Nueva nota](https://github.com/MiguelPalmaDF/ironhack-lab-1/assets/129919164/f08fb8ad-04b8-4d77-b2b2-a5dfed5b9a68)


## 2.- Conlflict Resolution and Merging

Se debe simular escenarios de desarrollo en el cual haya conlictos relacionados a la modificacion los mismos archivos en diferentes rama.






  
