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
ms.openlocfilehash: e023ba8ee2c4791ebc8c3f2ac7ebf9a198f4a5ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640956"
---
# <a name="animating-a-palette"></a><span data-ttu-id="0f1f8-107">Animando uma paleta</span><span class="sxs-lookup"><span data-stu-id="0f1f8-107">Animating a Palette</span></span>

<span data-ttu-id="0f1f8-108">O exemplo a seguir anima uma paleta usando as funções [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)e [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .</span><span class="sxs-lookup"><span data-stu-id="0f1f8-108">The following example animates a palette by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette), and [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) functions.</span></span>

<span data-ttu-id="0f1f8-109">Você pode alterar as cores de um bitmap usando a função [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) em combinação com [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette).</span><span class="sxs-lookup"><span data-stu-id="0f1f8-109">You can change the colors of a bitmap by using the [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) function in combination with [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette).</span></span> <span data-ttu-id="0f1f8-110">Primeiro, para permitir alterações na paleta, especifique o \_ sinalizador de animação do DDF na chamada para **DrawDibBegin**.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-110">First, to allow palette changes, specify the DDF\_ANIMATE flag in the call to **DrawDibBegin**.</span></span> <span data-ttu-id="0f1f8-111">Em segundo lugar, defina os valores da tabela de cores nas entradas da paleta usando **DrawDibChangePalette**.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-111">Second, set the color table values from the palette entries by using **DrawDibChangePalette**.</span></span>

<span data-ttu-id="0f1f8-112">Por exemplo, se *lppe* for um endereço da matriz [PaletteEntry](/previous-versions//ms532623(v=vs.85)) que contém as novas cores e *lpbi* for a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) usada em [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) ou [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), o fragmento a seguir atualizará a tabela de cores DIB.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-112">For example, if *lppe* is an address of the [PALETTEENTRY](/previous-versions//ms532623(v=vs.85)) array containing the new colors, and *lpbi* is the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure used in [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) or [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), the following fragment updates the DIB color table.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0f1f8-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f1f8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f1f8-114">Usando DrawDib</span><span class="sxs-lookup"><span data-stu-id="0f1f8-114">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 