---
title: Tipo complexo registrationTriggerType
description: Define elementos filho e informações de sequenciamento para o elemento RegistrationTrigger.
ms.assetid: 3663c015-67cf-4775-a1a6-4429cce93b96
keywords:
- Agendador de Tarefas tipo complexo registrationTriggerType
topic_type:
- apiref
api_name:
- registrationTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ddb55436a0a6980a8909da636a02ca59244ca85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369786"
---
# <a name="registrationtriggertype-complex-type"></a><span data-ttu-id="58bb7-104">Tipo complexo registrationTriggerType</span><span class="sxs-lookup"><span data-stu-id="58bb7-104">registrationTriggerType Complex Type</span></span>

<span data-ttu-id="58bb7-105">Define elementos filho e informações de sequenciamento para o elemento [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="58bb7-105">Defines child elements and sequencing information for the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="registrationTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="58bb7-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="58bb7-106">Child elements</span></span>



| <span data-ttu-id="58bb7-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="58bb7-107">Element</span></span>                                                                    | <span data-ttu-id="58bb7-108">Type</span><span class="sxs-lookup"><span data-stu-id="58bb7-108">Type</span></span>     | <span data-ttu-id="58bb7-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="58bb7-109">Description</span></span>                                                                                               |
|----------------------------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58bb7-110">**Retardo**</span><span class="sxs-lookup"><span data-stu-id="58bb7-110">**Delay**</span></span>](taskschedulerschema-delay-registrationtriggertype-element.md) | <span data-ttu-id="58bb7-111">duration</span><span class="sxs-lookup"><span data-stu-id="58bb7-111">duration</span></span> | <span data-ttu-id="58bb7-112">Especifica a quantidade de tempo entre quando a tarefa é registrada e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="58bb7-112">Specifies the amount of time between when the task is registered and when the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="58bb7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="58bb7-113">Remarks</span></span>

<span data-ttu-id="58bb7-114">Além dos elementos filho definidos aqui, o elemento [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) também usa elementos filho definidos pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="58bb7-114">In addition to the child elements defined here, the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="58bb7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58bb7-115">Requirements</span></span>



| <span data-ttu-id="58bb7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="58bb7-116">Requirement</span></span> | <span data-ttu-id="58bb7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="58bb7-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="58bb7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58bb7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="58bb7-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58bb7-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="58bb7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58bb7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="58bb7-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="58bb7-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58bb7-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="58bb7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58bb7-123">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="58bb7-123">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="58bb7-124">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="58bb7-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





