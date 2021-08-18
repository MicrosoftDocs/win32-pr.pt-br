---
title: Documento do serviceInfo para uma loja online tipo 2
description: Documento do serviceInfo para uma loja online tipo 2
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Windows Media Player repositórios online, documento do serviceinfo
- repositórios online, documento do serviceInfo
- tipo 2 lojas online, documento do serviceInfo
- Documento do serviceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6830b4c54b037f254adb21624ed893ec16fa9b3973dfe1536170dff1b4f9e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995426"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a>Documento do serviceInfo para uma loja online tipo 2

O tipo 2 provedores de loja online devem fornecer à Microsoft a URL de um documento XML que descreve a loja online. Windows Media Player 10 e Windows Media Player 11 use este documento para determinar como configurar a interface do usuário para hospedar o repositório online.

no Windows Media Player 10, o documento do serviceinfo fornece o seguinte:

-   informações sobre como configurar os painéis de tarefas que Windows Media Player exibe quando o repositório online está ativo. Um repositório online pode ter um, dois ou três painéis de tarefas.
-   Informações usadas para configurar os botões do painel de tarefas, como o texto do botão, a cor do botão e as dicas de ferramenta para os botões.
-   URLs para imagens que Windows Media Player exibe para identificar a loja online.
-   URLs de páginas da web, fornecidas pela loja online, que Windows Media Player hospeda em sua interface do usuário.
-   informações sobre como Windows Media Player instalação deve configurar o primeiro armazenamento online que o usuário vê.

no Windows Media Player 11, o documento do serviceinfo fornece o seguinte:

-   Informações usadas para configurar o botão para lojas online guia, como o texto do botão e a dica de ferramenta para o botão.
-   URLs para imagens que Windows Media Player exibe para identificar a loja online.
-   URLs de páginas da web, fornecidas pela loja online, que Windows Media Player hospeda em sua interface do usuário.

Ao começar a desenvolver sua loja online, você deve fornecer à Microsoft a URL para seu documento do serviceInfo. durante a fase de desenvolvimento, sua loja online aparecerá em Windows Media Player somente quando uma chave de registro especial for definida.

depois que sua loja online é publicada, o cenário ususal é que Windows Media Player recupera o documento do seu serviceinfo da Web automaticamente. em alguns casos, no entanto, Windows Media Player recupera o documento de informações do computador do usuário. Para obter mais informações, consulte [definindo a loja online inicial](setting-the-initial-online-store.md).

quando Windows Media Player recupera o documento serviceinfo da Web, ele anexa uma cadeia de caracteres de consulta à URL. a cadeia de caracteres de consulta contém parâmetros que fornecem informações sobre a localidade do usuário e a versão Windows Media Player.

Você pode criar documentos de informações estáticas ou dinâmicas. Um documento do serviceInfo estático tem uma extensão de nome de arquivo .xml. Um documento de informações dinâmicas é uma página ASP e tem uma extensão de nome de arquivo. asp ou. aspx.

Nem todos os elementos disponíveis para uso no documento do serviceInfo podem ser usados por cada loja online e alguns elementos são opcionais para todas as lojas online. para obter informações sobre os tipos de lojas online que você pode criar e os recursos disponíveis para cada tipo, consulte [Windows Media Player lojas online](windows-media-player-online-stores.md).

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

 

 




