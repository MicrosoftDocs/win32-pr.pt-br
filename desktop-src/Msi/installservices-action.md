---
description: A ação Installservices registra um serviço para o sistema. Esta ação consulta a tabela de instalação.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Ação installservices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5964deb08f811e391418211efc6f774261bd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789778"
---
# <a name="installservices-action"></a><span data-ttu-id="7248d-104">Ação installservices</span><span class="sxs-lookup"><span data-stu-id="7248d-104">InstallServices Action</span></span>

<span data-ttu-id="7248d-105">A ação Installservices registra um serviço para o sistema.</span><span class="sxs-lookup"><span data-stu-id="7248d-105">The InstallServices action registers a service for the system.</span></span> <span data-ttu-id="7248d-106">Esta ação consulta a [tabela de instalação](serviceinstall-table.md).</span><span class="sxs-lookup"><span data-stu-id="7248d-106">This action queries the [ServiceInstall table](serviceinstall-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="7248d-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="7248d-107">Sequence Restrictions</span></span>

<span data-ttu-id="7248d-108">A ação de serviços deve ser usada na sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="7248d-108">The services action must be used in the following sequence.</span></span>

[<span data-ttu-id="7248d-109">Pararservices</span><span class="sxs-lookup"><span data-stu-id="7248d-109">StopServices</span></span>](stopservices-action.md)

[<span data-ttu-id="7248d-110">Excluirservices</span><span class="sxs-lookup"><span data-stu-id="7248d-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="7248d-111">Qualquer uma das seguintes ações: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)e [RemoveDuplicateFiles](removeduplicatefiles-action.md) ações.</span><span class="sxs-lookup"><span data-stu-id="7248d-111">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>

<span data-ttu-id="7248d-112">Instalarservices</span><span class="sxs-lookup"><span data-stu-id="7248d-112">InstallServices</span></span>

[<span data-ttu-id="7248d-113">Iniciarservices</span><span class="sxs-lookup"><span data-stu-id="7248d-113">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="7248d-114">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="7248d-114">ActionData Messages</span></span>

<span data-ttu-id="7248d-115">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="7248d-115">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="7248d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7248d-116">Remarks</span></span>

<span data-ttu-id="7248d-117">Essa ação requer que o usuário seja um administrador ou tenha privilégios elevados com permissão para instalar serviços ou que o aplicativo faça parte de uma instalação gerenciada.</span><span class="sxs-lookup"><span data-stu-id="7248d-117">This action requires that the user be an administrator or have elevated privileges with permission to install services or that the application be part of a managed installation.</span></span>

 

 



