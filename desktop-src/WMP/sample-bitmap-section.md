---
title: Exemplo de seção de bitmap
description: Exemplo de seção de bitmap
ms.assetid: 51b84b34-3cbb-4863-b7dc-e33e80d6ba23
keywords:
- Capas do Windows Media Player Mobile, bitmaps
- capas, bitmaps
- referência para capas, bitmaps
- bitmaps em capas, seção bitmaps
- arquivos de definição de capa, seção bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b05183be7ba56ed5b00a6bfd26ee6162e008cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822844"
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
> A região e super bitmaps são preteridos em capas para Windows Media Player 10 Mobile ou posterior.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Bitmaps**](bitmaps.md)
</dt> </dl>

 

 




