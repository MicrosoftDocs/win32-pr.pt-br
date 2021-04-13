---
title: Parâmetro de preferência de teclado
description: O parâmetro de preferência de teclado indica que o usuário depende do teclado, em vez do mouse, de modo que os aplicativos devem exibir as interfaces de teclado que, de outra forma, seriam ocultas.
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802d4ff76efae985cc07b6fe42f9d6b53cdf0b53
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366260"
---
# <a name="keyboard-preference-parameter"></a><span data-ttu-id="2d311-103">Parâmetro de preferência de teclado</span><span class="sxs-lookup"><span data-stu-id="2d311-103">Keyboard preference parameter</span></span>

<span data-ttu-id="2d311-104">O parâmetro de preferência de teclado indica que o usuário depende do teclado, em vez do mouse, de modo que os aplicativos devem exibir as interfaces de teclado que, de outra forma, seriam ocultas.</span><span class="sxs-lookup"><span data-stu-id="2d311-104">The keyboard preference parameter indicates that the user relies on the keyboard instead of the mouse, so applications should display keyboard interfaces that would otherwise be hidden.</span></span>

<span data-ttu-id="2d311-105">O usuário controla a configuração do parâmetro de preferência de teclado usando a central de facilidade de acesso no painel de controle ou outro aplicativo para personalizar o ambiente.</span><span class="sxs-lookup"><span data-stu-id="2d311-105">The user controls the setting of the keyboard preference parameter by using the Ease of Access Center in Control Panel, or another application for customizing the environment.</span></span> <span data-ttu-id="2d311-106">Os aplicativos usam os sinalizadores **SPI \_ GETKEYBOARDPREF** e **SPI \_ SETKEYBOARDPREF** com a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obter e definir o parâmetro de preferência de teclado.</span><span class="sxs-lookup"><span data-stu-id="2d311-106">Applications use the **SPI\_GETKEYBOARDPREF** and **SPI\_SETKEYBOARDPREF** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the keyboard preference parameter.</span></span>

<span data-ttu-id="2d311-107">Além disso, no Windows 2000, os usuários podem definir um parâmetro que indica se as teclas de acesso do menu sempre serão sublinhadas.</span><span class="sxs-lookup"><span data-stu-id="2d311-107">Additionally, on Windows 2000, users can set a parameter that indicates whether menu access keys are always underlined.</span></span> <span data-ttu-id="2d311-108">Os aplicativos usam os sinalizadores **SPI \_ GETMENUUNDERLINES** e **SPI \_ SETMENUUNDERLINES** com a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obter e definir o parâmetro sublinhado do menu.</span><span class="sxs-lookup"><span data-stu-id="2d311-108">Applications use the **SPI\_GETMENUUNDERLINES** and **SPI\_SETMENUUNDERLINES** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the menu underlines parameter.</span></span>

<span data-ttu-id="2d311-109">Quando um aplicativo recebe uma mensagem de [**\_ SETTINGCHANGE do WM**](/windows/desktop/winmsg/wm-settingchange) para o parâmetro de sublinhado de menu ou de preferência de teclado, é recomendável que o aplicativo chame [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para atualizar as informações para ambos os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2d311-109">When an application receives a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message for either the keyboard preference or menu underline parameter, it is recommended that the application call [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) to update the information for both parameters.</span></span>

<span data-ttu-id="2d311-110">Observe que **o \_ SPI GETMENUUNDERLINES** é o mesmo que **SPI \_ GETKEYBOARDCUES**, e **SPI \_ SETMENUUNDERLINES** é o mesmo que **SPI \_ SETKEYBOARDCUES**.</span><span class="sxs-lookup"><span data-stu-id="2d311-110">Note that **SPI\_GETMENUUNDERLINES** is the same as **SPI\_GETKEYBOARDCUES**, and **SPI\_SETMENUUNDERLINES** is the same as **SPI\_SETKEYBOARDCUES**.</span></span>

 

 