---
title: Integrando o recurso de exibição do centro de informações
description: Integrando o recurso de exibição do centro de informações
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Lojas online do Windows Media Player, integrando o modo de exibição do centro de informações
- lojas online, integração da exibição do centro de informações
- Digite 1 lojas online, integração da exibição do centro de informações
- Digite 2 lojas online, integrando a exibição do centro de informações
- Lojas online do Windows Media Player, exibição do centro de informações
- lojas online, exibição do centro de informações
- tipo 1 lojas online, exibição do centro de informações
- tipo 2 lojas online, exibição do centro de informações
- integração da exibição do centro de informações
- Exibição do centro de informações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9564a6210181e0500bd1e447f621568f634817c4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761442"
---
# <a name="integrating-the-info-center-view-feature"></a>Integrando o recurso de exibição do centro de informações

O Windows Media Player permite que os usuários abram e fechem o recurso de exibição do centro de informações. A exibição do centro de informações é o recurso em que os usuários esperam encontrar informações avançadas e estendidas sobre o conteúdo específico de mídia digital. Quando o usuário opta por abrir a exibição do centro de informações, o Windows Media Player chama o repositório de músicas atual para exibir a página da Web de exibição do info Center especificada pelo atributo **URL** do elemento **InfoCenter** do documento serviceInfo.

Para recuperar informações sobre o conteúdo de mídia digital em execução no momento, você deve inserir uma instância do controle do Windows Media Player em sua página da Web e usar o modelo de objeto do Player. Por exemplo, para recuperar o título, você pode usar o seguinte código JScript:


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a>Diretrizes para a exibição do centro de informações

Ao criar sua página da Web de **exibição do info Center** , use as seguintes diretrizes:

-   A página deve identificar claramente a loja online que fornece as informações. Você pode fazer isso exibindo de forma proeminente seu logotipo, por exemplo.
-   A página deve incluir um link para a política de privacidade da sua empresa.
-   Evite navegação de página dentro do recurso de exibição do info Center sempre que possível. Você deve navegar até sua loja online para a maioria das atividades.
-   É melhor fornecer informações valiosas sem exigir que o usuário instale programas ou faça logon na sua loja online.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**External. NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Elemento do InfoCenter**](infocenter-element.md)
</dt> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Usando o controle do Windows Media Player em uma página da Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




