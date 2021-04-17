---
description: 'Para anunciar um aplicativo em uma base de instalação por usuário quando o aplicativo requer privilégios elevados (ou seja, do sistema) para instalação, use as diretrizes na lista a seguir:'
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: Anunciando um aplicativo Per-User para ser instalado com privilégios elevados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d9888714f28282e060b3a1e7eea0291b4e0e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768488"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a><span data-ttu-id="42397-103">Anunciando um aplicativo Per-User para ser instalado com privilégios elevados</span><span class="sxs-lookup"><span data-stu-id="42397-103">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>

<span data-ttu-id="42397-104">Para anunciar um aplicativo em uma base de instalação por usuário quando o aplicativo requer privilégios elevados (ou seja, do sistema) para instalação, use as diretrizes na lista a seguir:</span><span class="sxs-lookup"><span data-stu-id="42397-104">To advertise an application on a per-user installation basis when the application requires elevated (that is, system) privileges for installation, use the guidelines in the following list:</span></span>

-   <span data-ttu-id="42397-105">Seu processo deve ser um serviço executado na conta do sistema LocalSystem no Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="42397-105">Your process must be a service that runs under the LocalSystem system account on Windows XP or later.</span></span>
-   <span data-ttu-id="42397-106">Gere um script de anúncio chamando [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) ou [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).</span><span class="sxs-lookup"><span data-stu-id="42397-106">Generate an advertise script by calling [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) or [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).</span></span>
-   <span data-ttu-id="42397-107">Seu processo deve representar o usuário que é o destino do anúncio.</span><span class="sxs-lookup"><span data-stu-id="42397-107">Your process must impersonate the user that is the target for the advertisement.</span></span>
-   <span data-ttu-id="42397-108">Chame [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)e use os sinalizadores SCRIPTFLAGS \_ CACHEINFO \| SCRIPTFLAGS \_ REGDATA \_ APPINFO \| \_ \_ \| \_ SCRIPTFLAGS REGDATA CNFGINFO SCRIPTFLAGS.</span><span class="sxs-lookup"><span data-stu-id="42397-108">Call [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta), and use the flags SCRIPTFLAGS\_CACHEINFO \| SCRIPTFLAGS\_REGDATA\_APPINFO \| SCRIPTFLAGS\_REGDATA\_CNFGINFO \| SCRIPTFLAGS\_SHORTCUTS.</span></span>

<span data-ttu-id="42397-109">Ao seguir as diretrizes, você anuncia um aplicativo para um usuário especificado e, quando o usuário opta por instalar, o aplicativo é instalado com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="42397-109">When you follow the guidelines, you advertise an application to a specified user, and when the user chooses to install, the application is installed with elevated privileges.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42397-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="42397-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42397-111">Aplicação de patch em aplicativos gerenciados por usuário</span><span class="sxs-lookup"><span data-stu-id="42397-111">Patching Per-User Managed Applications</span></span>](patching-per-user-managed-applications.md)
</dt> </dl>

 

 



