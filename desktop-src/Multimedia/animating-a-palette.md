---
title: Animando uma paleta
description: Animando uma paleta
ms.assetid: 89493cc3-eca9-407f-99c2-903fba16992c
keywords:
- DrawDib, paletas
- Função DrawDibRealize
- Função DrawDibDraw
- Função DrawDibChangePalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be9613e4e648fad0b1fafe5d48d091ab13c9b6c358eda4a858c1d5517ab8fc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808416"
---
# <a name="animating-a-palette"></a>Animando uma paleta

O exemplo a seguir anima uma paleta usando as funções [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)e [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .

Você pode alterar as cores de um bitmap usando a função [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) em combinação com [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette). Primeiro, para permitir alterações na paleta, especifique o \_ sinalizador de animação do DDF na chamada para **DrawDibBegin**. Em segundo lugar, defina os valores da tabela de cores nas entradas da paleta usando **DrawDibChangePalette**.

Por exemplo, se *lppe* for um endereço da matriz [PaletteEntry](/previous-versions//ms532623(v=vs.85)) que contém as novas cores e *lpbi* for a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) usada em [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) ou [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), o fragmento a seguir atualizará a tabela de cores DIB.


```C++
hdc = GetDC(hwnd); 
DrawDibBegin(hdd, ....., DDF_ANIMATE); 
DrawDibRealize(hdd, hdc, fBackground); 
DrawDibDraw(hdd, hdc, ...., DDF_SAME_DRAW|DDF_SAME_HDC); 
 
// Call to change color. 
DrawDibChangePalette(hDD, iStart, iLen, lppe); 
. 
. 
. 
ReleaseDC(hwnd, hdc); 

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando DrawDib](using-drawdib.md)
</dt> </dl>

 

 