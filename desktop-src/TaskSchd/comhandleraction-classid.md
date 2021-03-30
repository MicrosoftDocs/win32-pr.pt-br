---
title: Propriedade comhandleaction. ClassID
description: Para scripts, Obtém ou define o identificador da classe do manipulador.
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- Agendador de Tarefas da propriedade ClassID
- Propriedade ClassID Agendador de Tarefas, objeto comhandleaction
- Objeto comhandleaction Agendador de Tarefas, Propriedade ClassID
topic_type:
- apiref
api_name:
- ComHandlerAction.ClassId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30409d5ea8067d1148bf42c88e2a3d1bb6f65ad1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644491"
---
# <a name="comhandleractionclassid-property"></a><span data-ttu-id="dcb70-106">Propriedade comhandleaction. ClassID</span><span class="sxs-lookup"><span data-stu-id="dcb70-106">ComHandlerAction.ClassId property</span></span>

<span data-ttu-id="dcb70-107">Para scripts, Obtém ou define o identificador da classe do manipulador.</span><span class="sxs-lookup"><span data-stu-id="dcb70-107">For scripting, gets or sets the identifier of the handler class.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcb70-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dcb70-108">Syntax</span></span>


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a><span data-ttu-id="dcb70-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="dcb70-109">Property value</span></span>

<span data-ttu-id="dcb70-110">O identificador da classe que define o manipulador a ser acionado.</span><span class="sxs-lookup"><span data-stu-id="dcb70-110">The identifier of the class that defines the handler to be fired.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcb70-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="dcb70-111">Remarks</span></span>

<span data-ttu-id="dcb70-112">Ao ler ou gravar XML, a classe de um manipulador COM é especificada no elemento [**ClassID**](taskschedulerschema-classid-comhandlertype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="dcb70-112">When reading or writing XML, the class of a COM handler is specified in the [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcb70-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcb70-113">Requirements</span></span>



| <span data-ttu-id="dcb70-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcb70-114">Requirement</span></span> | <span data-ttu-id="dcb70-115">Valor</span><span class="sxs-lookup"><span data-stu-id="dcb70-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb70-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcb70-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dcb70-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dcb70-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dcb70-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcb70-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dcb70-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dcb70-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dcb70-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="dcb70-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="dcb70-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dcb70-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dcb70-122">DLL</span><span class="sxs-lookup"><span data-stu-id="dcb70-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcb70-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcb70-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcb70-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="dcb70-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcb70-125">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="dcb70-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="dcb70-126">**Comhandleaction**</span><span class="sxs-lookup"><span data-stu-id="dcb70-126">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





