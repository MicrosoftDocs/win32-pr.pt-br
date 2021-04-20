---
title: Propriedade WeeklyTrigger. RandomDelay
description: Para scripts, Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. | Propriedade WeeklyTrigger. RandomDelay
ms.assetid: 711b188d-b283-4c99-b43d-644f39a31cdc
keywords:
- Agendador de Tarefas da propriedade RandomDelay
- Propriedade RandomDelay Agendador de Tarefas, objeto WeeklyTrigger
- Objeto WeeklyTrigger Agendador de Tarefas, Propriedade RandomDelay
topic_type:
- apiref
api_name:
- WeeklyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2b320b0def6f8e9cb0dabff9ff04bdfea3d858e
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734151"
---
# <a name="weeklytriggerrandomdelay-property"></a><span data-ttu-id="16c45-107">Propriedade WeeklyTrigger. RandomDelay</span><span class="sxs-lookup"><span data-stu-id="16c45-107">WeeklyTrigger.RandomDelay property</span></span>

<span data-ttu-id="16c45-108">Para scripts, Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.</span><span class="sxs-lookup"><span data-stu-id="16c45-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="16c45-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16c45-109">Syntax</span></span>


```VB
WeeklyTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="16c45-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="16c45-110">Property value</span></span>

<span data-ttu-id="16c45-111">O tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.</span><span class="sxs-lookup"><span data-stu-id="16c45-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="16c45-112">O formato dessa cadeia de caracteres é `P<days>DT<hours>H<minutes>M<seconds>S` (por exemplo, P2DT5S é um atraso de 2 dias, 5 segundos).</span><span class="sxs-lookup"><span data-stu-id="16c45-112">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="16c45-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16c45-113">Requirements</span></span>



| <span data-ttu-id="16c45-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="16c45-114">Requirement</span></span> | <span data-ttu-id="16c45-115">Valor</span><span class="sxs-lookup"><span data-stu-id="16c45-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16c45-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16c45-116">Minimum supported client</span></span><br/> | <span data-ttu-id="16c45-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16c45-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="16c45-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16c45-118">Minimum supported server</span></span><br/> | <span data-ttu-id="16c45-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="16c45-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="16c45-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="16c45-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="16c45-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="16c45-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="16c45-122">DLL</span><span class="sxs-lookup"><span data-stu-id="16c45-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16c45-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16c45-123"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





