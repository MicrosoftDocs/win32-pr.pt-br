---
title: Seção bitmaps
description: Seção bitmaps
ms.assetid: db2801e5-c55a-4681-9fe9-6027f28653e0
keywords:
- Windows Media Player Capas móveis, bitmaps
- capas, bitmaps
- Criando capas, seção bitmaps
- escrevendo código para capas, seção bitmaps
- bitmaps em capas, seção bitmaps
- arquivos de definição de capa, seção bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3062a8679e916fc8eaa733ab82c3df51845969873fcf83534be5f9ec6e4c6f14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573456"
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
> a região e Super bitmaps são preteridos em capas Windows Media Player 10 Mobile ou posteriores.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Escrevendo o código**](writing-the-code.md)
</dt> </dl>

 

 




