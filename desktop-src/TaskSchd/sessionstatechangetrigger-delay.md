---
title: Propriedade SessionStateChangeTrigger. Delay
description: Para scripts, Obtém ou define um valor que indica por quanto tempo um atraso ocorre antes de uma tarefa ser iniciada depois que uma alteração de estado de sessão de Terminal Server é detectada.
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- Agendador de Tarefas de propriedade de atraso
- Propriedade Delay Agendador de Tarefas, objeto SessionStateChangeTrigger
- Agendador de Tarefas de objeto SessionStateChangeTrigger, Propriedade Delay
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd5afde8ebd2884aee19fbdafb785355b9fedb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085318"
---
# <a name="sessionstatechangetriggerdelay-property"></a><span data-ttu-id="cf9f0-106">Propriedade SessionStateChangeTrigger. Delay</span><span class="sxs-lookup"><span data-stu-id="cf9f0-106">SessionStateChangeTrigger.Delay property</span></span>

<span data-ttu-id="cf9f0-107">Para scripts, Obtém ou define um valor que indica por quanto tempo um atraso ocorre antes de uma tarefa ser iniciada depois que uma alteração de estado de sessão de Terminal Server é detectada.</span><span class="sxs-lookup"><span data-stu-id="cf9f0-107">For scripting, gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected.</span></span> <span data-ttu-id="cf9f0-108">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="cf9f0-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="cf9f0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf9f0-109">Syntax</span></span>


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="cf9f0-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cf9f0-110">Property value</span></span>

<span data-ttu-id="cf9f0-111">O atraso que ocorre antes de uma tarefa ser iniciada depois que uma alteração de estado de sessão de Terminal Server é detectada.</span><span class="sxs-lookup"><span data-stu-id="cf9f0-111">The delay that takes place before a task is started after a Terminal Server session state change is detected.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf9f0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf9f0-112">Requirements</span></span>



| <span data-ttu-id="cf9f0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf9f0-113">Requirement</span></span> | <span data-ttu-id="cf9f0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="cf9f0-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf9f0-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf9f0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cf9f0-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf9f0-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cf9f0-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf9f0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cf9f0-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cf9f0-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cf9f0-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cf9f0-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="cf9f0-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cf9f0-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cf9f0-121">DLL</span><span class="sxs-lookup"><span data-stu-id="cf9f0-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf9f0-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf9f0-122"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





