---
description: A ação DeleteServices interrompe um serviço e remove seu registro do sistema. Esta ação consulta a tabela de UserControl.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: Ação de excluirservices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5fc22bbb0c11cd546f1ffbb9f3ad98e06efae3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296918"
---
# <a name="deleteservices-action"></a><span data-ttu-id="e4a03-104">Ação de excluirservices</span><span class="sxs-lookup"><span data-stu-id="e4a03-104">DeleteServices Action</span></span>

<span data-ttu-id="e4a03-105">A ação DeleteServices interrompe um serviço e remove seu registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="e4a03-105">The DeleteServices action stops a service and removes its registration from the system.</span></span> <span data-ttu-id="e4a03-106">Esta ação consulta a [tabela de UserControl](servicecontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="e4a03-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e4a03-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="e4a03-107">Sequence Restrictions</span></span>

<span data-ttu-id="e4a03-108">As ações de serviços devem ser usadas na seguinte sequência:</span><span class="sxs-lookup"><span data-stu-id="e4a03-108">The services actions must be used in the following sequence:</span></span>

1.  [<span data-ttu-id="e4a03-109">Pararservices</span><span class="sxs-lookup"><span data-stu-id="e4a03-109">StopServices</span></span>](stopservices-action.md)
2.  <span data-ttu-id="e4a03-110">Excluirservices</span><span class="sxs-lookup"><span data-stu-id="e4a03-110">DeleteServices</span></span>
3.  <span data-ttu-id="e4a03-111">Qualquer uma das seguintes ações: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)e [RemoveDuplicateFiles](removeduplicatefiles-action.md) ações.</span><span class="sxs-lookup"><span data-stu-id="e4a03-111">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>
4.  [<span data-ttu-id="e4a03-112">Ação installservices</span><span class="sxs-lookup"><span data-stu-id="e4a03-112">InstallServices action</span></span>](installservices-action.md)
5.  [<span data-ttu-id="e4a03-113">Iniciarservices</span><span class="sxs-lookup"><span data-stu-id="e4a03-113">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="e4a03-114">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="e4a03-114">ActionData Messages</span></span>



| <span data-ttu-id="e4a03-115">Campo</span><span class="sxs-lookup"><span data-stu-id="e4a03-115">Field</span></span> | <span data-ttu-id="e4a03-116">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="e4a03-116">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="e4a03-117">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e4a03-117">\[1\]</span></span> | <span data-ttu-id="e4a03-118">Nome de exibição do serviço.</span><span class="sxs-lookup"><span data-stu-id="e4a03-118">Service display name.</span></span>      |
| <span data-ttu-id="e4a03-119">\[2\]</span><span class="sxs-lookup"><span data-stu-id="e4a03-119">\[2\]</span></span> | <span data-ttu-id="e4a03-120">Nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="e4a03-120">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="e4a03-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4a03-121">Remarks</span></span>

<span data-ttu-id="e4a03-122">Essa ação requer que o usuário seja um administrador ou tenha privilégios elevados com permissão para excluir serviços ou que o aplicativo faça parte de uma instalação gerenciada.</span><span class="sxs-lookup"><span data-stu-id="e4a03-122">This action requires the user be an administrator or have elevated privileges with permission to delete services or that the application be part of a managed installation.</span></span>

 

 



