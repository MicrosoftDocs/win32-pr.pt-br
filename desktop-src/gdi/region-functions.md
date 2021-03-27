---
description: As funções a seguir são usadas com regiões.
ms.assetid: 3a42fc7a-4c07-4540-99a7-520f99532f33
title: Funções de região (GDI do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0f55549f978dd2868f231b9ff042f6f825459d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967599"
---
# <a name="region-functions-windows-gdi"></a>Funções de região (GDI do Windows)

As funções a seguir são usadas com regiões.



| Função                                                       | Descrição                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn)                               | Combina duas regiões e armazena o resultado em uma terceira região.                                |
| [**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn)                 | Cria uma região elíptica.                                                                |
| [**CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect) | Cria uma região elíptica.                                                                |
| [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn)                   | Cria uma região poligonal.                                                                  |
| [**CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)           | Cria uma região que consiste em uma série de polígonos.                                         |
| [**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn)                         | Cria uma região retangular.                                                                |
| [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect)         | Cria uma região retangular.                                                                |
| [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)               | Cria uma região retangular com cantos arredondados.                                           |
| [**EqualRgn**](/windows/desktop/api/Wingdi/nf-wingdi-equalrgn)                                   | Verifica as duas regiões especificadas para determinar se elas são idênticas.                    |
| [**ExtCreateRegion**](/windows/desktop/api/Wingdi/nf-wingdi-extcreateregion)                     | Cria uma região a partir da região especificada e dos dados de transformação.                          |
| [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn)                                     | Preenche uma região usando o pincel especificado.                                                 |
| [**FrameRgn**](/windows/desktop/api/Wingdi/nf-wingdi-framergn)                                   | Desenha uma borda em torno da região especificada usando o pincel especificado.                     |
| [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)                     | Recupera o modo de preenchimento do polígono atual.                                                     |
| [**GetRegionData**](/windows/desktop/api/Wingdi/nf-wingdi-getregiondata)                         | Preenche o buffer especificado com dados que descrevem uma região.                                    |
| [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox)                                 | Recupera o retângulo delimitador da região especificada.                                    |
| [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn)                                 | Inverte as cores na região especificada.                                                  |
| [**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)                                 | Move uma região de acordo com os deslocamentos especificados.                                                     |
| [**PaintRgn**](/windows/desktop/api/Wingdi/nf-wingdi-paintrgn)                                   | Pinta a região especificada usando o pincel selecionado no momento no contexto do dispositivo.   |
| [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion)                               | Determina se o ponto especificado está dentro da região especificada.                       |
| [**RectInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-rectinregion)                           | Determina se qualquer parte do retângulo especificado está dentro dos limites de uma região. |
| [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)                     | Define o modo de preenchimento do polígono para funções que preenchem polígonos.                                 |
| [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)                               | Converte uma região em uma região retangular com as coordenadas especificadas.                  |



 

 

 



