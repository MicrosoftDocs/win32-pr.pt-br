---
title: Exemplo de seção de bitmap
description: Exemplo de seção de bitmap
ms.assetid: 51b84b34-3cbb-4863-b7dc-e33e80d6ba23
keywords:
- Windows Media Player Capas móveis, bitmaps
- capas, bitmaps
- referência para capas, bitmaps
- bitmaps em capas, seção bitmaps
- arquivos de definição de capa, seção bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de401906896abcdda4728ff0984871ef4a399d3e223b36afd9d585eb0e4fce76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833390"
---
# <a name="sample-bitmap-section"></a>Exemplo de seção de bitmap

As linhas a seguir mostram uma seção de bitmaps típico de um arquivo de definição de capa:


```C++
[ Bitmaps ]

//  <Type>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0
    

```



Isso define cinco bitmaps que são usados para criar uma imagem de plano de fundo, imagens para botões desabilitados e enviados por push, uma imagem de região para botões de região e uma superimagem para trackbars.

> [!Note]  
> a região e Super bitmaps são preteridos em capas para Windows Media Player 10 Mobile ou posterior.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Bitmaps**](bitmaps.md)
</dt> </dl>

 

 




