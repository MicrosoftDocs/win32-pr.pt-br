---
description: A ação RegisterClassInfo gerencia o registro de informações de classe com com o sistema. Ele usa a tabela AppId.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: Ação RegisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd916772bc236dfc86df336347514c10d5dfbce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759208"
---
# <a name="registerclassinfo-action"></a><span data-ttu-id="49784-104">Ação RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="49784-104">RegisterClassInfo Action</span></span>

<span data-ttu-id="49784-105">A ação RegisterClassInfo gerencia o registro de informações de classe com com o sistema.</span><span class="sxs-lookup"><span data-stu-id="49784-105">The RegisterClassInfo action manages the registration of COM class information with the system.</span></span> <span data-ttu-id="49784-106">Ele usa a [tabela AppID](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="49784-106">It uses the [AppId table](appid-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="49784-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="49784-107">Sequence Restrictions</span></span>

<span data-ttu-id="49784-108">A ação RegisterClassInfo deve vir após a ação [InstallFiles](installfiles-action.md) e a ação [UnregisterClassInfo](unregisterclassinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="49784-108">The RegisterClassInfo action must come after the [InstallFiles](installfiles-action.md) action and the [UnregisterClassInfo](unregisterclassinfo-action.md) action.</span></span>

<span data-ttu-id="49784-109">O sequenciamento das ações no grupo a seguir é restrito.</span><span class="sxs-lookup"><span data-stu-id="49784-109">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="49784-110">Se qualquer subconjunto dessas ações ocorrer em conjunto em uma tabela de sequência, eles deverão ter a mesma ordem de sequência relativa mostrada:</span><span class="sxs-lookup"><span data-stu-id="49784-110">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="49784-111">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="49784-111">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="49784-112">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="49784-112">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="49784-113">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="49784-113">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="49784-114">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="49784-114">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   <span data-ttu-id="49784-115">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="49784-115">RegisterClassInfo</span></span>
-   [<span data-ttu-id="49784-116">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="49784-116">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="49784-117">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="49784-117">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="49784-118">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="49784-118">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="49784-119">Por exemplo, RegisterClassInfo deve vir após [UnregisterMIMEInfo](unregistermimeinfo-action.md) na tabela de sequência.</span><span class="sxs-lookup"><span data-stu-id="49784-119">For example, RegisterClassInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="49784-120">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="49784-120">ActionData Messages</span></span>



| <span data-ttu-id="49784-121">Campo</span><span class="sxs-lookup"><span data-stu-id="49784-121">Field</span></span> | <span data-ttu-id="49784-122">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="49784-122">Description of action data</span></span>                          |
|-------|-----------------------------------------------------|
| <span data-ttu-id="49784-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="49784-123">\[1\]</span></span> | <span data-ttu-id="49784-124">Identificador de classe de GUID do servidor COM registrado.</span><span class="sxs-lookup"><span data-stu-id="49784-124">GUID class identifier of the registered COM server.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="49784-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="49784-125">Remarks</span></span>

<span data-ttu-id="49784-126">Se o sistema oferecer suporte à instalação sob demanda para servidores OLE, o RegisterClassInfo registrará todas as classes COM na [tabela de classes](class-table.md) associada a um recurso selecionado a ser instalado ou anunciado.</span><span class="sxs-lookup"><span data-stu-id="49784-126">If the system supports install-on-demand for OLE servers, RegisterClassInfo registers all COM classes in the [Class table](class-table.md) associated with a feature selected to be installed or advertised.</span></span> <span data-ttu-id="49784-127">Caso contrário, essa ação registra apenas as classes COM associadas a um recurso selecionado para instalação.</span><span class="sxs-lookup"><span data-stu-id="49784-127">Otherwise this action only registers the COM classes associated with a feature selected for installation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49784-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="49784-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49784-129">**Propriedade OLEAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="49784-129">**OLEAdvtSupport property**</span></span>](oleadvtsupport.md)
</dt> </dl>

 

 



