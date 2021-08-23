---
description: As técnicas fornecem o capacidade de renderização. Uma técnica encapsula o estado de efeito que determina um estilo de renderização. Uma técnica é composta de uma ou mais passagens.
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: Técnicas e passagens (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9999927d96a914b80f870a2128b0eae12074616e4ae787b011551b6aab919220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044204"
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

 

 



