---
description: O sistema fornece seis fontes de estoque.
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: Usando uma fonte de estoque para desenhar texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a7e580175956185bcc26a7ebbae8d46dfff078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922498"
---
# <a name="using-a-stock-font-to-draw-text"></a>Usando uma fonte de estoque para desenhar texto

O sistema fornece seis fontes de estoque. Uma fonte de ações é uma fonte lógica que um aplicativo pode obter chamando a função [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) e especificando a fonte solicitada. A lista a seguir contém os valores que você pode especificar para obter uma fonte de estoque.



| Valor                 | Significado                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_fonte fixa \_ ANSI     | Especifica uma fonte monospace com base no conjunto de caracteres do Windows. Uma fonte Courier normalmente é usada.                                                                                                                                                                                                |
| \_fonte de var ANSI \_       | Especifica uma fonte proporcional com base no conjunto de caracteres do Windows. MS Sans Serif é normalmente usado.                                                                                                                                                                                              |
| \_fonte padrão do dispositivo \_ | Especifica a fonte preferencial para o dispositivo especificado. Normalmente, essa é a fonte do sistema para dispositivos de vídeo; no entanto, para algumas impressoras de matriz de pontos, essa é uma fonte residente no dispositivo. (A impressão com essa fonte geralmente é mais rápida do que a impressão com uma fonte de bitmap baixada).    |
| \_fonte fixa do OEM \_      | Especifica uma fonte monospace com base em um conjunto de caracteres OEM. Para computadores IBM e compatíveis, a fonte OEM é baseada no conjunto de caracteres do PC IBM.                                                                                                                                                 |
| fonte do sistema \_          | Especifica a fonte do sistema. Essa é uma fonte proporcional baseada no conjunto de caracteres do Windows e é usada pelo sistema operacional para exibir títulos de janela, nomes de menu e texto nas caixas de diálogo. A fonte do sistema está sempre disponível. Outras fontes estarão disponíveis somente se tiverem sido instaladas. |
| \_fonte fixa do sistema \_   | Especifica uma fonte monospace compatível com a fonte do sistema nas versões anteriores do Windows.                                                                                                                                                                                                        |



 

Para obter mais informações sobre fontes, consulte [about fonts](about-fonts.md).

O exemplo a seguir recupera um identificador para a fonte de ações da variável, seleciona-a em um contexto de dispositivo e, em seguida, grava uma cadeia de caracteres usando essa fonte:


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



Se outras fontes de estoque não estiverem disponíveis, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) retornará um identificador para a fonte do sistema (fonte do sistema \_ ). Você deve usar fontes de estoque somente se o modo de mapeamento para o contexto do dispositivo do seu aplicativo for um \_ texto mm.

 

 



