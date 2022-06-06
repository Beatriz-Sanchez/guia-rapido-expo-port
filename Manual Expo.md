# Módulo 3 v2

### Guia rápido - projetos Expo

##### Instalando/atualizando o Expo

- verificar versão do expo:

```
expo --version
```

- instalando Expo:

```powershell
npm install -g expo-cli
```

- conferindo o login do expo:

```powershell
expo whoami
```

- verificar também a versão do npm e atualizar se precisar

```powershell
npm update -g
```

- Atualizando os pacotes expo de um projeto já começado (depois de ter atualizado a versão expo, por exemplo):

```powershell
expo upgrade
```

OU

```powershell
expo update
```



##### Iniciando um projeto Expo do 0

*** Uma pasta do projeto será criada automaticamente ao se iniciar um repositório Expo

- ir até onde você quer que a pasta fique e iniciar repositório expo

```powershell
expo i <nome do projeto> --npm
```

- Escolher a opção `blank`
- ir até a pasta do projeto antes de abrir com o code

```powershell
cd <nome do projeto>
```

- testar usando `expo start`



##### Instalando pacotes a projetos

***Evitar instalar os pacotes usando npm ou yarn diretamente, pois algumas versões mais recentes de pacotes são incompatíveis com o expo

- Sempre usar

```powershell
expo install <pacote>
```

OU

```
expo add <pacote>
```

- É possível adicionar `--npm` ou `--yarn`, mas não é necessário, ele já padroniza para o que você escolheu ao iniciar o projeto expo



##### Continuando um projeto Expo já iniciado

- dar pull em um repo já inciado, ou clonar o repo

```bash
git clone <link_git> <nome_do_branch>
```

```bash
git init
git pull <link_git> <nome_do_branch>
```

- instalar todos os pacotes que já não vieram instalados

```powershell
expo install .
```

*** verificar se veio com o .gitignore, se não veio, aqui tem um exemplo de um .gitignore padrão de um projeto expo

```gitignore
node_modules/
.expo/
dist/
npm-debug.*
*.jks
*.p8
*.p12
*.key
*.mobileprovision
*.orig.*
web-build/

# macOS
.DS_Store
```

***se o projeto for muito antigo pode não rodar em um expo go novo, talvez seja uma boa ideia rodar também o ``expo update``



##### Depurando apps Expo

- Para logs detalhados no chrome:
  1. abrir dev menu (chacoalhar celular com o app aberto)
  2. clicar na opção “debug remote JS” -> abre uma guia `localhost:19000/debugger-ui/`
  3. abrir console, os logs estarão lá conforme o app atualiza

*** Faz o app rodar mais devagar, aparece um aviso falando isso. Para silenciar o aviso:

```react
//importar LogBox de 'react-native'

LogBox.ignoreLogs(['Remote debugger'])
```



- diagnóstico (versões, aparelho, etc) - antigo expo diagnosis

```
npx expo-env-info
```

- achar problemas com o projeto (versões incompatíveis, por exemplo)

```powershell
expo doctor
```

- para já consertar direto, adicionar `--fix-dependencies`

- Você pode instalar o react-devtools para ver detalhes

```powershell
npm install -g react-devtools
```

- para usar

```powershell
react-devtools
```



##### Checando comandos

- do Expo:

  - geral:

  ```powershell
  expo --help
  ```

  - sobre um comando específico:

  ```powershell
  expo <comando> <opção>
  ```
