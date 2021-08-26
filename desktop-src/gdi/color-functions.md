---
description: As funções a seguir são usadas com cor.
ms.assetid: 9dd32d4a-30bd-406f-a934-bb71ad4ca2cb
title: Funções de cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ef9e233e5376718ac983982fd3f06e9fcd6c6fc5843d4a32d685fe64bbc1af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966306"
---
# <a name="color-functions"></a>Funções de cor

As funções a seguir são usadas com cor.



| Função                                                   | Descrição                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette)                   | Substitui entradas na paleta lógica especificada.                                                                                                    |
| [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette)     | Cria uma paleta de meio-tom para o DC (contexto de dispositivo) especificado.                                                                                     |
| [**Createpalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette)                     | Cria uma paleta lógica.                                                                                                                            |
| [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment)           | Recupera os valores de ajuste de cor para o DC especificado.                                                                                           |
| [**GetNearestColor**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestcolor)                 | Recupera um valor de cor que identifica uma cor da paleta do sistema que será exibida quando o valor de cor especificado for usado.                    |
| [**GetNelettePaletteIndex**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestpaletteindex)   | Recupera o índice para a entrada na paleta lógica especificada mais próximo de um valor de cor especificado.                                     |
| [**GetPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getpaletteentries)             | Recupera um intervalo especificado de entradas de paleta da paleta lógica especificada.                                                                        |
| [**Getsystempaletteentries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) | Recupera um intervalo de entradas de paleta da paleta do sistema associada ao DC especificado.                                                |
| [**GetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteuse)         | Recupera o estado atual da paleta do sistema (físico) para o DC especificado.                                                                    |
| [**Realizepalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette)                   | Mapas de paleta da paleta lógica atual para a paleta do sistema.                                                                          |
| [**Resizepalette**](/windows/desktop/api/Wingdi/nf-wingdi-resizepalette)                     | Aumenta ou diminui o tamanho de uma paleta lógica com base no valor especificado.                                                                    |
| [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette)                     | Seleciona a paleta lógica especificada em um contexto de dispositivo.                                                                                          |
| [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment)           | Define os valores de ajuste de cor para um DC usando os valores especificados.                                                                                 |
| [**Setpaletteentries**](/windows/desktop/api/Wingdi/nf-wingdi-setpaletteentries)             | Define valores de cor RGB (vermelho, verde, azul) e sinalizadores em um intervalo de entradas em uma paleta lógica.                                                        |
| [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse)         | Permite que um aplicativo especifique se a paleta do sistema contém 2 ou 20 cores estáticas.                                                           |
| [**Unrealizeobject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject)                 | Redefine a origem de um pincel ou redefine uma paleta lógica.                                                                                             |
| [**Updatecolors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors)                       | Atualiza a área de cliente do contexto do dispositivo especificado remapeando as cores atuais na área do cliente para a paleta lógica atualmente realizada. |



 

 

 



