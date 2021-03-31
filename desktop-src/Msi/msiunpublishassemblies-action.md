---
description: A ação MsiUnpublishAssemblies gerencia o anúncio de assemblies de Common Language Runtime e assemblies do Win32 que estão sendo removidos.
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: Ação MsiUnpublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d398c66781e6e356b110828c56de6f5e616775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829564"
---
# <a name="msiunpublishassemblies-action"></a><span data-ttu-id="2dc52-103">Ação MsiUnpublishAssemblies</span><span class="sxs-lookup"><span data-stu-id="2dc52-103">MsiUnpublishAssemblies Action</span></span>

<span data-ttu-id="2dc52-104">A ação MsiUnpublishAssemblies gerencia o anúncio de assemblies de Common Language Runtime e assemblies do Win32 que estão sendo removidos.</span><span class="sxs-lookup"><span data-stu-id="2dc52-104">The MsiUnpublishAssemblies action manages the advertisement of common language runtime assemblies and Win32 assemblies that are being removed.</span></span> <span data-ttu-id="2dc52-105">A ação consulta a [tabela MsiAssembly](msiassembly-table.md) para determinar quais assemblies têm recursos anunciados ou instalados que estão sendo removidos do cache de assembly global e quais assemblies têm um componente pai anunciado ou instalado que está sendo removido de um local isolado para um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="2dc52-105">The action queries the [MsiAssembly table](msiassembly-table.md) to determine which assemblies have advertised or installed features being removed from the global assembly cache and which assemblies have an advertised or installed parent component being removed from a location isolated for a particular application.</span></span> <span data-ttu-id="2dc52-106">Para obter informações, consulte [instalação de assemblies no cache de assembly global](installation-of-assemblies-to-the-global-assembly-cache.md) e [instalação de assemblies do Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="2dc52-106">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="2dc52-107">Em sistemas que executam o Windows XP e versões posteriores, Windows Installer pode instalar assemblies do Win32 como [assemblies lado a lado](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="2dc52-107">On systems running Windows XP and later, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="2dc52-108">Para obter mais informações, consulte [sobre aplicativos isolados e assemblies lado a lado](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="2dc52-108">For more information, see [About Isolated Applications and Side-by-side Assemblies](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2dc52-109">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="2dc52-109">Sequence Restrictions</span></span>

<span data-ttu-id="2dc52-110">A ação MsiUnpublishAssemblies deve vir após a [ação InstallInitialize](installinitialize-action.md) na [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2dc52-110">The MsiUnpublishAssemblies action must come after the [InstallInitialize action](installinitialize-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2dc52-111">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="2dc52-111">ActionData Messages</span></span>



| <span data-ttu-id="2dc52-112">Campo</span><span class="sxs-lookup"><span data-stu-id="2dc52-112">Field</span></span> | <span data-ttu-id="2dc52-113">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="2dc52-113">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="2dc52-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2dc52-114">\[1\]</span></span> | <span data-ttu-id="2dc52-115">Contexto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2dc52-115">Application context.</span></span>       |
| <span data-ttu-id="2dc52-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="2dc52-116">\[2\]</span></span> | <span data-ttu-id="2dc52-117">Nome do assembly.</span><span class="sxs-lookup"><span data-stu-id="2dc52-117">Assembly name.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="2dc52-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="2dc52-118">Remarks</span></span>

<span data-ttu-id="2dc52-119">A [ação MsiPublishAssemblies](msipublishassemblies-action.md) gerencia o anúncio de assemblies sendo anunciados ou instalados.</span><span class="sxs-lookup"><span data-stu-id="2dc52-119">The [MsiPublishAssemblies Action](msipublishassemblies-action.md) manages the advertisement of assemblies being advertised or installed.</span></span>

 

 
