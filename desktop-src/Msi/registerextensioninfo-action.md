---
description: A ação RegisterExtensionInfo gerencia o registro de informações relacionadas à extensão com o sistema.
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: Ação RegisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310344b6579ef65faac41238bb607ce98411b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750603"
---
# <a name="registerextensioninfo-action"></a><span data-ttu-id="169e5-103">Ação RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="169e5-103">RegisterExtensionInfo Action</span></span>

<span data-ttu-id="169e5-104">A ação RegisterExtensionInfo gerencia o registro de informações relacionadas à extensão com o sistema.</span><span class="sxs-lookup"><span data-stu-id="169e5-104">The RegisterExtensionInfo action manages the registration of extension related information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="169e5-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="169e5-105">Sequence Restrictions</span></span>

<span data-ttu-id="169e5-106">A ação RegisterExtensionInfo deve vir após a ação [InstallFiles](installfiles-action.md) e a ação [UnregisterExtensionInfo](unregisterextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="169e5-106">The RegisterExtensionInfo action must come after the [InstallFiles](installfiles-action.md) action and the [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action.</span></span>

<span data-ttu-id="169e5-107">O sequenciamento das ações no grupo a seguir é restrito.</span><span class="sxs-lookup"><span data-stu-id="169e5-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="169e5-108">Se qualquer subconjunto dessas ações ocorrer em conjunto em uma tabela de sequência, eles deverão ter a mesma ordem de sequência relativa mostrada:</span><span class="sxs-lookup"><span data-stu-id="169e5-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="169e5-109">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="169e5-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="169e5-110">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="169e5-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="169e5-111">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="169e5-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="169e5-112">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="169e5-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="169e5-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="169e5-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   <span data-ttu-id="169e5-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="169e5-114">RegisterExtensionInfo</span></span>
-   [<span data-ttu-id="169e5-115">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="169e5-115">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="169e5-116">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="169e5-116">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="169e5-117">Por exemplo, RegisterExtensionInfo deve vir após [UnregisterMIMEInfo](unregistermimeinfo-action.md) na tabela de sequência.</span><span class="sxs-lookup"><span data-stu-id="169e5-117">For example, RegisterExtensionInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="169e5-118">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="169e5-118">ActionData Messages</span></span>



| <span data-ttu-id="169e5-119">Campo</span><span class="sxs-lookup"><span data-stu-id="169e5-119">Field</span></span> | <span data-ttu-id="169e5-120">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="169e5-120">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="169e5-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="169e5-121">\[1\]</span></span> | <span data-ttu-id="169e5-122">Extensão registrada.</span><span class="sxs-lookup"><span data-stu-id="169e5-122">Registered extension.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="169e5-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="169e5-123">Remarks</span></span>

<span data-ttu-id="169e5-124">Se o sistema oferecer suporte à instalação sob demanda para servidores de extensão, o RegisterExtensionInfo registrará todos os servidores de extensão na [tabela de extensão](extension-table.md) associada aos recursos definidos para instalação ou anúncio.</span><span class="sxs-lookup"><span data-stu-id="169e5-124">If the system supports installation-on-demand for extension servers, RegisterExtensionInfo registers all extension servers in the [Extension table](extension-table.md) associated with features set for installation or advertisement.</span></span> <span data-ttu-id="169e5-125">Caso contrário, essa ação registra somente os servidores de extensão associados aos recursos definidos como instalação.</span><span class="sxs-lookup"><span data-stu-id="169e5-125">Otherwise this action only registers extension servers associated with features set to installation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="169e5-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="169e5-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="169e5-127">**Propriedade ShellAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="169e5-127">**ShellAdvtSupport property**</span></span>](shelladvtsupport.md)
</dt> </dl>

 

 



