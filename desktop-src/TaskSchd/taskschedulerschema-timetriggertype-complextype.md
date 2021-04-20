---
title: Tipo complexo timetriggertype
description: Define o tipo base para o elemento timetrigger.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- tipo complexo de timetriggertype Agendador de Tarefas
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f44f0959a9f67e4bfee0b0ef5dd7f095ffbadce
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734131"
---
# <a name="timetriggertype-complex-type"></a><span data-ttu-id="c88e9-104">Tipo complexo timetriggertype</span><span class="sxs-lookup"><span data-stu-id="c88e9-104">timeTriggerType Complex Type</span></span>

<span data-ttu-id="c88e9-105">Define o tipo base para o elemento [**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c88e9-105">Defines the base type for the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="timeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c88e9-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c88e9-106">Child elements</span></span>



| <span data-ttu-id="c88e9-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="c88e9-107">Element</span></span>                                                                        | <span data-ttu-id="c88e9-108">Type</span><span class="sxs-lookup"><span data-stu-id="c88e9-108">Type</span></span>     | <span data-ttu-id="c88e9-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c88e9-109">Description</span></span>                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c88e9-110">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="c88e9-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-timetriggertype-element.md) | <span data-ttu-id="c88e9-111">duration</span><span class="sxs-lookup"><span data-stu-id="c88e9-111">duration</span></span> | <span data-ttu-id="c88e9-112">Especifica o tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.</span><span class="sxs-lookup"><span data-stu-id="c88e9-112">Specifies the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="c88e9-113">O formato dessa cadeia de caracteres é `P<days>DT<hours>H<minutes>M<seconds>S` (por exemplo, P2DT5S é um atraso de 2 dias, 5 segundos).</span><span class="sxs-lookup"><span data-stu-id="c88e9-113">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="c88e9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c88e9-114">Remarks</span></span>

<span data-ttu-id="c88e9-115">Observe que esse elemento não adiciona nenhum elemento filho àqueles definidos pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c88e9-115">Note that this element does not add any child elements to those defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c88e9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c88e9-116">Requirements</span></span>



| <span data-ttu-id="c88e9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c88e9-117">Requirement</span></span> | <span data-ttu-id="c88e9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c88e9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c88e9-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c88e9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c88e9-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c88e9-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c88e9-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c88e9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c88e9-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c88e9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c88e9-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c88e9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c88e9-124">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="c88e9-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="c88e9-125">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="c88e9-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





