---
description: O sistema fornece seis fontes de estoque.
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: Usando uma fonte de estoque para desenhar texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9bd140a931a13f6232235036fb7b9cf3de1a20505666e869f214219b7a60a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468326"
---
# <a name="using-a-stock-font-to-draw-text"></a>Usando uma fonte de estoque para desenhar texto

O sistema fornece seis fontes de estoque. Uma fonte de estoque é uma fonte lógica que um aplicativo pode obter chamando a [função GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) e especificando a fonte solicitada. A lista a seguir contém os valores que você pode especificar para obter uma fonte de estoque.



| Valor                 | Significado                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FONTE FIXA \_ ANSI \_     | Especifica uma fonte monospace com base no conjunto Windows caracteres. Normalmente, uma fonte Courier é usada.                                                                                                                                                                                                |
| FONTE ANSI \_ VAR \_       | Especifica uma fonte proporcional com base no conjunto Windows caracteres. O MS Sans Serif normalmente é usado.                                                                                                                                                                                              |
| FONTE \_ PADRÃO DO \_ DISPOSITIVO | Especifica a fonte preferencial para o dispositivo especificado. Normalmente, essa é a fonte Do sistema para dispositivos de exibição; no entanto, para algumas impressoras de matriz de ponto, essa é uma fonte que é residente no dispositivo. (Imprimir com essa fonte geralmente é mais rápido do que imprimir com uma fonte de bitmap baixada).    |
| FONTE \_ FIXA OEM \_      | Especifica uma fonte de monospace com base em um conjunto de caracteres OEM. Para computadores IBM e compatíveis, a fonte OEM é baseada no conjunto de caracteres do COMPUTADOR IBM.                                                                                                                                                 |
| FONTE DO \_ SISTEMA          | Especifica a fonte System. Essa é uma fonte proporcional com base no conjunto Windows caracteres e é usada pelo sistema operacional para exibir títulos de janela, nomes de menu e texto nas caixas de diálogo. A fonte System está sempre disponível. Outras fontes só estarão disponíveis se elas foram instaladas. |
| FONTE \_ FIXA DO \_ SISTEMA   | Especifica uma fonte monospace compatível com a fonte System nas versões anteriores do Windows.                                                                                                                                                                                                        |



 

Para obter mais informações sobre fontes, consulte [Sobre fontes](about-fonts.md).

O exemplo a seguir recupera um alça para a fonte de estoque variável, seleciona-o em um contexto de dispositivo e, em seguida, grava uma cadeia de caracteres usando essa fonte:


```C++
HFONT hFont, hOldFont; 

// Retrieve a handle to the variable stock font.  
hFont = (HFONT)GetStockObject(ANSI_VAR_FONT); 

// Select the variable stock font into the specified device context. 
if (hOldFont = (HFONT)SelectObject(hdc, hFont)) 
{
    // Display the text string.  
    TextOut(hdc, 10, 50, L"Sample ANSI_VAR_FONT text", 25); 

    // Restore the original font.        
    SelectObject(hdc, hOldFont); 
}
```



Se outras fontes de estoque não estão disponíveis, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) retorna um handle para a fonte System (SYSTEM \_ FONT). Você deve usar fontes de estoque somente se o modo de mapeamento para o contexto do dispositivo do aplicativo for MM \_ TEXT.

 

 



