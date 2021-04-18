---
description: O ICE91 lançará um aviso se um arquivo, arquivo. ini ou arquivo de atalho for instalado em um diretório somente por usuário.
ms.assetid: 1834d841-b1d9-4646-8057-a41dd88310b6
title: ICE91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f5723369c21894817dacbc1755430a31f17199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752649"
---
# <a name="ice91"></a>ICE91

O ICE91 lançará um aviso se um arquivo, arquivo. ini ou arquivo de atalho for instalado em um diretório somente por usuário. Esses avisos serão inofensivos se o pacote for usado apenas para instalação no contexto de [instalação](installation-context.md) por usuário e nunca for usado para instalações por máquina.

Arquivos, arquivos. ini ou atalhos em diretórios somente por usuário são instalados em um perfil de usuário específico. Mesmo que o usuário defina a propriedade [**AllUsers**](allusers.md) para instalações por computador, arquivos, arquivos. ini ou atalhos em diretórios somente por usuário não serão copiados no perfil "todos os usuários" e não estarão disponíveis para outros usuários. Os diretórios somente por usuário não variam com a propriedade **AllUsers** . A seguir está uma lista dos diretórios somente por usuário:

-   AppDataFolder
-   FavoritesFolder
-   NetHoodFolder
-   PersonalFolder
-   PrintHoodFolder
-   RecentFolder
-   SendToFolder
-   MyPicturesFolder
-   LocalAppDataFolder

## <a name="result"></a>Resultado

ICE91 posta os seguintes avisos.



| Aviso de ICE91                                                                                                                                                                                                                            | Descrição                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| O arquivo ' \[ 1 \] ' será instalado no diretório por usuário ' \[ 2 \] ' que não varia com base no valor [**AllUsers**](allusers.md) . Esse arquivo não será copiado para cada perfil de usuário, mesmo que uma instalação por computador seja desejada.     | O arquivo é instalado em um diretório somente por usuário. Ele não é instalado em cada perfil de usuário durante uma instalação por máquina.      |
| O IniFile ' \[ 1 \] ' será instalado no diretório por usuário ' \[ 2 \] ' que não varia com base no valor [**AllUsers**](allusers.md) . Esse arquivo não será copiado para cada perfil de usuário, mesmo que uma instalação por computador seja desejada.  | O arquivo. ini é instalado em um diretório somente por usuário. Ele não é instalado em cada perfil de usuário durante uma instalação por máquina. |
| O atalho ' \[ 1 \] ' será instalado no diretório por usuário ' \[ 2 \] ' que não varia com base no valor [**AllUsers**](allusers.md) . Esse arquivo não será copiado para cada perfil de usuário, mesmo que uma instalação por computador seja desejada. | O atalho é instalado em um diretório somente por usuário. Ele não é instalado em cada perfil de usuário durante uma instalação por máquina.  |



 

## <a name="example"></a>Exemplo

ICE91 relata os seguintes avisos para o exemplo:

``` syntax
The file 'File1' will be installed to the per user directory 'MyPicturesFolder' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The IniFile 'IniFile1' will be installed to the per user directory 'MyIniDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The shortcut 'Shortcut1' will be installed to the per user directory 'MyShortcutDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.
```

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | Componente\_ |
|-------|-------------|
| Arquivo1 | C1          |



 

[Tabela de componentes](component-table.md) (parcial) (parcial) (parcial) (parcial)



| Componente | Diretório\_ |
|-----------|-------------|
| C1        | MyDir       |



 

[Tabela IniFile](inifile-table.md)



| IniFile  | DirProperty |
|----------|-------------|
| IniFile1 | MyIniDir    |



 

[Tabela de atalho](shortcut-table.md)



| Atalho  | Diretório\_   |
|-----------|---------------|
| Shortcut1 | MyShortcutDir |



 

[Tabela de diretórios](directory-table.md)



| Diretório     | Pai do diretório \_  |
|---------------|--------------------|
| MyDir         | FavoritesFolder    |
| MyIniDir      | LocalAppDataFolder |
| MyShortcutDir | PersonalFolder     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



