---
description: As funções a seguir são usadas com pincéis.
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: funções de pincel (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c44f122592e1f13186253b349089706686d352460a364e405c404fd326f64989
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849286"
---
# <a name="brush-functions-windows-gdi"></a>funções de pincel (Windows GDI)

As funções a seguir são usadas com pincéis.



| Função                                                   | Descrição                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)         | Cria um pincel com um estilo, cor e padrão especificados |
| [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) | Cria um pincel com o padrão de um DIB                |
| [**CreateHatchBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)               | Cria um pincel com um padrão de hachura e cor             |
| [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)           | Cria um pincel com um padrão de bitmap                      |
| [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)               | Cria um pincel com uma cor sólida                         |
| [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)                     | Obtém a origem do pincel para um contexto de dispositivo                 |
| [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush)               | Obtém um identificador para um pincel que corresponde a um índice de cor |
| [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt)                                   | Pinta um retângulo                                         |
| [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex)                     | Define a origem do pincel para um contexto de dispositivo                 |
| [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Define a cor do pincel do contexto do dispositivo atual.               |



 

## <a name="obsolete-functions"></a>Funções obsoletas

As funções a seguir são fornecidas apenas para compatibilidade com versões de 16 bits do Windows.

[**CreateDIBPatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)

 

 



