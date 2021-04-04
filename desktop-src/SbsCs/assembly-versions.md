---
description: Cada assembly lado a lado deve ter uma versão.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Versões de assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c9e32ecc0990572f17264edd2ff51c205a01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662427"
---
# <a name="assembly-versions"></a><span data-ttu-id="9b634-103">Versões de assembly</span><span class="sxs-lookup"><span data-stu-id="9b634-103">Assembly Versions</span></span>

<span data-ttu-id="9b634-104">Cada assembly lado a lado deve ter uma versão.</span><span class="sxs-lookup"><span data-stu-id="9b634-104">Every side-by-side assembly must have a version.</span></span> <span data-ttu-id="9b634-105">Cada versão do assembly é associada a um número de versão com quatro partes separadas por pontos: *Major. Minor. Build. Revision*.</span><span class="sxs-lookup"><span data-stu-id="9b634-105">Each assembly version is associated with a version number having four parts separated by periods: *major.minor.build.revision*.</span></span> <span data-ttu-id="9b634-106">Se uma alteração for feita em um assembly, o que o torna incompatível com as versões existentes, as partes *principais* ou *secundárias* do número de versão devem ser alteradas.</span><span class="sxs-lookup"><span data-stu-id="9b634-106">If a change is made to an assembly making it incompatible with existing versions, the *major* or *minor* parts of the version number must be changed.</span></span> <span data-ttu-id="9b634-107">Um número de versão que é alterado somente nas partes de *compilação* ou *revisão* indica que o assembly é compatível com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="9b634-107">A version number that changes only in the *build* or *revision* parts indicates that the assembly is backward compatible with prior versions.</span></span>

<span data-ttu-id="9b634-108">A versão deve ser especificada em elementos **AssemblyIdentity** de [manifestos](manifests.md).</span><span class="sxs-lookup"><span data-stu-id="9b634-108">The version must be specified in **assemblyIdentity** elements of [manifests](manifests.md).</span></span> <span data-ttu-id="9b634-109">Use o formato de versão de quatro partes: mmmmm. NNNNN. Ooooo. ppppp.</span><span class="sxs-lookup"><span data-stu-id="9b634-109">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="9b634-110">Cada uma das partes separadas por períodos pode ser de 0-65535 inclusive.</span><span class="sxs-lookup"><span data-stu-id="9b634-110">Each of the parts separated by periods can be 0-65535 inclusive.</span></span>

 

 



