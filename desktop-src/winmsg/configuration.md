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
# <a name="configuration-windows-and-messages"></a><span data-ttu-id="c5586-103">Configuração (Windows e mensagens)</span><span class="sxs-lookup"><span data-stu-id="c5586-103">Configuration (Windows and Messages)</span></span>

<span data-ttu-id="c5586-104">Os *elementos de exibição* são as partes de uma janela e a exibição que aparecem na tela de exibição do sistema.</span><span class="sxs-lookup"><span data-stu-id="c5586-104">*Display elements* are the parts of a window and the display that appear on the system display screen.</span></span> <span data-ttu-id="c5586-105">As *métricas do sistema* são as dimensões de vários elementos de exibição.</span><span class="sxs-lookup"><span data-stu-id="c5586-105">*System metrics* are the dimensions of various display elements.</span></span> <span data-ttu-id="c5586-106">As métricas de sistema típicas incluem a largura da borda da janela, a altura do ícone e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c5586-106">Typical system metrics include the window border width, icon height, and so on.</span></span> <span data-ttu-id="c5586-107">As métricas do sistema também descrevem outros aspectos do sistema, como se um mouse está instalado, se há suporte para caracteres de dois bytes ou se uma versão de depuração do sistema operacional está instalada.</span><span class="sxs-lookup"><span data-stu-id="c5586-107">System metrics also describe other aspects of the system, such as whether a mouse is installed, double-byte characters are supported, or a debugging version of the operating system is installed.</span></span> <span data-ttu-id="c5586-108">A função [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) recupera a métrica do sistema especificada.</span><span class="sxs-lookup"><span data-stu-id="c5586-108">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function retrieves the specified system metric.</span></span>

<span data-ttu-id="c5586-109">Os aplicativos também podem recuperar e definir a cor dos elementos da janela, como menus, barras de rolagem e botões usando as funções [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) e [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c5586-109">Applications can also retrieve and set the color of window elements such as menus, scroll bars, and buttons by using the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) and [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) functions, respectively.</span></span>

<span data-ttu-id="c5586-110">A função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) recupera ou define vários atributos do sistema, como tempo de clique duplo, tempo limite de proteção de tela, largura da borda da janela e padrão da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c5586-110">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function retrieves or sets various system attributes, such as double-click time, screen saver time-out, window border width, and desktop pattern.</span></span> <span data-ttu-id="c5586-111">Quando um aplicativo usa **SystemParametersInfo** para definir um parâmetro, a alteração ocorre imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c5586-111">When an application uses **SystemParametersInfo** to set a parameter, the change takes place immediately.</span></span> <span data-ttu-id="c5586-112">Essa função também permite que os aplicativos atualizem o perfil do usuário, portanto, as alterações no sistema serão preservadas quando o sistema for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="c5586-112">This function also enables applications to update the user profile, so changes to the system will be preserved when the system is restarted.</span></span>

 

 
