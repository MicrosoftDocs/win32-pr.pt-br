---
description: Você pode instalar assemblies lado a lado como assemblies compartilhados ou como assemblies privados. Para obter mais informações, consulte Instalando assemblies lado a lado como assemblies privados e instalando assemblies lado a lado como assemblies compartilhados.
ms.assetid: 36f271ff-be0c-4162-8e1c-86088ebddbcc
title: Instalando assemblies lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be68580c7f0e3890c2e53b148daec92fbad18ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461039"
---
# <a name="installing-side-by-side-assemblies"></a><span data-ttu-id="c91ea-104">Instalando assemblies lado a lado</span><span class="sxs-lookup"><span data-stu-id="c91ea-104">Installing Side-by-side Assemblies</span></span>

<span data-ttu-id="c91ea-105">Você pode instalar assemblies lado a lado como [assemblies compartilhados](/windows/desktop/Msi/shared-assemblies) ou como [assemblies privados](/windows/desktop/Msi/private-assemblies).</span><span class="sxs-lookup"><span data-stu-id="c91ea-105">You may install side-by-side assemblies as [shared assemblies](/windows/desktop/Msi/shared-assemblies) or as [private assemblies](/windows/desktop/Msi/private-assemblies).</span></span> <span data-ttu-id="c91ea-106">Para obter mais informações, consulte [instalando assemblies lado a lado como assemblies privados](installing-side-by-side-assemblies-as-private-assemblies.md) e [instalando assemblies lado a lado como assemblies compartilhados](installing-side-by-side-assemblies-as-shared-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="c91ea-106">For more information, see [Installing Side-by-Side Assemblies as Private Assemblies](installing-side-by-side-assemblies-as-private-assemblies.md) and [Installing Side-by-side Assemblies as Shared Assemblies](installing-side-by-side-assemblies-as-shared-assemblies.md).</span></span>

<span data-ttu-id="c91ea-107">Observe que:</span><span class="sxs-lookup"><span data-stu-id="c91ea-107">Note that:</span></span>

-   <span data-ttu-id="c91ea-108">Os assemblies instalados no cache de assembly global por uma instalação usando o contexto de [instalação](/windows/desktop/Msi/installation-context) por usuário não são protegidos pela proteção de arquivo do Windows.</span><span class="sxs-lookup"><span data-stu-id="c91ea-108">Assemblies installed to the global assembly cache by an installation using the per-user [installation context](/windows/desktop/Msi/installation-context) are not protected by Windows File Protection.</span></span>
-   <span data-ttu-id="c91ea-109">Os assemblies que são instalados no cache de assembly global por uma instalação usando o contexto de [instalação](/windows/desktop/Msi/installation-context) por máquina são protegidos pela proteção de arquivo do Windows.</span><span class="sxs-lookup"><span data-stu-id="c91ea-109">Assemblies that are installed to the global assembly cache by an installation using the per-machine [installation context](/windows/desktop/Msi/installation-context) are protected by Windows File Protection.</span></span>

 

 
