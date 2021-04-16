---
description: O Windows Installer é integrado à diretiva de restrição de software no Microsoft Windows XP.
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Windows Installer e política de restrição de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b080a1ed9a1396f4ac212e73d1fda6e2719bf40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757776"
---
# <a name="windows-installer-and-software-restriction-policy"></a><span data-ttu-id="eb37f-103">Windows Installer e política de restrição de software</span><span class="sxs-lookup"><span data-stu-id="eb37f-103">Windows Installer and Software Restriction Policy</span></span>

<span data-ttu-id="eb37f-104">O Windows Installer é integrado à diretiva de restrição de software no Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="eb37f-104">Windows Installer is integrated with Software Restriction Policy in Microsoft Windows XP.</span></span> <span data-ttu-id="eb37f-105">A diretiva de restrição de software é configurável por meio da diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="eb37f-105">Software Restriction Policy is configurable through group policy.</span></span> <span data-ttu-id="eb37f-106">A diretiva de restrição de software permite que um administrador restrinja administradores e não administradores de executar arquivos com base nos critérios de caminho, zona de URL, hash ou Publicador.</span><span class="sxs-lookup"><span data-stu-id="eb37f-106">Software Restriction Policy allows an administrator to restrict both administrators and nonadministrators from running files based upon the path, URL zone, hash, or publisher criteria.</span></span> <span data-ttu-id="eb37f-107">A política de restrição de software tem dois níveis: irrestrito e não permitido.</span><span class="sxs-lookup"><span data-stu-id="eb37f-107">Software Restriction Policy has two levels: unrestricted and disallowed.</span></span> <span data-ttu-id="eb37f-108">O Windows Installer instala apenas os pacotes com permissão para serem executados no nível irrestrito.</span><span class="sxs-lookup"><span data-stu-id="eb37f-108">The Windows Installer only installs packages allowed to run at the unrestricted level.</span></span>

<span data-ttu-id="eb37f-109">Patches ou transformações também devem ter permissão para serem executados no nível irrestrito.</span><span class="sxs-lookup"><span data-stu-id="eb37f-109">Patches or transforms must also be allowed to run at the unrestricted level.</span></span> <span data-ttu-id="eb37f-110">Se um pacote, patch ou transformação estiver configurado para ser executado em um nível diferente de irrestrito, o Windows Installer exibirá uma mensagem de erro e registrará uma entrada no log de eventos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eb37f-110">If a package, patch, or transform is configured to run at a level different from unrestricted, the Windows Installer displays an error message and logs an entry in the application event log.</span></span> <span data-ttu-id="eb37f-111">A diretiva de restrição de software é avaliada na primeira vez em que um aplicativo é instalado, quando um novo patch é aplicado e quando o pacote de instalação é armazenado em cache novamente.</span><span class="sxs-lookup"><span data-stu-id="eb37f-111">Software restriction policy is evaluated the first time an application is installed, when a new patch is applied, and when the installation package is re-cached.</span></span>

<span data-ttu-id="eb37f-112">Se um pacote, patch ou transformação for restrito, o Windows Installer exibirá uma mensagem de erro e gravará uma entrada de [log de eventos](event-logging.md) no log de eventos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eb37f-112">If a package, patch, or transform is restricted, the Windows Installer displays an error message and writes an [Event Logging](event-logging.md) entry in the application event log.</span></span> <span data-ttu-id="eb37f-113">A diretiva de restrição de software é avaliada na primeira vez em que um aplicativo é instalado, quando um novo patch é aplicado e quando o pacote de instalação é armazenado em cache novamente.</span><span class="sxs-lookup"><span data-stu-id="eb37f-113">Software restriction policy is evaluated the first time an application is installed, when a new patch is applied, and when the installation package is re-cached.</span></span>

<span data-ttu-id="eb37f-114">Para obter mais informações sobre a diretiva de restrição de software, consulte a documentação do produto e [pesquise no site do TechNet](https://www.microsoft.com/technet/sitemap.mspx).</span><span class="sxs-lookup"><span data-stu-id="eb37f-114">For more information on software restriction policy, consult the product documentation and [search the TechNet Site](https://www.microsoft.com/technet/sitemap.mspx).</span></span>

 

 



