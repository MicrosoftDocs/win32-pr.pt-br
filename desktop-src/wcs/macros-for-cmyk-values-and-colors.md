---
title: Macros para valores CMYK e cores
description: As macros a seguir são úteis na manipulação de valores CMYK.
ms.assetid: e5d107fb-e010-400b-9ec5-90c2c0381dbe
keywords:
- WCS (sistema de cores do Windows), macros CMYK
- WCS (sistema de cores do Windows), macros CMYK
- gerenciamento de cores de imagem, macros CMYK
- gerenciamento de cores, macros CMYK
- cores, macros CMYK
- Referência do WCS, macros CMYK
- referência para WCS, macros CMYK
- Macros CMYK
- preto-magenta amarelo ciano (CMYK)
- CMYK (ciano magenta amarelo preto)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0efcbb6b0dc25f8f93f420113cc8c0797cba46
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "105785996"
---
# <a name="macros-for-cmyk-values-and-colors"></a>Macros para valores CMYK e cores

As macros a seguir são úteis na manipulação de valores CMYK.



| Macro                          | Descrição                                                                  |
|--------------------------------|------------------------------------------------------------------------------|
| [**CMYK**](/windows/desktop/api/Wingdi/nf-wingdi-cmyk)           | Cria um valor CMYK de valores de ciano, magenta, amarelo e preto individuais. |
| [**GetCValue**](/windows/desktop/api/Wingdi/nf-wingdi-getcvalue) | Recupera o valor de cor ciano de um valor de cor CMYK.                      |
| [**GetKValue**](/windows/desktop/api/Wingdi/nf-wingdi-getkvalue) | Recupera o valor de cor preta de um valor de cor CMYK.                     |
| [**GetMValue**](/windows/desktop/api/Wingdi/nf-wingdi-getmvalue) | Recupera o valor magenta de um valor de cor CMYK.                         |
| [**GetYValue**](/windows/desktop/api/Wingdi/nf-wingdi-getyvalue) | Recupera o valor de cor amarela de um valor de cor CMYK.                    |



 

As macros a seguir são usadas com cores.



| Macro                                | Descrição                                                                                                                                           |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetBValue**](/windows/win32/api/wingdi/nf-wingdi-getbvalue)       | Obtém um valor azul RGB.                                                                                                                               |
| [**GetGValue**](/windows/win32/api/wingdi/nf-wingdi-getgvalue)       | Obtém um valor verde RGB.                                                                                                                              |
| [**GetRValue**](/windows/win32/api/wingdi/nf-wingdi-getrvalue)       | Obtém um valor vermelho RGB.                                                                                                                                |
| [**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85)) | Aceita um índice para uma entrada de paleta de cores lógicas e retorna um especificador de entrada de paleta.                                                              |
| [**PALETTERGB**](/windows/win32/api/wingdi/nf-wingdi-palettergb)     | Aceita três valores que representam as intensidades relativas de vermelho, verde e azul e retorna um especificador vermelho, verde, azul (RGB) relativo à paleta. |
| [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb)                       | Seleciona uma cor vermelha, verde, azul (RGB) com base nos argumentos fornecidos e nos recursos de cores do dispositivo de saída.                               |



 

 

 