---
description: As técnicas fornecem o capacidade de renderização. Uma técnica encapsula o estado de efeito que determina um estilo de renderização. Uma técnica é composta de uma ou mais passagens.
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: Técnicas e passagens (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3a68ac40db16b3e6819adf6fcd1f8a6f790325
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105760111"
---
# <a name="techniques-and-passes-direct3d-9"></a>Técnicas e passagens (Direct3D 9)

As técnicas fornecem o capacidade de renderização. Uma técnica encapsula o estado de efeito que determina um estilo de renderização. Uma técnica é composta de uma ou mais passagens.

## <a name="techniques"></a>Técnicas

A sintaxe para chamar uma técnica é a seguinte:


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



Em que:

-   ID é um nome exclusivo opcional.
-   a anotação é zero ou mais partes opcionais de informações específicas do usuário. Consulte [adicionar informações para parâmetros de efeito com \_ anotações](using-an-effect.md).
-   as Pass (es) são zero ou mais passagens. Cada passagem contém atribuições de estado. Veja abaixo.

## <a name="passes"></a>Passa

Uma passagem contém as atribuições de estado necessárias para renderizar.


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



Em que:

-   ID é um nome exclusivo opcional.
-   a anotação é uma ou mais informações adicionais específicas do usuário. Consulte [adicionar informações para parâmetros de efeito com \_ anotações](using-an-effect.md).
-   a atribuição (ões) atribui zero ou mais valores de estado ou avalia uma ou mais expressões. Consulte [Estados de efeito (Direct3D 9)](effect-states.md) e [expressões (Direct3D 9)](expressions.md).

Passa ignorar tudo, exceto a última atribuição em um conjunto de atribuições repetidas para o mesmo estado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato do efeito](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



