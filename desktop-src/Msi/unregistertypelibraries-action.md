---
description: A ação UnregisterTypeLibraries cancela o registro de bibliotecas de tipos do sistema. Essa ação é aplicada a cada arquivo listado na tabela TypeLib que é disparada para ser desinstalada.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: Ação UnregisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399f80d940839c5e94028a9c32e706f4826341a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748755"
---
# <a name="unregistertypelibraries-action"></a><span data-ttu-id="a782a-104">Ação UnregisterTypeLibraries</span><span class="sxs-lookup"><span data-stu-id="a782a-104">UnregisterTypeLibraries Action</span></span>

<span data-ttu-id="a782a-105">A ação UnregisterTypeLibraries cancela o registro de bibliotecas de tipos do sistema.</span><span class="sxs-lookup"><span data-stu-id="a782a-105">The UnregisterTypeLibraries action unregisters type libraries from the system.</span></span> <span data-ttu-id="a782a-106">Essa ação é aplicada a cada arquivo listado na tabela [TypeLib](typelib-table.md) que é disparada para ser desinstalada.</span><span class="sxs-lookup"><span data-stu-id="a782a-106">This action is applied to each file listed in the [TypeLib](typelib-table.md) table that is triggered to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a782a-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="a782a-107">Sequence Restrictions</span></span>

<span data-ttu-id="a782a-108">A ação UnregisterTypeLibraries deve vir antes da ação [RemoveFiles](removefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="a782a-108">The UnregisterTypeLibraries action must come before the [RemoveFiles](removefiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a782a-109">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="a782a-109">ActionData Messages</span></span>



| <span data-ttu-id="a782a-110">Campo</span><span class="sxs-lookup"><span data-stu-id="a782a-110">Field</span></span> | <span data-ttu-id="a782a-111">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="a782a-111">Description of action data</span></span>                        |
|-------|---------------------------------------------------|
| <span data-ttu-id="a782a-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a782a-112">\[1\]</span></span> | <span data-ttu-id="a782a-113">[GUID](guid.md) de uma biblioteca de tipos não registrada.</span><span class="sxs-lookup"><span data-stu-id="a782a-113">[GUID](guid.md) of an unregistered type library.</span></span> |



 

 

 



