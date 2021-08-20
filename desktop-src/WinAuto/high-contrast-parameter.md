---
title: Parâmetro de alto contraste
description: O parâmetro de alto contraste indica se o usuário deseja um alto contraste entre as cores usadas para visuais de primeiro plano e plano de fundo.
ms.assetid: ec89c4ce-4e8b-4e1f-a349-fbd47431d675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c268acbf95981e70e8e0d36843cfd9abfe9c1b459e1193dc2176032dec5a1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929637"
---
# <a name="high-contrast-parameter"></a>Parâmetro de alto contraste

O parâmetro de alto contraste indica se o usuário deseja um alto contraste entre as cores usadas para visuais de primeiro plano e plano de fundo.

O usuário controla a configuração do parâmetro de alto contraste usando o Central de Facilidade de Acesso no Painel de Controle ou outro aplicativo para personalizar o ambiente. Os aplicativos usam os sinalizadores **\_ SPI GETHIGHCONTRAST** e **SPI \_ SPIIGHCONTRAST** com a [**função SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obter e definir o parâmetro de alto contraste.

Durante a inicialização e ao processar [**mensagens WM \_ SYSCOLORCHANGE,**](/windows/desktop/gdi/wm-syscolorchange) os aplicativos devem determinar o estado do parâmetro de alto contraste. Para fazer essa determinação, os aplicativos devem chamar [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) com o **sinalizador SPI \_ GETHIGHCONTRAST** para obter uma [**estrutura HIGHCONTRAST.**](/windows/win32/api/winuser/ns-winuser-highcontrasta) Se o **membro dwFlags** da estrutura **HIGHCONTRAST** tiver o bit **HCF \_ HIGHCONTRA LTD** definido, o recurso de alto contraste será habilitado e os aplicativos deverão fazer o seguinte:

-   Mapeie todas as cores para um único par de cores de primeiro plano e de plano de fundo. Use a [**função GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) para determinar as cores de primeiro plano e de plano de fundo apropriadas, usando uma combinação de **COLOR \_ WINDOWTEXT** e **COLOR WINDOW \_ ou** uma combinação de **COLOR \_ BTNTEXT** e **COLOR \_ BTNFACE.** A **função GetSysColor** retorna as cores selecionadas pelo usuário por meio do Painel de Controle.
-   Omita todas as imagens bit a bit que normalmente seriam exibidas atrás do texto. Essas imagens são visualmente distração para um usuário que precisa de alto contraste.
-   Imagens que normalmente seriam desenhadas em várias cores devem ser desenhadas usando as cores de primeiro plano e de plano de fundo selecionadas para o texto.

Além disso, os aplicativos usam os sinalizadores **SPI \_ GETDISABLEOVERLAPPEDCONTENT** e **SPI \_ SETDISABLEOVERLAPPEDCONTENT** com a [**função SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obter e definir o parâmetro de conteúdo sobreposto. Exibir recursos como imagens de tela de fundo, telas de fundo com textura, marcas d'água em documentos, mesclagem alfa e transparência podem reduzir o contraste entre o primeiro plano e a tela de fundo, dificultando que os usuários com visão baixa vejam objetos na tela. Esse sinalizador permite que os aplicativos determinem se esse conteúdo sobrecarrado foi desabilitado

 

 