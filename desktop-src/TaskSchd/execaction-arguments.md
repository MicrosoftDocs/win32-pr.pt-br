---
title: Propriedade execaction. Arguments
description: Para scripts, Obtém ou define os argumentos associados à operação de linha de comando.
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Propriedade Arguments Agendador de Tarefas
- Propriedade Arguments Agendador de Tarefas, objeto Execaction
- Agendador de Tarefas de objeto execaction, Propriedade Arguments
topic_type:
- apiref
api_name:
- ExecAction.Arguments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4207a9fbfb60d9e45c15e174a33e7d6ab66e5fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918218"
---
# <a name="execactionarguments-property"></a><span data-ttu-id="d90c7-106">Propriedade execaction. Arguments</span><span class="sxs-lookup"><span data-stu-id="d90c7-106">ExecAction.Arguments property</span></span>

<span data-ttu-id="d90c7-107">Para scripts, Obtém ou define os argumentos associados à operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="d90c7-107">For scripting, gets or sets the arguments associated with the command-line operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d90c7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d90c7-108">Syntax</span></span>


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a><span data-ttu-id="d90c7-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d90c7-109">Property value</span></span>

<span data-ttu-id="d90c7-110">Os argumentos que são necessários para a operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="d90c7-110">The arguments that are needed by the command-line operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d90c7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d90c7-111">Remarks</span></span>

<span data-ttu-id="d90c7-112">Ao ler ou gravar XML, os argumentos da operação de linha de comando são especificados no elemento [**arguments**](taskschedulerschema-arguments-exectype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="d90c7-112">When reading or writing XML, the command-line operation arguments are specified in the [**Arguments**](taskschedulerschema-arguments-exectype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d90c7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d90c7-113">Requirements</span></span>



| <span data-ttu-id="d90c7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d90c7-114">Requirement</span></span> | <span data-ttu-id="d90c7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d90c7-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d90c7-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d90c7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d90c7-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d90c7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d90c7-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d90c7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d90c7-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d90c7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d90c7-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d90c7-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="d90c7-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d90c7-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d90c7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d90c7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d90c7-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d90c7-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d90c7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d90c7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d90c7-125">**Execaction**</span><span class="sxs-lookup"><span data-stu-id="d90c7-125">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="d90c7-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="d90c7-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





