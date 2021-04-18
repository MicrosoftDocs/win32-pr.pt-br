---
title: Eventos externos
description: Eventos externos
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Capas do Windows Media Player, eventos externos
- capas, eventos externos
- eventos, externos
- escrevendo código para capas, eventos externos
- eventos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa09a01b709f0da51d09fc2bec70cba0a1b07d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105810552"
---
# <a name="external-events"></a>Eventos externos

Quando os usuários clicam em um botão ou pressionam uma tecla, você pode responder à sua entrada com manipuladores de eventos. Um manipulador de eventos é uma seção de código que é executada sempre que o evento é disparado.

Os seguintes eventos são suportados pelos elementos de capa:

-   **carga**
-   **close**
-   **alonga**
-   **tempo**
-   **Selecione**
-   **DblClick**
-   **error**
-   **MouseDown**
-   **MouseUp**
-   **ocorra**
-   **acima**
-   **mouseout**
-   **pressionar**
-   **KeyDown**
-   **KeyUp**

Consulte a [referência de programação de capa](skin-programming-reference.md) para obter mais detalhes sobre eventos específicos.

Um manipulador de eventos externos típico deve nomear o evento e definir o código que será executado. Por exemplo, se você quiser criar código para iniciar o Windows Media Player quando o usuário clicar em um botão, você colocaria a linha a seguir em seu código de botão.


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



Isso irá reproduzir o arquivo chamado Laure. WMA. Observe que você adiciona a palavra "on" a eventos específicos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Manipulando eventos**](handling-events.md)
</dt> </dl>

 

 




