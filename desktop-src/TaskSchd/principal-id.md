---
title: Propriedade Principal.Id
description: Para scripts, Obtém ou define o identificador da entidade de segurança.
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- Agendador de Tarefas de propriedade de ID
- Propriedade de ID Agendador de Tarefas, objeto principal
- Objeto principal Agendador de Tarefas, Propriedade ID
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369791"
---
# <a name="principalid-property"></a><span data-ttu-id="4a814-106">Propriedade Principal.Id</span><span class="sxs-lookup"><span data-stu-id="4a814-106">Principal.Id property</span></span>

<span data-ttu-id="4a814-107">Para scripts, Obtém ou define o identificador da entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="4a814-107">For scripting, gets or sets the identifier of the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a814-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a814-108">Syntax</span></span>


```VB
Principal.Id As String
```



## <a name="property-value"></a><span data-ttu-id="4a814-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4a814-109">Property value</span></span>

<span data-ttu-id="4a814-110">O identificador da entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="4a814-110">The identifier of the principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a814-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a814-111">Remarks</span></span>

<span data-ttu-id="4a814-112">Esse identificador também é usado ao especificar a propriedade [**ActionCollection. Context**](actioncollection-context.md) .</span><span class="sxs-lookup"><span data-stu-id="4a814-112">This identifier is also used when specifying the [**ActionCollection.Context**](actioncollection-context.md) property.</span></span>

<span data-ttu-id="4a814-113">Ao ler ou gravar XML para uma tarefa, o identificador da entidade de segurança é especificado no atributo ID do elemento [**principal**](taskschedulerschema-principal-principaltype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="4a814-113">When reading or writing XML for a task, the identifier of the principal is specified in the Id attribute of the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a814-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a814-114">Requirements</span></span>



| <span data-ttu-id="4a814-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a814-115">Requirement</span></span> | <span data-ttu-id="4a814-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4a814-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a814-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a814-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4a814-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a814-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4a814-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a814-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4a814-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a814-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4a814-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4a814-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="4a814-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4a814-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4a814-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4a814-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a814-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a814-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a814-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a814-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a814-126">**ActionCollection. Context**</span><span class="sxs-lookup"><span data-stu-id="4a814-126">**ActionCollection.Context**</span></span>](actioncollection-context.md)
</dt> <dt>

[<span data-ttu-id="4a814-127">**Beneficiário**</span><span class="sxs-lookup"><span data-stu-id="4a814-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="4a814-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4a814-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





