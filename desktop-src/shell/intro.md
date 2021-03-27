---
description: A interface do usuário do Windows fornece aos usuários acesso a uma ampla variedade de objetos necessários para executar aplicativos e gerenciar o sistema operacional.
title: Guia do desenvolvedor do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1be17ca90b7138294be3e1b34fa3fcb4dcb4227a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988776"
---
# <a name="shell-developers-guide"></a>Guia do desenvolvedor do Shell

A interface do usuário do Windows fornece aos usuários acesso a uma ampla variedade de objetos necessários para executar aplicativos e gerenciar o sistema operacional. Os mais numerosos e familiares desses objetos são as pastas e os arquivos que residem nas unidades de disco do computador. Também há uma série de objetos virtuais que permitem ao usuário realizar tarefas como enviar arquivos para impressoras remotas ou acessar a lixeira. O Shell organiza esses objetos em um namespace hierárquico e fornece aos usuários e aplicativos uma maneira consistente e eficiente de acessar e gerenciar objetos.

## <a name="in-this-section"></a>Nesta seção

-   [Considerações de segurança: Shell do Microsoft Windows](sec-shell.md)
-   [Diretrizes para implementar extensões de In-Process](shell-and-managed-code.md)
-   [Versões do Shell e de controles comuns](versions.md)
-   [Implementando as interfaces de objeto de pasta básica](nse-implement.md)
-   [Implementando um formato de arquivo personalizado](customizing-file-types-bumper.md)
-   [Extensibilidade do Shell (criando uma fonte de dados)](shell-extensibility-bumper.md)
-   [Implementando itens do painel de controle](control-panel-applications.md)
-   [Suporte a aplicativos do Shell](application-support-bumper.md)
-   [Tópicos de shell herdados](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a>Convenções de documento

O guia de desenvolvedores do Shell segue as convenções de documento comuns do SDK (Software Development Kit) do Windows. Duas convenções em particular devem ser observadas:

-   O código de exemplo omite o código de correção de erro normal. Esse código foi removido apenas para tornar o código mais legível. Você deve incluir todo o código de correção de erro apropriado em seus próprios aplicativos.
-   Para tornar as entradas de registro de exemplo clara, chave, subchave e nomes de entrada, bem como os valores são exibidos com uma fonte padrão. Os nomes de itens definidos pelo usuário ou pelo aplicativo estão em itálico.

 

 



