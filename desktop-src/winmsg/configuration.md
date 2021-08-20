---
description: Esta seção de referência descreve a configuração para Windows e Mensagens. Saiba mais sobre elementos de exibição e métricas do sistema.
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Configuração (Windows e Mensagens)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5c910fd9614d4d0e8fe9f6ba38d9dd59a0fd5649e836c3629427cde5d8617
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028464"
---
# <a name="configuration-windows-and-messages"></a>Configuração (Windows e Mensagens)

*Elementos de* exibição são as partes de uma janela e a exibição que aparecem na tela de exibição do sistema. *As métricas do* sistema são as dimensões de vários elementos de exibição. As métricas típicas do sistema incluem a largura da borda da janela, a altura do ícone e assim por diante. As métricas do sistema também descrevem outros aspectos do sistema, como se um mouse está instalado, se há suporte para caracteres de byte duplo ou se uma versão de depuração do sistema operacional está instalada. A [**função GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) recupera a métrica do sistema especificada.

Os aplicativos também podem recuperar e definir a cor dos elementos da janela, como menus, barras de rolagem e botões, usando as funções [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) e [**SetSysColors,**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) respectivamente.

A [**função SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) recupera ou define vários atributos do sistema, como tempo de clique duplo, tempo limite de economia de tela, largura da borda da janela e padrão de área de trabalho. Quando um aplicativo usa **SystemParametersInfo** para definir um parâmetro, a alteração ocorre imediatamente. Essa função também permite que os aplicativos atualizem o perfil do usuário, portanto, as alterações no sistema serão preservadas quando o sistema for reiniciado.

 

 
