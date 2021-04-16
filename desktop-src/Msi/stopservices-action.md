---
description: A ação StopServices interrompe os serviços do sistema. Esta ação consulta a tabela de UserControl.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Ação StopServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb271b99c434a1ac54ab9744697b991e9e1fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758760"
---
# <a name="stopservices-action"></a><span data-ttu-id="a1e8f-104">Ação StopServices</span><span class="sxs-lookup"><span data-stu-id="a1e8f-104">StopServices Action</span></span>

<span data-ttu-id="a1e8f-105">A ação StopServices interrompe os serviços do sistema.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-105">The StopServices action stops system services.</span></span> <span data-ttu-id="a1e8f-106">Esta ação consulta a [tabela de UserControl](servicecontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="a1e8f-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a1e8f-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="a1e8f-107">Sequence Restrictions</span></span>

<span data-ttu-id="a1e8f-108">As ações de serviços devem ser usadas na seguinte sequência:</span><span class="sxs-lookup"><span data-stu-id="a1e8f-108">The services actions must be used in the following sequence:</span></span>

-   <span data-ttu-id="a1e8f-109">Pararservices</span><span class="sxs-lookup"><span data-stu-id="a1e8f-109">StopServices</span></span>
-   [<span data-ttu-id="a1e8f-110">Excluirservices</span><span class="sxs-lookup"><span data-stu-id="a1e8f-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="a1e8f-111">Qualquer uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="a1e8f-111">Any of the following actions:</span></span>

-   [<span data-ttu-id="a1e8f-112">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="a1e8f-112">InstallFiles</span></span>](installfiles-action.md)
-   [<span data-ttu-id="a1e8f-113">Removes</span><span class="sxs-lookup"><span data-stu-id="a1e8f-113">RemoveFiles</span></span>](removefiles-action.md)
-   [<span data-ttu-id="a1e8f-114">DuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="a1e8f-114">DuplicateFiles</span></span>](duplicatefiles-action.md)
-   [<span data-ttu-id="a1e8f-115">MoveFile</span><span class="sxs-lookup"><span data-stu-id="a1e8f-115">MoveFiles</span></span>](movefiles-action.md)
-   [<span data-ttu-id="a1e8f-116">PatchFiles</span><span class="sxs-lookup"><span data-stu-id="a1e8f-116">PatchFiles</span></span>](patchfiles-action.md)
-   [<span data-ttu-id="a1e8f-117">RemoveDuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="a1e8f-117">RemoveDuplicateFiles</span></span>](removeduplicatefiles-action.md)
-   [<span data-ttu-id="a1e8f-118">Instalarservices</span><span class="sxs-lookup"><span data-stu-id="a1e8f-118">InstallServices</span></span>](installservices-action.md)
-   [<span data-ttu-id="a1e8f-119">Iniciarservices</span><span class="sxs-lookup"><span data-stu-id="a1e8f-119">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="a1e8f-120">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="a1e8f-120">ActionData Messages</span></span>



| <span data-ttu-id="a1e8f-121">Campo</span><span class="sxs-lookup"><span data-stu-id="a1e8f-121">Field</span></span> | <span data-ttu-id="a1e8f-122">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="a1e8f-122">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="a1e8f-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a1e8f-123">\[1\]</span></span> | <span data-ttu-id="a1e8f-124">Nome de exibição do serviço.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-124">Service display name.</span></span>      |
| <span data-ttu-id="a1e8f-125">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a1e8f-125">\[2\]</span></span> | <span data-ttu-id="a1e8f-126">Nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-126">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="a1e8f-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1e8f-127">Remarks</span></span>

<span data-ttu-id="a1e8f-128">Essa ação requer que o usuário seja um administrador ou tenha privilégios elevados com permissão para controlar serviços ou que o aplicativo faça parte de uma instalação gerenciada.</span><span class="sxs-lookup"><span data-stu-id="a1e8f-128">This action requires that the user be an administrator or have elevated privileges with permission to control services or that the application be part of a managed installation.</span></span>

 

 



