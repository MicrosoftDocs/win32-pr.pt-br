---
title: Eventos secundários
description: Eventos secundários
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Capas do Windows Media Player, eventos secundários
- capas, eventos secundários
- eventos, secundários
- escrevendo código para capas, eventos secundários
- eventos secundários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e04785a7468353665083287ac1b74bce5cbf0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453684"
---
# <a name="secondary-events"></a>Eventos secundários

Você pode determinar quais outros eventos estão ocorrendo quando um evento específico é disparado. Por exemplo, quando um botão do mouse é clicado, talvez você queira saber se a tecla ALT estava inativa ao mesmo tempo.

## <a name="event-attributes"></a>Atributos do evento

Os seguintes atributos de evento têm suporte para capas:

-   **altKey**
-   **Button**
-   **clientX**
-   **cliente**
-   **ctrlKey**
-   **deelement**
-   **offsetX**
-   **offsetY**
-   **screenX**
-   **tela**
-   **shiftKey**
-   **srcElement**
-   **elemento**
-   **x**
-   **y**
-   **KeyCode**

Para obter mais informações sobre esses atributos, consulte a [referência de programação de capa](skin-programming-reference.md).

## <a name="using-secondary-events"></a>Usando eventos secundários

Você só pode processar atributos de evento no código JScript. Você deve usar a seguinte sintaxe:


```C++
event.eventattributename
```



*eventattributename* é o nome do atributo de evento. Por exemplo, para determinar se a tecla ALT foi pressionada durante um evento de clique, você pode usar as seguintes linhas em seu código JScript:


```C++
wasAlt = event.altKey ;
if (wasAlt = true)
{
   // Do something here.
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Manipulando eventos**](handling-events.md)
</dt> </dl>

 

 




