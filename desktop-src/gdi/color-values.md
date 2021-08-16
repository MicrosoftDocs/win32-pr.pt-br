---
description: A cor é definida como uma combinação de três cores primárias vermelho, verde e azul.
ms.assetid: 6e44935c-2b3b-4062-8273-f1f3e70300d2
title: Valores de cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b1518060e1ad4af7ada1c244ecdcac742f27a36133080f31199714dd8059d5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761926"
---
# <a name="color-values"></a>Valores de cor

A cor é definida como uma combinação de três cores primárias vermelho, verde e azul. o sistema identifica uma cor, dando a ela um valor de cor (às vezes chamado de tripleto RGB), que consiste em três valores de 8 bits especificando as intensidades de seus componentes de cor. Preto tem a intensidade mínima para vermelho, verde e azul, portanto, o valor da cor para preto é (0, 0, 0). Branco tem a intensidade máxima para vermelho, verde e azul, portanto, seu valor de cor é (255, 255, 255).

> [!Note]  
> Se a correspondência de cores da imagem estiver habilitada, a definição de cor e o significado de um valor de cor dependerão do tipo de espaço de cor que está definido atualmente para o contexto do dispositivo.

 

O sistema e os aplicativos usam parâmetros e variáveis com o [tipo COLORREF](colorref.md) para passar e armazenar valores de cor. Por exemplo, a [**função EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) identifica a cor de cada caneta definindo o membro **lopnColor** em uma estrutura [**LOGPEN**](/windows/win32/api/wingdi/ns-wingdi-logpen) como um valor de cor. Os aplicativos podem extrair os valores individuais dos componentes vermelho, verde e azul de um valor de cor usando as macros [**GetRValue,**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue) [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)e [**GetBValue,**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) respectivamente. Os aplicativos podem criar um valor de cor de valores de componente individuais usando a macro [**RGB.**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) Ao criar ou examinar uma paleta lógica, um aplicativo usa a estrutura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) para definir valores de cor e examinar valores de componente individuais.

 

 



