---
title: Eventos secundários
description: Eventos secundários
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Windows Media Player capas, eventos secundários
- skins, eventos secundários
- eventos, secundários
- escrevendo código para capas, eventos secundários
- eventos secundários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fd121330a99c73ed7a52def712bb53949113745a8af0f4c01ded8f9aeaea4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735776"
---
# <a name="secondary-events"></a>Eventos secundários

Você pode determinar quais outros eventos estão ocorrendo quando um evento específico é disparado. Por exemplo, quando um botão do mouse é clicado, talvez você queira saber se a tecla ALT estava ino mesmo.

## <a name="event-attributes"></a>Atributos de evento

Os seguintes atributos de evento têm suporte para capas:

-   **altKey**
-   **Botão**
-   **clientX**
-   **clientY**
-   **ctrlKey**
-   **Fromelement**
-   **Offsetx**
-   **Offsety**
-   **screenX**
-   **screenY**
-   **shiftKey**
-   **srcElement**
-   **toElement**
-   **x**
-   **y**
-   **Keycode**

Para obter mais informações sobre esses atributos, consulte a Referência [de programação de capa](skin-programming-reference.md).

## <a name="using-secondary-events"></a>Usando eventos secundários

Você só pode processar atributos de evento JScript código. Você deve usar a seguinte sintaxe:


```C++
event.eventattributename
```



*eventattributename* é o nome do atributo de evento. Por exemplo, para determinar se a tecla ALT foi pressionada durante um evento de clique, você pode usar as seguintes linhas em seu JScript código:


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

 

 




