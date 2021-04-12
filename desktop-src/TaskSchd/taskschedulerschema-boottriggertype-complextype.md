---
title: Tipo complexo bootTriggerType
description: Define o elemento filho e as informações de sequenciamento para o elemento BootTrigger.
ms.assetid: 36ade928-7640-4f91-ab76-18398b0cd65f
keywords:
- Agendador de Tarefas tipo complexo bootTriggerType
topic_type:
- apiref
api_name:
- bootTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d16634cacb9c17e5027ac9e6b6dd7abb26b78007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455638"
---
# <a name="boottriggertype-complex-type"></a><span data-ttu-id="df660-104">Tipo complexo bootTriggerType</span><span class="sxs-lookup"><span data-stu-id="df660-104">bootTriggerType Complex Type</span></span>

<span data-ttu-id="df660-105">Define o elemento filho e as informações de sequenciamento para o elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="df660-105">Defines the child element and sequencing information for the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="bootTriggerType">
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

## <a name="child-elements"></a><span data-ttu-id="df660-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="df660-106">Child elements</span></span>



| <span data-ttu-id="df660-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="df660-107">Element</span></span>                                                            | <span data-ttu-id="df660-108">Type</span><span class="sxs-lookup"><span data-stu-id="df660-108">Type</span></span>     | <span data-ttu-id="df660-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="df660-109">Description</span></span>                                                                                 |
|--------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df660-110">**Retardo**</span><span class="sxs-lookup"><span data-stu-id="df660-110">**Delay**</span></span>](taskschedulerschema-delay-boottriggertype-element.md) | <span data-ttu-id="df660-111">duration</span><span class="sxs-lookup"><span data-stu-id="df660-111">duration</span></span> | <span data-ttu-id="df660-112">Quantidade de tempo entre quando o sistema é inicializado e quando o gatilho é acionado.</span><span class="sxs-lookup"><span data-stu-id="df660-112">Amount of time between when the system is booted and when the trigger is fired.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="df660-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="df660-113">Remarks</span></span>

<span data-ttu-id="df660-114">Além do elemento filho definido aqui, o elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) também usa elementos filho definidos pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="df660-114">In addition to the child element defined here, the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="df660-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df660-115">Requirements</span></span>



| <span data-ttu-id="df660-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="df660-116">Requirement</span></span> | <span data-ttu-id="df660-117">Valor</span><span class="sxs-lookup"><span data-stu-id="df660-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="df660-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df660-118">Minimum supported client</span></span><br/> | <span data-ttu-id="df660-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df660-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="df660-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df660-120">Minimum supported server</span></span><br/> | <span data-ttu-id="df660-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="df660-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df660-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="df660-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df660-123">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="df660-123">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="df660-124">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="df660-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





