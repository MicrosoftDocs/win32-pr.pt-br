---
description: A ação MsiPublishAssemblies gerencia o anúncio de assemblies de Common Language Runtime e assemblies do Win32.
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: Ação MsiPublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24e1787aeb87cf00eb82aefab375771c7c1ddc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755077"
---
# <a name="msipublishassemblies-action"></a><span data-ttu-id="1594c-103">Ação MsiPublishAssemblies</span><span class="sxs-lookup"><span data-stu-id="1594c-103">MsiPublishAssemblies Action</span></span>

<span data-ttu-id="1594c-104">A ação MsiPublishAssemblies gerencia o anúncio de assemblies de Common Language Runtime e assemblies do Win32.</span><span class="sxs-lookup"><span data-stu-id="1594c-104">The MsiPublishAssemblies action manages the advertisement of common language runtime assemblies and Win32 assemblies.</span></span> <span data-ttu-id="1594c-105">A ação consulta a [tabela MsiAssembly](msiassembly-table.md) para determinar quais assemblies têm recursos sendo anunciados ou instalados no cache de assembly global e quais assemblies têm um componente pai sendo anunciado ou instalado em um local isolado para um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="1594c-105">The action queries the [MsiAssembly table](msiassembly-table.md) to determine which assemblies have features being advertised or installed to the global assembly cache and which assemblies have a parent component being advertised or installed to a location isolated for a particular application.</span></span> <span data-ttu-id="1594c-106">Para obter informações, consulte [instalação de assemblies no cache de assembly global](installation-of-assemblies-to-the-global-assembly-cache.md) e [instalação de assemblies do Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="1594c-106">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="1594c-107">No Microsoft Windows XP e em sistemas posteriores, Windows Installer pode instalar assemblies [do Win32 como assemblies lado a lado](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="1594c-107">On Microsoft Windows XP and later systems, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="1594c-108">Para obter mais informações, consulte [sobre aplicativos isolados e assemblies lado a lado](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="1594c-108">For more information, see [About Isolated Applications and Side-by-side Assemblies](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="1594c-109">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="1594c-109">Sequence Restrictions</span></span>

<span data-ttu-id="1594c-110">A ação MsiPublishAssemblies deve vir após a [ação InstallInitialize](installinitialize-action.md) na [tabela InstallExecuteSequence](installexecutesequence-table.md) ou na [tabela AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="1594c-110">The MsiPublishAssemblies action must come after the [InstallInitialize action](installinitialize-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md) or [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="1594c-111">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="1594c-111">ActionData Messages</span></span>



| <span data-ttu-id="1594c-112">Campo</span><span class="sxs-lookup"><span data-stu-id="1594c-112">Field</span></span> | <span data-ttu-id="1594c-113">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="1594c-113">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="1594c-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="1594c-114">\[1\]</span></span> | <span data-ttu-id="1594c-115">Contexto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1594c-115">Application context.</span></span>       |
| <span data-ttu-id="1594c-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="1594c-116">\[2\]</span></span> | <span data-ttu-id="1594c-117">Nome do assembly.</span><span class="sxs-lookup"><span data-stu-id="1594c-117">Assembly name.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="1594c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="1594c-118">Remarks</span></span>

<span data-ttu-id="1594c-119">Para obter mais informações, consulte [assemblies](assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="1594c-119">For more information, see [Assemblies](assemblies.md).</span></span>

<span data-ttu-id="1594c-120">A [ação MsiUnpublishAssemblies](msiunpublishassemblies-action.md) gerencia o anúncio de assemblies que estão sendo removidos.</span><span class="sxs-lookup"><span data-stu-id="1594c-120">The [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md) manages the advertisement of assemblies being removed.</span></span>

 

 
