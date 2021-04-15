---
title: Propriedade comhandleaction. Data
description: Para scripts, Obtém ou define dados adicionais associados ao manipulador.
ms.assetid: bf4d3e77-4b2b-4622-b26b-a8f7e9aa687b
keywords:
- Agendador de Tarefas de propriedade de dados
- Propriedade de dados Agendador de Tarefas, objeto comhandleaction
- Agendador de Tarefas de objeto comhandleaction, propriedade data
topic_type:
- apiref
api_name:
- ComHandlerAction.Data
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15743c3f787a591a4644081fdd63189829d2eab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369852"
---
# <a name="comhandleractiondata-property"></a><span data-ttu-id="c383c-106">Propriedade comhandleaction. Data</span><span class="sxs-lookup"><span data-stu-id="c383c-106">ComHandlerAction.Data property</span></span>

<span data-ttu-id="c383c-107">Para scripts, Obtém ou define dados adicionais associados ao manipulador.</span><span class="sxs-lookup"><span data-stu-id="c383c-107">For scripting, gets or sets additional data that is associated with the handler.</span></span>

## <a name="syntax"></a><span data-ttu-id="c383c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c383c-108">Syntax</span></span>


```VB
ComHandlerAction.Data As String
```



## <a name="property-value"></a><span data-ttu-id="c383c-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c383c-109">Property value</span></span>

<span data-ttu-id="c383c-110">Os argumentos que são necessários para o manipulador.</span><span class="sxs-lookup"><span data-stu-id="c383c-110">The arguments that are needed by the handler.</span></span>

## <a name="remarks"></a><span data-ttu-id="c383c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c383c-111">Remarks</span></span>

<span data-ttu-id="c383c-112">Ao ler ou gravar XML, os dados de um manipulador COM são especificados no elemento [**Data**](taskschedulerschema-data-comhandlertype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="c383c-112">When reading or writing XML, the data of a COM handler is specified in the [**Data**](taskschedulerschema-data-comhandlertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="c383c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c383c-113">Requirements</span></span>



| <span data-ttu-id="c383c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c383c-114">Requirement</span></span> | <span data-ttu-id="c383c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c383c-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c383c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c383c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c383c-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c383c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c383c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c383c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c383c-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c383c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c383c-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c383c-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="c383c-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c383c-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c383c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c383c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c383c-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c383c-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c383c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c383c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c383c-125">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="c383c-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="c383c-126">**Comhandleaction**</span><span class="sxs-lookup"><span data-stu-id="c383c-126">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





