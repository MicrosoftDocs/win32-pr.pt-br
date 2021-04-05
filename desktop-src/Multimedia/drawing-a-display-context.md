---
title: Desenhando um contexto de exibição
description: Desenhando um contexto de exibição
ms.assetid: c3328375-faa3-4b29-a155-8a25cc62269f
keywords:
- DrawDib, contexto do dispositivo (DC)
- DrawDib, DCs de desenho
- Função DrawDibRealize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1c79c2b7bb938cc34527b23cfc66fda6d19503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005486"
---
# <a name="drawing-a-display-context"></a>Desenhando um contexto de exibição

O exemplo a seguir prepara um DrawDib DC usando a função [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) antes de exibir várias imagens em uma sequência de bitmap.


```C++
hdc = GetDC(hwnd); 
DrawDibBegin(hdd, hdc, dxDest, dyDest, lpbi, dxSrc, dySrc, NULL); 
DrawDibRealize(hdd, hdc, fBackground); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
ReleaseDC(hwnd, hdc); 

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando DrawDib](using-drawdib.md)
</dt> </dl>

 

 




