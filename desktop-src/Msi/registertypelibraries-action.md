---
description: A ação RegisterTypeLibraries registra bibliotecas de tipos com o sistema. Essa ação é aplicada a cada arquivo referenciado na tabela TypeLib que está agendada para instalação.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: Ação RegisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469cc18fc2842a3258804fc012c48a49085f1598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754347"
---
# <a name="registertypelibraries-action"></a><span data-ttu-id="af66f-104">Ação RegisterTypeLibraries</span><span class="sxs-lookup"><span data-stu-id="af66f-104">RegisterTypeLibraries Action</span></span>

<span data-ttu-id="af66f-105">A ação RegisterTypeLibraries registra bibliotecas de tipos com o sistema.</span><span class="sxs-lookup"><span data-stu-id="af66f-105">The RegisterTypeLibraries action registers type libraries with the system.</span></span> <span data-ttu-id="af66f-106">Essa ação é aplicada a cada arquivo referenciado na [tabela Typelib](typelib-table.md) que está agendada para instalação.</span><span class="sxs-lookup"><span data-stu-id="af66f-106">This action is applied to each file referred to in the [TypeLib table](typelib-table.md) that is scheduled for install.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="af66f-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="af66f-107">Sequence Restrictions</span></span>

<span data-ttu-id="af66f-108">A ação RegisterTypeLibraries deve vir após a ação [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="af66f-108">The RegisterTypeLibraries action must come after the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="af66f-109">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="af66f-109">ActionData Messages</span></span>



| <span data-ttu-id="af66f-110">Campo</span><span class="sxs-lookup"><span data-stu-id="af66f-110">Field</span></span> | <span data-ttu-id="af66f-111">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="af66f-111">Description of action data</span></span>                   |
|-------|----------------------------------------------|
| <span data-ttu-id="af66f-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="af66f-112">\[1\]</span></span> | <span data-ttu-id="af66f-113">[GUID](guid.md) da biblioteca de tipos registrada.</span><span class="sxs-lookup"><span data-stu-id="af66f-113">[GUID](guid.md) of registered type library.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="af66f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="af66f-114">Remarks</span></span>

<span data-ttu-id="af66f-115">A ação RegisterTypeLibraries requer que o idioma da biblioteca de tipos seja criado corretamente no campo idioma da tabela TypeLib.</span><span class="sxs-lookup"><span data-stu-id="af66f-115">The RegisterTypeLibraries action requires that the type library language be correctly authored in the Language field of the TypeLib table.</span></span> <span data-ttu-id="af66f-116">A criação incorreta do campo de idioma pode fazer com que o instalador falhe ao registrar uma biblioteca de tipos válida de outra forma.</span><span class="sxs-lookup"><span data-stu-id="af66f-116">Incorrect authoring of the Language field can cause the installer to fail to register an otherwise valid type library.</span></span>

 

 



