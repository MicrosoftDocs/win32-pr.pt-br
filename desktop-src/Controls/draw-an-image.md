---
title: Como desenhar uma imagem
description: Este tópico demonstra como usar a função ImageList \_ Draw para desenhar uma imagem.
ms.assetid: BE2F20F3-B7D3-4FA2-B1E9-60A47A609C36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7b42e97ad9b7cab8693431654dc31b473267414f31ae5811f4f66a6663ce8e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878326"
---
# <a name="how-to-draw-an-image"></a>Como desenhar uma imagem

Este tópico demonstra como usar a função [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) para desenhar uma imagem.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções


Para desenhar uma imagem, use a função [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) ou [**ImageList \_ DrawEx.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) Especifique o handle para uma lista de imagens, o índice da imagem a ser desenhada, o handle para o contexto do dispositivo de destino, um local dentro do contexto do dispositivo e um ou mais estilos de desenho.

A função definida pelo usuário no exemplo de código C++ a seguir usa a função [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) para desenhar uma imagem e salva as coordenadas do cliente do retângulo delimitado da imagem. Uma função subsequente usa o retângulo delimitado para determinar se o usuário clicou na imagem.



```C++
// DrawTheImage - draws an image transparently and saves 
// the bounding rectangle of the drawn image.
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which to draw the image. 
// himl - handle to the image list that contains the image. 
// cx and cy - client coordinates for the upper-left corner of the image. 
// 
// Global variables and constants 
//     g_nImage - index of the image to draw. 
//     g_rcImage - bounding rectangle of the image. 
//     CX_IMAGE and CY_IMAGE - width and height of the image. 
extern int g_nImage; 
extern RECT g_rcImage; 
 
#define CX_IMAGE 32 
#define CY_IMAGE 32 
 
BOOL DrawTheImage(HWND hwnd, HIMAGELIST himl, int cx, int cy) 
{ 
    HDC hdc; 
 
    if ((hdc = GetDC(hwnd)) == NULL) 
        return FALSE; 
    if (!ImageList_Draw(himl, g_nImage, hdc, cx, cy, ILD_TRANSPARENT)) 
        return FALSE; 
    ReleaseDC(hwnd, hdc); 
 
    SetRect(&g_rcImage, cx, cy, CX_IMAGE + cx, CY_IMAGE + cy); 
 
    return TRUE; 
} 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de listas de imagens](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[Sobre listas de imagens](image-lists.md)
</dt> <dt>

[Usando listas de imagens](using-image-lists.md)
</dt> </dl>

 

 




