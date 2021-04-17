---
description: O provedor de serviços de diretório faz o espelhamento de classes e instâncias de Active Directory no namespace LDAP (Lightweight Directory Access Protocol) do WMI.
ms.assetid: 0215b614-cb10-4195-837d-bf81d523c560
ms.tgt_platform: multiple
title: Mapeando Active Directory para o WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0162f722eb8a053270ac2a8e75eaed4f1cd405
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770315"
---
# <a name="mapping-active-directory-to-wmi"></a><span data-ttu-id="116b7-103">Mapeando Active Directory para o WMI</span><span class="sxs-lookup"><span data-stu-id="116b7-103">Mapping Active Directory to WMI</span></span>

<span data-ttu-id="116b7-104">O provedor de serviços de diretório faz o espelhamento de classes e instâncias de Active Directory no namespace LDAP (Lightweight Directory Access Protocol) do WMI.</span><span class="sxs-lookup"><span data-stu-id="116b7-104">The Directory Services Provider mirrors classes and instances from Active Directory into the WMI Lightweight Directory Access Protocol (LDAP) namespace.</span></span> <span data-ttu-id="116b7-105">Devido às diferenças fundamentais nos dois ambientes, você não pode simplesmente renomear as classes Active Directory e instâncias e esperar acessar corretamente essas classes e instâncias no WMI.</span><span class="sxs-lookup"><span data-stu-id="116b7-105">Because of fundamental differences in the two environments, you cannot simply rename the Active Directory classes and instances and hope to properly access those classes and instances in WMI.</span></span> <span data-ttu-id="116b7-106">Em vez disso, o provedor de serviços de diretório segue as regras de nomenclatura para preservar as relações existentes entre as classes de Active Directory e as instâncias.</span><span class="sxs-lookup"><span data-stu-id="116b7-106">Instead, the Directory Services provider follows naming rules to preserve the relationships that exist between the Active Directory classes and instances.</span></span>

<span data-ttu-id="116b7-107">Os tópicos a seguir fornecem informações sobre como mapear classes e instâncias de Active Directory:</span><span class="sxs-lookup"><span data-stu-id="116b7-107">The following topics provide information about mapping Active Directory classes and instances:</span></span>

-   [<span data-ttu-id="116b7-108">Mapeando classes de Active Directory</span><span class="sxs-lookup"><span data-stu-id="116b7-108">Mapping Active Directory Classes</span></span>](mapping-active-directory-classes.md)
-   [<span data-ttu-id="116b7-109">Mapeando instâncias de Active Directory</span><span class="sxs-lookup"><span data-stu-id="116b7-109">Mapping Active Directory Instances</span></span>](mapping-active-directory-instances.md)

> [!Note]  
> <span data-ttu-id="116b7-110">Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte [disponibilidade do sistema operacional de componentes WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="116b7-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



