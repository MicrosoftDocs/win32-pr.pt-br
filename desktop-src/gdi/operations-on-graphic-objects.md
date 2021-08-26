---
description: Depois que um aplicativo cria um DC de exibição ou impressora, ele pode começar a desenhar no dispositivo associado ou, no caso do DC de memória, ele pode começar a desenhar no bitmap armazenado na memória.
ms.assetid: 73657a66-9415-4db0-a800-463c3d639240
title: Operações em objetos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ae7467e04f53196c839b6daa72482ab73845c3185208eb3cb886cb0ce6a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965616"
---
# <a name="operations-on-graphic-objects"></a>Operações em objetos gráficos

Depois que um aplicativo cria um DC de exibição ou impressora, ele pode começar a desenhar no dispositivo associado ou, no caso do DC de memória, ele pode começar a desenhar no bitmap armazenado na memória. No entanto, antes do início do desenho e, às vezes, enquanto o desenho está em andamento, geralmente é necessário substituir os objetos padrão por novos objetos.

Um aplicativo pode examinar os atributos de um objeto padrão chamando as funções [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) e [**GetObject.**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) A **função GetCurrentObject** retorna um identificador que identifica a caneta atual, pincel, paleta, bitmap ou fonte e a função **GetObject** inicializa uma estrutura que contém os atributos desse objeto.

Algumas impressoras fornecem canetas, pincéis e fontes residentes que podem ser usadas para melhorar a velocidade de desenho em um aplicativo. Duas funções podem ser usadas para enumerar esses objetos: [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) [**e EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa). Se o aplicativo precisa enumerar canetas ou pincéis residentes, ele pode chamar a função **EnumObjects** para examinar os atributos correspondentes. Se o aplicativo precisa enumerar fontes residentes, ele pode chamar a função **EnumFontFamilies** (que também pode enumerar fontes GDI).

Depois que um aplicativo determina que um objeto padrão precisa ser substituído, ele cria um novo objeto chamando uma das funções de criação a seguir.



| Objeto gráfico | Função                                                                                                                                                                                                                                                                                                                                                             |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bitmap         | [**CreateBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) [**CreateBitmapIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) [**CreateCompatibleBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) [**CreateDiscardableBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                                                                                                           |
| Pincel          | [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect), [**CreateDIBPatternBrush,**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush) [**CreateDIBPatternBrushPt,**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) [**CreateHatchBrush,**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush) [**CreatePatternBrush,**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)                                                 |
| Paleta de cores  | [**Createpalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette)                                                                                                                                                                                                                                                                                                                               |
| Fonte           | [**CreateFont,**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) [ **CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)                                                                                                                                                                                                                                                                                   |
| Caneta            | [**CreatePen,**](/windows/desktop/api/Wingdi/nf-wingdi-createpen) [**CreatePenIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect) [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen)                                                                                                                                                                                                                                                 |
| Região         | [**CreateEllipticRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn) [**CreateEllipticRgnIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect) [**CreatePolygonRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn) [**CreatePolyPolygonRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn) [**CreateRectRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn) [**CreateRectRgnIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect) [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn) |



 

Cada uma dessas funções retorna um identificador que identifica um novo objeto. Depois que um aplicativo recupera um identificador, ele deve chamar a [**função SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) para substituir o objeto padrão. No entanto, o aplicativo deve salvar o identificador que identifica o objeto padrão e usar esse identificador para substituir o novo objeto quando ele não for mais necessário. Quando o aplicativo terminar de desenhar com o novo objeto, ele deverá restaurar o objeto padrão chamando a função **SelectObject** e, em seguida, excluir o novo objeto chamando a [**função DeleteObject.**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) A falha na exclusão de objetos causa sérios problemas de desempenho.

 

 



