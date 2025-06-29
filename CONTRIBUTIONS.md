 Contribuciones de Alex Vega

## Sprint 1
- **2025-06-24 (Dia 1):**

- Se agregan dockerfile y archivo python para la app de ejemplo, se usa Flask y se muestra la hora actual en zonas UTC y Lima.
  - **Commit:** `a7be7d56bd7746479d6e3ce888651e12f69c9711`
  - **Commit:** `fb0da48c84dd0b00f4b7fc15a8b0e3631deb0e40`

- Se agregan archivo manifest inicial para despliegue de pods y servicio en kubernetes, se modifica README para mostrar los pasos del despliegue.
  - **Commit:** `15034c7bc69c09a3fc3697bac29a6e0ce48fa50b`
  - **Commit:** `34706e1413c2eae84aac06d4c27a80761b33fab7`

- **Tareas en kanban board:**
  - [https://github.com/grupo10-CC3S2/Proyecto7-PC4/issues/3](https://github.com/grupo10-CC3S2/Proyecto7-PC4/issues/3)
  - [https://github.com/grupo10-CC3S2/Proyecto7-PC4/pull/13](https://github.com/grupo10-CC3S2/Proyecto7-PC4/pull/13)

- **Pull request:**
  - [https://github.com/grupo10-CC3S2/Proyecto7-PC4/pull/13](https://github.com/grupo10-CC3S2/Proyecto7-PC4/pull/13)

## Sprint 2
- **2025-06-27 (Dia 3):**

- Se agrega Makefile para comandos de setup y limpiar recursos para desplegar los pods y apps.
  * **Commit:** `f924f9ba69cee1280cd0dc94a97b649f384c2297`

- Se agrega loggers, en 3 nivels (warning, error e info) a la app de Flask
  - **Commit:** `d145309c6dd389df8c12958e5e2b0d8a61f55aee`

- Uso de devcontainer para despliegue y uso de `fluxcd`:
  - **Commit:** `dfa1982e7e4f57df03f218a50c0da04e00faaf2d`

- Se realiza setup de `kontributions` y `repository` de `fluxcd` para el repositorio, se agrega archivo de configuracion `flux-gitrepository.yaml` y `flux-kustomization`  y se agrega el namespace `default`.
  - **Commit:** `20805e2bac970f5d8a101f164452b91339572315`
  - **Commit:** `b44c68a1252c673147b3de71a8294014e2fe7952`
  - **Commit:** `957948ae36f54b219b630c94b220e258e19d9682`

- Para el uso de `fluxcd` se usa commits y cambio de imagenes que realizara cambios locales si se encuentra `configuration drift`, por lo que se cambia la version de imagen:
  - **Commit:** `a04ec92ecf9d7c90821274c42e439605bfc03001`

- **Tareas en kanban board:**
  - [https://github.com/grupo10-CC3S2/Proyecto7-PC4/issues/8](https://github.com/grupo10-CC3S2/Proyecto7-PC4/issues/8)
  - [https://github.com/grupo10-CC3S2/Proyecto7-PC4/pull/20](https://github.com/grupo10-CC3S2/Proyecto7-PC4/pull/20)

- **Pull request:**
  - [https://github.com/grupo10-CC3S2/Proyecto7-PC4/pull/20](https://github.com/grupo10-CC3S2/Proyecto7-PC4/pull/20)

## Sprint 3
- **2025-06-28 (Dia 4):**
- Se modifica la app para agrega ruta `/health` para tests, se actualiza imagen a v3.
  - **Commit:** `aed328bf9c1ac403fc821afe6e759cb51dd1b56a`
  - **Commit:** `3eb65faf39c9701fe5660341bc4313cd7e714ade`

- Se agrega `conftest.py` para uso de fixtures que se usaran en tests de health y e2e, se realiza uso de libreria `kubernetes` para interactuar con el cluster de kubernetes y obtener informacion de los recursos.
  * **Commit:** `6de23196d068f966ceb4243eea30451e180be461`

- **2025-06-29 (Dia 5):**

- Se agrega tests de health para infraestructura (pods de kubernetes) que revisa el despliegue y salud usando libreria `kubernetes` de python.
  - **Commit:** `74bca3831a117401a66053c66ea8a551f508e957`
  - **Commit:** `a7806e61e612658b102fc2061626735c8791bff2`

- Se agrega test e2e qu verifica que todo el pipeline de observabilidad funcionen, se usa el ciclo AAA (Arrange, Act, Assert) para verificar que se crean directorios, logs y metricas y se usa teardown para borrar los archivos creados. Se moficia conftest para lograr estos pasos con fixtures a nivel `function` puesto que se requiere que cada test sea independiente.
  - **Commit:** `32010034d1f8a4f44dd94434356e37400cde6603`
  - **Commit:** `d52fb9c6ed34f716333ac4333ad09ffa01d3b6c5`

- **Tareas en kanban board:**
  - [https://github.com/grupo10-CC3S2/Proyecto7-PC4/issues/10](https://github.com/grupo10-CC3S2/Proyecto7-PC4/issues/10)
  - [https://github.com/grupo10-CC3S2/Proyecto7-PC4/issues/11](https://github.com/grupo10-CC3S2/Proyecto7-PC4/issues/11)
  - [https://github.com/grupo10-CC3S2/Proyecto7-PC4/pull/24](https://github.com/grupo10-CC3S2/Proyecto7-PC4/pull/24)

- **Pull request:**
  - [https://github.com/grupo10-CC3S2/Proyecto7-PC4/pull/24](https://github.com/grupo10-CC3S2/Proyecto7-PC4/pull/24)
