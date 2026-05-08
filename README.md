# KLEA© - Serviço de Impressão

Repositório oficial de distribuição do instalador Windows do **KLEA© - Serviço de Impressão**.

Este repositório armazena os arquivos `.msi` publicados em **Releases**, para que usuários possam baixar e instalar o serviço local responsável pela integração entre a plataforma KLEA© e as impressoras conectadas ao computador.

## O Que É

O **KLEA© - Serviço de Impressão** é um serviço Windows instalado localmente na máquina que possui acesso às impressoras.

Ele permite que a plataforma KLEA© envie comandos de impressão para impressoras locais por meio de uma conexão segura com o Hub de Impressão.

## Download

A versão mais recente do instalador está disponível na aba **Releases**.

Baixe o arquivo com o nome semelhante a:

```text
KLEA©-Servico-de-Impressao-v1.0.msi
```

## Instalação

1. Acesse a plataforma KLEA©.
2. Vá até **Dispositivos e Impressoras**.
3. Gere um novo token de instalação.
4. Baixe o instalador `.msi` na aba **Releases** deste repositório.
5. Execute o instalador no computador que possui acesso às impressoras.
6. Quando solicitado, cole o token de integração gerado na plataforma.
7. Conclua a instalação.

Após a instalação, o serviço será registrado no Windows como:

```text
KLEA© - Serviço de Impressão
```

## Requisitos

- Windows 10 ou superior
- Permissão de administrador para instalar serviços Windows
- Acesso à internet
- Impressora instalada e acessível no computador
- Token de integração gerado na plataforma KLEA©

## Como Verificar Se Está Funcionando

No Windows:

1. Abra `services.msc`.
2. Localize o serviço **KLEA© - Serviço de Impressão**.
3. Confirme se o status está como **Em execução**.
4. Volte para a plataforma KLEA© e atualize o status em **Dispositivos e Impressoras**.

Na plataforma, o status esperado é:

```text
Hub de Impressão: Online
Serviço Windows: Online
```

## Atualização

Para atualizar o serviço:

1. Baixe a versão mais recente do `.msi` em **Releases**.
2. Execute o instalador.
3. Informe um token válido quando solicitado.
4. Conclua a instalação.

O instalador substitui a versão anterior mantendo o serviço configurado para inicialização automática.

## Desinstalação

Para remover o serviço:

1. Abra **Configurações do Windows**.
2. Vá em **Aplicativos**.
3. Localize **KLEA© - Serviço de Impressão**.
4. Clique em **Desinstalar**.

Também é possível remover pelo Painel de Controle em **Programas e Recursos**.

## Solução De Problemas

### O serviço aparece offline na plataforma

Verifique:

- O serviço Windows está em execução.
- O token informado na instalação é válido e não foi revogado.
- O computador tem acesso à internet.
- A impressora está instalada e disponível.
- O antivírus ou firewall não está bloqueando a conexão do serviço.

### O Hub está online, mas o Serviço Windows está offline

Isso geralmente indica que o serviço local não conseguiu autenticar ou conectar ao Hub.

Tente:

1. Gerar um novo token na plataforma.
2. Reinstalar o `.msi`.
3. Colar o token completo no instalador.
4. Reiniciar o serviço Windows.

### A impressora não aparece ou aparece indisponível

Verifique:

- A impressora está ligada.
- O driver está instalado corretamente.
- A impressora não está marcada como offline no Windows.
- O computador consegue imprimir uma página de teste pelo próprio Windows.

## Logs

Eventos do serviço podem ser consultados no **Visualizador de Eventos do Windows**:

```text
Logs do Windows > Aplicativo
```

Fontes comuns:

```text
LabelPrintService
LabelPrintServiceInstaller
MsiInstaller
```

## Versões

As versões publicadas seguem o padrão:

```text
KLEA©-Servico-de-Impressao-vX.Y.msi
```

Exemplo:

```text
KLEA©-Servico-de-Impressao-v1.0.msi
```

## Observação

Este repositório é destinado apenas à distribuição dos instaladores oficiais do **KLEA© - Serviço de Impressão**.

O código-fonte do serviço e da plataforma não faz parte deste repositório.
