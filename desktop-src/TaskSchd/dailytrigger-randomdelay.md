---
title: Propriedade DailyTrigger. RandomDelay
description: Para scripts, Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. | Propriedade DailyTrigger. RandomDelay
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- Agendador de Tarefas da propriedade RandomDelay
- Propriedade RandomDelay Agendador de Tarefas, objeto DailyTrigger
- Objeto DailyTrigger Agendador de Tarefas, Propriedade RandomDelay
topic_type:
- apiref
api_name:
- DailyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303192d578a2681e250784c1e1eb2831c98482cc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734101"
---
# <a name="dailytriggerrandomdelay-property"></a><span data-ttu-id="bc368-107">Propriedade DailyTrigger. RandomDelay</span><span class="sxs-lookup"><span data-stu-id="bc368-107">DailyTrigger.RandomDelay property</span></span>

<span data-ttu-id="bc368-108">Para scripts, Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.</span><span class="sxs-lookup"><span data-stu-id="bc368-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc368-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc368-109">Syntax</span></span>


```VB
DailyTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="bc368-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bc368-110">Property value</span></span>

<span data-ttu-id="bc368-111">O tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.</span><span class="sxs-lookup"><span data-stu-id="bc368-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="bc368-112">O formato dessa cadeia de caracteres é `P<days>DT<hours>H<minutes>M<seconds>S` (por exemplo, P2DT5S é um atraso de 2 dias, 5 segundos).</span><span class="sxs-lookup"><span data-stu-id="bc368-112">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc368-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc368-113">Requirements</span></span>



| <span data-ttu-id="bc368-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc368-114">Requirement</span></span> | <span data-ttu-id="bc368-115">Valor</span><span class="sxs-lookup"><span data-stu-id="bc368-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc368-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc368-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bc368-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc368-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bc368-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc368-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bc368-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bc368-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bc368-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bc368-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc368-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bc368-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bc368-122">DLL</span><span class="sxs-lookup"><span data-stu-id="bc368-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc368-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc368-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc368-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bc368-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc368-125">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="bc368-125">**DailyTrigger**</span></span>](dailytrigger.md)
</dt> <dt>

[<span data-ttu-id="bc368-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="bc368-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





