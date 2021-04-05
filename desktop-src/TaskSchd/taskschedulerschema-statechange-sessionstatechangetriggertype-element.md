---
title: Elemento StateChange (sessionStateChangeTriggerType)
description: Contém o tipo de Terminal Server alteração de sessão que dispararia um lançamento de tarefa.
ms.assetid: 0b17a4a5-caa7-4b58-a1a4-cbc7564838bb
keywords:
- Agendador de Tarefas do elemento StateChange
topic_type:
- apiref
api_name:
- StateChange
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3991a767256184f23fbb9defda7e33465c0477e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086445"
---
# <a name="statechange-sessionstatechangetriggertype-element"></a><span data-ttu-id="fa751-104">Elemento StateChange (sessionStateChangeTriggerType)</span><span class="sxs-lookup"><span data-stu-id="fa751-104">StateChange (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="fa751-105">Contém o tipo de Terminal Server alteração de sessão que dispararia um lançamento de tarefa.</span><span class="sxs-lookup"><span data-stu-id="fa751-105">Contains the kind of Terminal Server session change that would trigger a task launch.</span></span>

``` syntax
<xs:element name="StateChange"
    type="sessionStateChangeType"
 />
```

<span data-ttu-id="fa751-106">O elemento **StateChange** é definido pelo tipo complexo [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="fa751-106">The **StateChange** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="fa751-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="fa751-107">Parent element</span></span>



| <span data-ttu-id="fa751-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="fa751-108">Element</span></span>                       | <span data-ttu-id="fa751-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="fa751-109">Derived from</span></span>                                                                                           | <span data-ttu-id="fa751-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa751-110">Description</span></span>                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa751-111">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="fa751-111">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="fa751-112">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="fa751-112">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="fa751-113">Especifica um gatilho que inicia uma tarefa quando uma sessão de Terminal Server muda de estado.</span><span class="sxs-lookup"><span data-stu-id="fa751-113">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fa751-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa751-114">Remarks</span></span>

<span data-ttu-id="fa751-115">Para desenvolvimento em C++, consulte a [**Propriedade StateChange de ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).</span><span class="sxs-lookup"><span data-stu-id="fa751-115">For C++ development, see [**StateChange Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).</span></span>

<span data-ttu-id="fa751-116">Para desenvolvimento de script, consulte [**SessionStateChangeTrigger. StateChange**](sessionstatechangetrigger-statechange.md).</span><span class="sxs-lookup"><span data-stu-id="fa751-116">For script development, see [**SessionStateChangeTrigger.StateChange**](sessionstatechangetrigger-statechange.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa751-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa751-117">Requirements</span></span>



| <span data-ttu-id="fa751-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa751-118">Requirement</span></span> | <span data-ttu-id="fa751-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fa751-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fa751-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa751-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fa751-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa751-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fa751-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa751-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fa751-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fa751-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





