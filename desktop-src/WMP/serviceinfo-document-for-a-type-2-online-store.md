---
title: Documento do serviceInfo para uma loja online tipo 2
description: Documento do serviceInfo para uma loja online tipo 2
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Repositórios online do Windows Media Player, documento do serviceInfo
- repositórios online, documento do serviceInfo
- tipo 2 lojas online, documento do serviceInfo
- Documento do serviceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb558661332ab08edd2057fa024a1a0e2034b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005663"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a>Documento do serviceInfo para uma loja online tipo 2

O tipo 2 provedores de loja online devem fornecer à Microsoft a URL de um documento XML que descreve a loja online. Windows Media Player 10 e Windows Media Player 11 Use este documento para determinar como configurar a interface do usuário para hospedar o repositório online.

No Windows Media Player 10, o documento do serviceInfo fornece o seguinte:

-   Informações sobre como configurar os painéis de tarefas que o Windows Media Player exibe quando o repositório online está ativo. Um repositório online pode ter um, dois ou três painéis de tarefas.
-   Informações usadas para configurar os botões do painel de tarefas, como o texto do botão, a cor do botão e as dicas de ferramenta para os botões.
-   URLs para imagens que o Windows Media Player exibe para identificar a loja online.
-   URLs de páginas da Web, fornecidas pela loja online, que o Windows Media Player hospeda em sua interface do usuário.
-   Informações sobre como a instalação do Windows Media Player deve configurar o primeiro armazenamento online que o usuário vê.

No Windows Media Player 11, o documento do serviceInfo fornece o seguinte:

-   Informações usadas para configurar o botão para lojas online guia, como o texto do botão e a dica de ferramenta para o botão.
-   URLs para imagens que o Windows Media Player exibe para identificar a loja online.
-   URLs de páginas da Web, fornecidas pela loja online, que o Windows Media Player hospeda em sua interface do usuário.

Ao começar a desenvolver sua loja online, você deve fornecer à Microsoft a URL para seu documento do serviceInfo. Durante a fase de desenvolvimento, sua loja online aparecerá no Windows Media Player somente quando uma chave de registro especial for definida.

Depois que a loja online é publicada, o cenário ususal é que o Windows Media Player recupera o documento do seu serviceInfo da Web automaticamente. Em alguns casos, no entanto, o Windows Media Player recupera o documento de informações do computador do usuário. Para obter mais informações, consulte [definindo a loja online inicial](setting-the-initial-online-store.md).

Quando o Windows Media Player recupera o documento de informações da Web, ele anexa uma cadeia de caracteres de consulta à URL. A cadeia de caracteres de consulta contém parâmetros que fornecem informações sobre a localidade do usuário e a versão do Windows Media Player.

Você pode criar documentos de informações estáticas ou dinâmicas. Um documento do serviceInfo estático tem uma extensão de nome de arquivo. xml. Um documento de informações dinâmicas é uma página ASP e tem uma extensão de nome de arquivo. asp ou. aspx.

Nem todos os elementos disponíveis para uso no documento do serviceInfo podem ser usados por cada loja online e alguns elementos são opcionais para todas as lojas online. Para obter informações sobre os tipos de lojas online que você pode criar e os recursos disponíveis para cada tipo, consulte [lojas online do Windows Media Player](windows-media-player-online-stores.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre as lojas online do tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Criando o documento do serviceInfo dinamicamente**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Documento de informações de exemplo para uma loja online tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento do serviceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




