---
description: As funções a seguir são usadas com pincéis.
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: Funções de pincel (GDI do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2170ff5c4b743e19da669bd76b340ca95ac2ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502436"
---
# <a name="brush-functions-windows-gdi"></a>Funções de pincel (GDI do Windows)

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

 

 



