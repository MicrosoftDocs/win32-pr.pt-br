---
title: Elemento StopOnIdleEnd (idleSettingsType)
description: Especifica que o Agendador de Tarefas interromperá a tarefa se a condição de ociosidade terminar antes de a tarefa ser concluída.
ms.assetid: 5e8e4fd9-bba1-4ede-a0b3-9f50feb1b6f3
keywords:
- Agendador de Tarefas do elemento StopOnIdleEnd
topic_type:
- apiref
api_name:
- TerminateOnIdleEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a47a01d7d77f3dd20f055bce8e4bb12fad82c771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919050"
---
# <a name="stoponidleend-idlesettingstype-element"></a><span data-ttu-id="d5072-104">Elemento StopOnIdleEnd (idleSettingsType)</span><span class="sxs-lookup"><span data-stu-id="d5072-104">StopOnIdleEnd (idleSettingsType) Element</span></span>

<span data-ttu-id="d5072-105">Especifica que o Agendador de Tarefas interromperá a tarefa se a condição de ociosidade terminar antes de a tarefa ser concluída.</span><span class="sxs-lookup"><span data-stu-id="d5072-105">Specifies that the Task Scheduler will stop the task if the idle condition ends before the task is completed.</span></span>

``` syntax
<xs:element name="StopOnIdleEnd"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

<span data-ttu-id="d5072-106">O elemento **StopOnIdleEnd** é definido pelo tipo complexo [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d5072-106">The **StopOnIdleEnd** element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d5072-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="d5072-107">Parent element</span></span>



| <span data-ttu-id="d5072-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d5072-108">Element</span></span>                                                                       | <span data-ttu-id="d5072-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="d5072-109">Derived from</span></span>                                                                 | <span data-ttu-id="d5072-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5072-110">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5072-111">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="d5072-111">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="d5072-112">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="d5072-112">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="d5072-113">Especifica como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="d5072-113">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d5072-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5072-114">Remarks</span></span>

<span data-ttu-id="d5072-115">Para desenvolvimento em C++, consulte a [**Propriedade StopOnIdleEnd de IIdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).</span><span class="sxs-lookup"><span data-stu-id="d5072-115">For C++ development, see [**StopOnIdleEnd Property of IIdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).</span></span>

<span data-ttu-id="d5072-116">Para desenvolvimento de script, consulte [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md).</span><span class="sxs-lookup"><span data-stu-id="d5072-116">For script development, see [**IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d5072-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d5072-117">Examples</span></span>

<span data-ttu-id="d5072-118">O XML a seguir define uma configuração ociosa que indica que a tarefa não deve ser executada quando a condição ociosa terminar.</span><span class="sxs-lookup"><span data-stu-id="d5072-118">The following XML defines an idle setting that indicates the task should not be performed when the idle condition ends.</span></span>


```XML
<IdleSettings>
    <StopOnIdleEnd>false</StopOnIdleEnd>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="d5072-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5072-119">Requirements</span></span>



| <span data-ttu-id="d5072-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5072-120">Requirement</span></span> | <span data-ttu-id="d5072-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d5072-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d5072-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5072-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d5072-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5072-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d5072-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5072-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d5072-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5072-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5072-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5072-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5072-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="d5072-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





