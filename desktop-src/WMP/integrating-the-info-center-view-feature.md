---
title: Integrando o recurso de exibição do Info Center
description: Integrando o recurso de exibição do Info Center
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Windows Media Player online, integrando o Info Center View
- lojas online, integrando o Info Center View
- tipo 1 lojas online, integrando o Info Center View
- tipo 2 lojas online, integrando o Info Center View
- Windows Media Player online, Exibição do Info Center
- lojas online, Exibição do Info Center
- tipo 1 lojas online, Exibição do Info Center
- tipo 2 lojas online, Exibição do Info Center
- integrando o Info Center View
- Exibição do Info Center
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caea279f933c3cbb411da72aab9ddf971df5f38c69d7291ae4ac67f7b96ed91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135459"
---
# <a name="integrating-the-info-center-view-feature"></a>Integrando o recurso de exibição do Info Center

Windows Media Player permite que os usuários abram e fechem o recurso Exibição do Centro de Informações. Exibição do Info Center é o recurso em que os usuários esperam encontrar informações estendidas e rich sobre conteúdo de mídia digital específico. Quando o usuário opta por abrir a Exibição do Info Center, Windows Media Player chamadas no armazenamento de música atual para exibir a página da Web exibição do Info Center especificada pelo atributo **URL** do elemento **InfoCenter** do documento ServiceInfo.

Para recuperar informações sobre o conteúdo de mídia digital em reprodução no momento, você deve inserir uma instância do controle Windows Media Player em sua página da Web e usar o modelo de objeto Player. Por exemplo, para recuperar o título, você pode usar o seguinte JScript código:


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a>Diretrizes para Exibição do Info Center

Ao criar sua **página da Web do Info Center View,** use as seguintes diretrizes:

-   A página deve identificar claramente a loja online que fornece as informações. Você pode fazer isso exibindo o logotipo em destaque, por exemplo.
-   A página deve incluir um link para a política de privacidade da sua empresa.
-   Evite a navegação de página dentro do recurso Exibição do Info Center sempre que possível. Você deve navegar até sua loja online para a maioria das atividades.
-   É melhor fornecer informações valiosas sem exigir que o usuário instale programas ou faça logoff em sua loja online.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**External.NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Elemento InfoCenter**](infocenter-element.md)
</dt> <dt>

[**Informações comuns às lojas online do tipo 1 e do tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Usando o controle Windows Media Player em uma página da Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




