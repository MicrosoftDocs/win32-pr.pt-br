---
description: A ação RegisterMIMEInfo registra informações de registro relacionadas a MIME com o sistema.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: Ação RegisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41130d9e595cc2d95557470f79c217f3c3235d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662144"
---
# <a name="registermimeinfo-action"></a><span data-ttu-id="2de54-103">Ação RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="2de54-103">RegisterMIMEInfo Action</span></span>

<span data-ttu-id="2de54-104">A ação RegisterMIMEInfo registra informações de registro relacionadas a MIME com o sistema.</span><span class="sxs-lookup"><span data-stu-id="2de54-104">The RegisterMIMEInfo action registers MIME-related registry information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2de54-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="2de54-105">Sequence Restrictions</span></span>

<span data-ttu-id="2de54-106">A ação RegisterMIMEInfo deve vir após a ação [InstallFiles](installfiles-action.md) , a ação [UnregisterMIMEInfo](unregistermimeinfo-action.md) , a ação [RegisterClassInfo](registerclassinfo-action.md) e a ação [RegisterExtensionInfo](registerextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="2de54-106">The RegisterMIMEInfo action must come after the [InstallFiles](installfiles-action.md) action, [UnregisterMIMEInfo](unregistermimeinfo-action.md) action, [RegisterClassInfo](registerclassinfo-action.md) action, and the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="2de54-107">O sequenciamento das ações no grupo a seguir é restrito.</span><span class="sxs-lookup"><span data-stu-id="2de54-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="2de54-108">Se qualquer subconjunto dessas ações ocorrer em conjunto em uma tabela de sequência, eles deverão ter a mesma ordem de sequência relativa mostrada:</span><span class="sxs-lookup"><span data-stu-id="2de54-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="2de54-109">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="2de54-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="2de54-110">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="2de54-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="2de54-111">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="2de54-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="2de54-112">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="2de54-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="2de54-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="2de54-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="2de54-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="2de54-114">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="2de54-115">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="2de54-115">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   <span data-ttu-id="2de54-116">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="2de54-116">RegisterMIMEInfo</span></span>

<span data-ttu-id="2de54-117">Por exemplo, RegisterMIMEInfo deve vir após [UnregisterMIMEInfo](unregistermimeinfo-action.md) na tabela de sequência.</span><span class="sxs-lookup"><span data-stu-id="2de54-117">For example, RegisterMIMEInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2de54-118">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="2de54-118">ActionData Messages</span></span>



| <span data-ttu-id="2de54-119">Campo</span><span class="sxs-lookup"><span data-stu-id="2de54-119">Field</span></span> | <span data-ttu-id="2de54-120">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="2de54-120">Description of action data</span></span>                   |
|-------|----------------------------------------------|
| <span data-ttu-id="2de54-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2de54-121">\[1\]</span></span> | <span data-ttu-id="2de54-122">Identificador do tipo de conteúdo MIME registrado.</span><span class="sxs-lookup"><span data-stu-id="2de54-122">Identifier of registered MIME content type.</span></span>  |
| <span data-ttu-id="2de54-123">\[2\]</span><span class="sxs-lookup"><span data-stu-id="2de54-123">\[2\]</span></span> | <span data-ttu-id="2de54-124">Extensão associada ao tipo de conteúdo MIME.</span><span class="sxs-lookup"><span data-stu-id="2de54-124">Extension associated with MIME content type.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2de54-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="2de54-125">Remarks</span></span>

<span data-ttu-id="2de54-126">A ação RegisterMIMEInfo registra todas as informações de MIME para servidores da [tabela MIME](mime-table.md) para as quais o servidor de classe ou servidor de extensão correspondente foi selecionado para instalação.</span><span class="sxs-lookup"><span data-stu-id="2de54-126">The RegisterMIMEInfo action registers all MIME information for servers from the [MIME table](mime-table.md) for which the corresponding class server or extension server has been selected to be installed.</span></span>

 

 



