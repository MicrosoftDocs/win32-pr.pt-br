---
description: Em geral, os aplicativos mais antigos não precisam de alterações para trabalhar em vários sistemas de monitor.
ms.assetid: 908cf88c-69ed-4855-817d-ba749e14ff85
title: Várias considerações de monitor para programas mais antigos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feebb356cb2f9c5480c84f1718b51d6e866ef621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967643"
---
# <a name="multiple-monitor-considerations-for-older-programs"></a><span data-ttu-id="e6355-103">Várias considerações de monitor para programas mais antigos</span><span class="sxs-lookup"><span data-stu-id="e6355-103">Multiple Monitor Considerations for Older Programs</span></span>

<span data-ttu-id="e6355-104">Em geral, os aplicativos mais antigos não precisam de alterações para trabalhar em vários sistemas de monitor.</span><span class="sxs-lookup"><span data-stu-id="e6355-104">Generally, older applications do not need changes to work on multiple monitor systems.</span></span> <span data-ttu-id="e6355-105">Para a maioria, o sistema parecerá ter apenas uma exibição.</span><span class="sxs-lookup"><span data-stu-id="e6355-105">For most, the system will appear to have only one display.</span></span> <span data-ttu-id="e6355-106">As métricas do sistema refletem a exibição principal e os aplicativos em tela inteira aparecem no primário.</span><span class="sxs-lookup"><span data-stu-id="e6355-106">System metrics reflect the primary display and fullscreen applications show up on the primary.</span></span> <span data-ttu-id="e6355-107">O sistema lida com a minimização, maximização, menus e caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e6355-107">The system handles minimization, maximization, menus, and dialog boxes.</span></span>

<span data-ttu-id="e6355-108">No entanto, alguns programas terão problemas.</span><span class="sxs-lookup"><span data-stu-id="e6355-108">However, some programs will have problems.</span></span> <span data-ttu-id="e6355-109">Alguns que podem ter problemas são aplicativos de controle remoto, aqueles que têm acesso direto ao hardware e aqueles que têm corrigido o GDI ou o driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e6355-109">Some that could have problems are remote control applications, those that have direct hardware access, and those that have patched the GDI or DISPLAY driver.</span></span> <span data-ttu-id="e6355-110">Nesses casos, o usuário pode ser solicitado a desabilitar qualquer monitor além do monitor primário.</span><span class="sxs-lookup"><span data-stu-id="e6355-110">In these cases, the user may be required to disable any monitor beyond the primary monitor.</span></span>

 

 



