# SOLUCIÓN: Error 403 - Permisos de GitHub en Claude Code

## PROBLEMA
Clause Code muestra error 403: "Resource not accessible by integration"
Causa: La integración de GitHub en Claude Code sólo tiene permisos de lectura.

## SOLUCiÓN INMEDIATA

DEBES hacer esto EN TU IDE (Cursor, VS Code, etc.) - NO en el navegador:

### Opción 1: Desconectar y reconectar con permisos correctos

1. Abre Claude Code en tu IDE
2. 2. Ve a **Settings** (Ctrl+,)
   3. 3. Busca "GitHub" en la búsqueda
      4. 4. Encuentra la sección "Connections" → "GitHub"
         5. 5. Haz clic en el botón **"Disconnect"** (Desconectar)
            6. 6. Haz clic en **"Connect to GitHub"** nuevamente
               7. 7. Cuando GitHub te pida permisos, **ASEGÚRATE DE CONCEDER**:
                  8.    - Repository contents (write)
                        -    - Commits
                             -    - Push access
                                  - 8. Completa el flujo de autorización
                                   
                                    9. ### Opción 2: Usar Personal Access Token (más rápido)
                                   
                                    10. Si Claude Code permite:
                                   
                                    11. 1. Ve a Settings → Connections → GitHub
                                        2. 2. Busca una opción "Authentication Method" o "Use Personal Access Token"
                                           3. 3. Selecciona "Personal Access Token"
                                              4. 4. Pega este token:
                                                 5.    ```
                                                    github_pat_11CJLPSJy05KcJ41Au185Eg_7q4neQJ1439X3vofpztw1FxhTqzCn0h
                                                    ```
                                                    5. Confirma
                                                    6. Desconecta y reconecta la sesión de Claude Code

                                                    ## REPOSITORIO CONFIGURADO

                                                    - Repo: `edutri25-star/prueba-cloud`
                                                    - Permisos de token: Contents (Read and Write) ✅
                                                    - README: Creado ✅
                                                    - Listo para push: Sí ✅

                                                    ## DESPUÉS DE ARREGLARLO

                                                    Una vez que reconectes con los permisos correctos:
                                                    1. El error 403 desaparecerá
                                                    2. Podrás hacer push sin problemas
                                                    3. El commit c04e73e se subirá exitosamente

                                                    ---

                                                    **NOTA IMPORTANTE**: Este cambio DEBE hacerse desde tu IDE local, no desde el navegador.
                                                    No puedo acceder a Settings de Claude Code desde aquí porque está en tu computadora.
