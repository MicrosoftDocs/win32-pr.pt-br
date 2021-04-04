---
description: Configuração
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Configuração (Windows e mensagens)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac66d2ba25e81582734eb13148d2651b276ea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171310"
---
# <a name="configuration-windows-and-messages"></a>Configuração (Windows e mensagens)

Os *elementos de exibição* são as partes de uma janela e a exibição que aparecem na tela de exibição do sistema. As *métricas do sistema* são as dimensões de vários elementos de exibição. As métricas de sistema típicas incluem a largura da borda da janela, a altura do ícone e assim por diante. As métricas do sistema também descrevem outros aspectos do sistema, como se um mouse está instalado, se há suporte para caracteres de dois bytes ou se uma versão de depuração do sistema operacional está instalada. A função [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) recupera a métrica do sistema especificada.

Os aplicativos também podem recuperar e definir a cor dos elementos da janela, como menus, barras de rolagem e botões usando as funções [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) e [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) , respectivamente.

A função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) recupera ou define vários atributos do sistema, como tempo de clique duplo, tempo limite de proteção de tela, largura da borda da janela e padrão da área de trabalho. Quando um aplicativo usa **SystemParametersInfo** para definir um parâmetro, a alteração ocorre imediatamente. Essa função também permite que os aplicativos atualizem o perfil do usuário, portanto, as alterações no sistema serão preservadas quando o sistema for reiniciado.

 

 
