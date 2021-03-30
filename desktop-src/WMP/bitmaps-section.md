---
title: Seção bitmaps
description: Seção bitmaps
ms.assetid: db2801e5-c55a-4681-9fe9-6027f28653e0
keywords:
- Capas do Windows Media Player Mobile, bitmaps
- capas, bitmaps
- Criando capas, seção bitmaps
- escrevendo código para capas, seção bitmaps
- bitmaps em capas, seção bitmaps
- arquivos de definição de capa, seção bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4a5e41e8e2b095b199a072e31abde3c1cbaa29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005435"
---
# <a name="bitmaps-section"></a>Seção bitmaps

Em seguida, você deve ter uma seção que define cada um dos seus arquivos de bitmap. Cada tipo de bitmap que você usará deve ter um arquivo atribuído a ele, embora você possa ter mais de um tipo usando o mesmo bitmap.


```C++
[ Bitmaps ]

//  <Name>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



A seção bitmaps deve começar com os bitmaps do Word entre colchetes e, em seguida, uma linha para cada tipo de bitmap que você deseja definir. Neste exemplo, cinco tipos de bitmaps foram definidos. Para obter mais informações sobre a seção bitmaps, consulte [bitmaps](bitmaps.md) na referência de capa.

> [!Note]  
> A região e super bitmaps são preteridos nas capas do Windows Media Player 10 Mobile ou posteriores.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Escrevendo o código**](writing-the-code.md)
</dt> </dl>

 

 




