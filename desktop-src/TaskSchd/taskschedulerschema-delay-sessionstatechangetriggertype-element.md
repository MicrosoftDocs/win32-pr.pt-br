---
title: Elemento Delay (sessionStateChangeTriggerType)
description: Contém um valor que indica o comprimento do atraso para uma hora de início da tarefa quando uma alteração de estado de sessão Terminal Server é detectada.
ms.assetid: 7fb87c4c-0b69-4c5b-b038-d61fb7c4ab9a
keywords:
- Elemento Delay Agendador de Tarefas
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03f230465f2e2b49ce83f1af358dfa1f84f21433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086455"
---
# <a name="delay-sessionstatechangetriggertype-element"></a><span data-ttu-id="e99a1-104">Elemento Delay (sessionStateChangeTriggerType)</span><span class="sxs-lookup"><span data-stu-id="e99a1-104">Delay (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="e99a1-105">Contém um valor que indica o comprimento do atraso para uma hora de início da tarefa quando uma alteração de estado de sessão Terminal Server é detectada.</span><span class="sxs-lookup"><span data-stu-id="e99a1-105">Contains a value that indicates the delay length for a task start time, when a Terminal Server session state change is detected.</span></span> <span data-ttu-id="e99a1-106">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="e99a1-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="e99a1-107">Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="e99a1-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="e99a1-108">O elemento **Delay** é definido pelo tipo complexo [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e99a1-108">The **Delay** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e99a1-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="e99a1-109">Parent element</span></span>



| <span data-ttu-id="e99a1-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="e99a1-110">Element</span></span>                       | <span data-ttu-id="e99a1-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e99a1-111">Derived from</span></span>                                                                                           | <span data-ttu-id="e99a1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="e99a1-112">Description</span></span>                                                                                      |
|-------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e99a1-113">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="e99a1-113">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="e99a1-114">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e99a1-114">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="e99a1-115">Especifica um gatilho que inicia uma tarefa quando uma sessão de Terminal Server muda de estado.</span><span class="sxs-lookup"><span data-stu-id="e99a1-115">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="e99a1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e99a1-116">Remarks</span></span>

<span data-ttu-id="e99a1-117">Para o desenvolvimento de scripts, o atraso de gatilho de alteração de estado de sessão é especificado usando a propriedade [**SessionStateChangeTrigger. Delay**](sessionstatechangetrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="e99a1-117">For scripting development, the session state change trigger delay is specified using the [**SessionStateChangeTrigger.Delay**](sessionstatechangetrigger-delay.md) property.</span></span>

<span data-ttu-id="e99a1-118">Para desenvolvimento em C++, o atraso de gatilho de alteração de estado de sessão é especificado usando a [**Propriedade Delay de ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).</span><span class="sxs-lookup"><span data-stu-id="e99a1-118">For C++ development, the session state change trigger delay is specified using the [**Delay property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="e99a1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e99a1-119">Requirements</span></span>



| <span data-ttu-id="e99a1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e99a1-120">Requirement</span></span> | <span data-ttu-id="e99a1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e99a1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e99a1-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e99a1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e99a1-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e99a1-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e99a1-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e99a1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e99a1-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e99a1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





