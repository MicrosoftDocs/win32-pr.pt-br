---
title: Propriedade ActionCollection. Context
description: Para scripts, Obtém ou define o identificador da entidade de segurança da tarefa.
ms.assetid: 5d8ac31c-ce07-4801-a04e-e12e996b88c6
keywords:
- Agendador de Tarefas de propriedade de contexto
- Propriedade de contexto Agendador de Tarefas, objeto ActionCollection
- Agendador de Tarefas de objeto ActionCollection, Propriedade Context
topic_type:
- apiref
api_name:
- ActionCollection.Context
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98318ba8332e4c3bb0e7fee6b702a7ed50533
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779893"
---
# <a name="actioncollectioncontext-property"></a><span data-ttu-id="fd1e4-106">Propriedade ActionCollection. Context</span><span class="sxs-lookup"><span data-stu-id="fd1e4-106">ActionCollection.Context property</span></span>

<span data-ttu-id="fd1e4-107">Para scripts, Obtém ou define o identificador da entidade de segurança da tarefa.</span><span class="sxs-lookup"><span data-stu-id="fd1e4-107">For scripting, gets or sets the identifier of the principal for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd1e4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd1e4-108">Syntax</span></span>


```VB
ActionCollection.Context As String
```



## <a name="property-value"></a><span data-ttu-id="fd1e4-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fd1e4-109">Property value</span></span>

<span data-ttu-id="fd1e4-110">O identificador da entidade de segurança para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="fd1e4-110">The identifier of the principal for the task.</span></span> <span data-ttu-id="fd1e4-111">O identificador especificado aqui deve corresponder ao identificador especificado na propriedade ID da interface IPrincipal que define a entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="fd1e4-111">The identifier that is specified here must match the identifier that is specified in the Id property of the IPrincipal interface that defines the principal.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd1e4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd1e4-112">Requirements</span></span>



| <span data-ttu-id="fd1e4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd1e4-113">Requirement</span></span> | <span data-ttu-id="fd1e4-114">Valor</span><span class="sxs-lookup"><span data-stu-id="fd1e4-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd1e4-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd1e4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fd1e4-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd1e4-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fd1e4-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd1e4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fd1e4-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fd1e4-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fd1e4-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fd1e4-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="fd1e4-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fd1e4-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fd1e4-121">DLL</span><span class="sxs-lookup"><span data-stu-id="fd1e4-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd1e4-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd1e4-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd1e4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd1e4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd1e4-124">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="fd1e4-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="fd1e4-125">**Açãocollection**</span><span class="sxs-lookup"><span data-stu-id="fd1e4-125">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





