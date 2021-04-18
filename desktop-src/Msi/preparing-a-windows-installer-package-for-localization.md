---
description: Siga estas diretrizes para facilitar a localização de pacotes de Windows Installer.
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: Preparando um pacote de Windows Installer para localização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa46af5259b880398aa84dc817eb201bd63456eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752842"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a>Preparando um pacote de Windows Installer para localização

A localização de um pacote de Windows Installer em vários idiomas pode ser bastante facilitada fazendo o seguinte:

-   Crie um banco de dados de instalação base que seja uma página de código neutra. Consulte [criando um banco de dados com uma página de código neutra](creating-a-database-with-a-neutral-code-page.md). A página de código do banco de dados localizado pode ser definida importando uma tabela de arquivamento de texto com uma página de código não neutra no banco de dados base. Consulte [Configurando a página de código de um banco de dados](setting-the-code-page-of-a-database.md).
-   Organize arquivos que exigem localização em componentes separados e instale esses arquivos em diretórios separados. Isso garante que dois pacotes localizados nunca instalem arquivos com nomes idênticos no mesmo diretório.

Por exemplo, um aplicativo em todo o mundo usando os recursos a seguir pode ter três componentes.



| Componente | Recurso                   |
|-----------|----------------------------|
| PAÍSES     | worldwide.exe              |
| PAÍSES     | entradas de registro mundiais |
| PAÍSES     | atalho mundial         |
| ENG       | engui.dll                  |
| ENG       | readme.txt                 |
| FRA       | fraui.dll                  |
| FRA       | readme.txt                 |



 

Os arquivos que precisam ser localizados podem ser instalados nos seguintes locais de diretório:

-   \[ProgramFilesFolder \] \\ mundo \\worldwide.exe
-   \[ProgramFilesFolder \] \\ mundial \\ em inglês \\engui.dll
-   \[ProgramFilesFolder \] \\ mundial \\ em inglês \\readme.txt
-   \[fraui.dll ProgramFilesFolder do \] \\ mundo \\ francês \\
-   \[readme.txt ProgramFilesFolder do \] \\ mundo \\ francês \\

 

 



