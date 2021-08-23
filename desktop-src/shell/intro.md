---
description: A Windows interface do usuário fornece aos usuários acesso a uma ampla variedade de objetos necessários para executar aplicativos e gerenciar o sistema operacional.
title: Guia do desenvolvedor do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7e6fbef1a8e34746d3b430faa5cb03f93613bc7c35e047cdd35afeb4921a37fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032294"
---
# <a name="shell-developers-guide"></a>Guia do desenvolvedor do Shell

A Windows interface do usuário fornece aos usuários acesso a uma ampla variedade de objetos necessários para executar aplicativos e gerenciar o sistema operacional. Os mais diversos e familiares desses objetos são as pastas e arquivos que residem em unidades de disco do computador. Também há vários objetos virtuais que permitem que o usuário faça tarefas como enviar arquivos para impressoras remotas ou acessar o Lixeira. O Shell organiza esses objetos em um namespace hierárquico e fornece aos usuários e aplicativos uma maneira consistente e eficiente de acessar e gerenciar objetos.

## <a name="in-this-section"></a>Nesta seção

-   [Considerações sobre segurança: Microsoft Windows Shell](sec-shell.md)
-   [Diretrizes para implementar extensões In-Process dados](shell-and-managed-code.md)
-   [Versões do Shell e controles comuns](versions.md)
-   [Implementando as interfaces de objeto de pasta básica](nse-implement.md)
-   [Implementando um formato de arquivo personalizado](customizing-file-types-bumper.md)
-   [Extensibilidade do shell (criando uma fonte de dados)](shell-extensibility-bumper.md)
-   [Implementando Painel de Controle itens](control-panel-applications.md)
-   [Dando suporte a aplicativos shell](application-support-bumper.md)
-   [Tópicos do Shell Herddo](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a>Convenções de documento

O Guia dos Desenvolvedores do Shell segue as convenções comuns Windows documentos do SDK (Software Development Kit). Duas convenções em particular devem ser notadas:

-   O código de exemplo omite o código de correção de erro normal. Esse código foi removido apenas para tornar o código mais acessível. Você deve incluir todo o código de correção de erro apropriado em seus próprios aplicativos.
-   Para deixar as entradas de registro de exemplo claras, os nomes de chave, sub-chave e entrada, bem como valores, são exibidos com uma fonte padrão. Os nomes de item definidos pelo usuário ou pelo aplicativo são itálico.

 

 



