---
title: Parâmetro de alto contraste
description: O parâmetro de alto contraste indica se o usuário deseja um alto contraste entre as cores usadas para visuais em primeiro plano e em segundo plano.
ms.assetid: ec89c4ce-4e8b-4e1f-a349-fbd47431d675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1255e8a99b3cb253146e2fa2c019a879c4a1b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917437"
---
# <a name="high-contrast-parameter"></a>Parâmetro de alto contraste

O parâmetro de alto contraste indica se o usuário deseja um alto contraste entre as cores usadas para visuais em primeiro plano e em segundo plano.

O usuário controla a configuração do parâmetro de alto contraste usando a central de facilidade de acesso no painel de controle ou outro aplicativo para personalizar o ambiente. Os aplicativos usam os sinalizadores **SPI \_ GETHIGHCONTRAST** e **SPI \_ SETHIGHCONTRAST** com a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obter e definir o parâmetro de alto contraste.

Durante a inicialização e ao processar mensagens [**\_ SYSCOLORCHANGE do WM**](/windows/desktop/gdi/wm-syscolorchange) , os aplicativos devem determinar o estado do parâmetro de alto contraste. Para fazer essa determinação, os aplicativos devem chamar [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) com o sinalizador **SPI \_ GETHIGHCONTRAST** para obter uma estrutura [**HighContrast**](/windows/win32/api/winuser/ns-winuser-highcontrasta) . Se o membro **dwFlags** da estrutura **HighContrast** tiver o conjunto de bits de **HCF \_ HIGHCONTRASTON** , o recurso de alto contraste será habilitado e os aplicativos deverão fazer o seguinte:

-   Mapeie todas as cores para um único par de cores de primeiro plano e de segundo plano. Use a função [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) para determinar as cores de primeiro plano e plano de fundo apropriadas, usando uma combinação de **\_ WINDOWTEXT de cor** e **\_ janela de cor** ou uma combinação de **\_ BtnText** de cor e **\_ btnface de cor**. A função **GetSysColor** retorna as cores selecionadas pelo usuário por meio do painel de controle.
-   Omita todas as imagens de bitmap que normalmente seriam exibidas atrás do texto. Essas imagens são visualmente distraindo um usuário que precisa de alto contraste.
-   As imagens que normalmente seriam desenhadas em várias cores devem ser desenhadas usando as cores de primeiro e segundo plano selecionadas para texto.

Além disso, os aplicativos usam os sinalizadores **SPI \_ GETDISABLEOVERLAPPEDCONTENT** e **SPI \_ SETDISABLEOVERLAPPEDCONTENT** com a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obter e definir o parâmetro de conteúdo sobreposto. Os recursos de exibição, como imagens de plano de fundo, planos de fundo texturizados, marcas d' água em documentos, mesclagem alfa e transparência, podem reduzir o contraste entre o primeiro plano e o plano de fundo, tornando mais difícil para os usuários com pouca visão ver objetos na tela. Esse sinalizador permite que os aplicativos determinem se esse conteúdo sobreposto foi desabilitado

 

 