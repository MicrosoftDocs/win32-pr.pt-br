---
title: Tipo complexo logonTriggerType
description: Define os elementos filho e as informações de sequenciamento para o elemento LogonTrigger.
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- Agendador de Tarefas tipo complexo logonTriggerType
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81a3f42eb94d14506d96348b803c8b1bc41737d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758102"
---
# <a name="logontriggertype-complex-type"></a><span data-ttu-id="cc252-104">Tipo complexo logonTriggerType</span><span class="sxs-lookup"><span data-stu-id="cc252-104">logonTriggerType Complex Type</span></span>

<span data-ttu-id="cc252-105">Define os elementos filho e as informações de sequenciamento para o elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cc252-105">Defines the child elements and sequencing information for the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="logonTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
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

## <a name="child-elements"></a><span data-ttu-id="cc252-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cc252-106">Child elements</span></span>



| <span data-ttu-id="cc252-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="cc252-107">Element</span></span>                                                               | <span data-ttu-id="cc252-108">Type</span><span class="sxs-lookup"><span data-stu-id="cc252-108">Type</span></span>                                                                    | <span data-ttu-id="cc252-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc252-109">Description</span></span>                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc252-110">**Retardo**</span><span class="sxs-lookup"><span data-stu-id="cc252-110">**Delay**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)   | <span data-ttu-id="cc252-111">duration</span><span class="sxs-lookup"><span data-stu-id="cc252-111">duration</span></span>                                                                | <span data-ttu-id="cc252-112">Quantidade de tempo entre quando o usuário faz logon e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="cc252-112">Amount of time between when the user logs on and when the task is started.</span></span><br/>         |
| [<span data-ttu-id="cc252-113">**ID**</span><span class="sxs-lookup"><span data-stu-id="cc252-113">**UserId**</span></span>](taskschedulerschema-userid-logontriggertype-element.md) | [<span data-ttu-id="cc252-114">**não vazio**</span><span class="sxs-lookup"><span data-stu-id="cc252-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="cc252-115">Identificador do usuário.</span><span class="sxs-lookup"><span data-stu-id="cc252-115">Identifier of the user.</span></span> <span data-ttu-id="cc252-116">A tarefa é iniciada quando esse usuário faz logon no computador.</span><span class="sxs-lookup"><span data-stu-id="cc252-116">The task is started when this user logs onto the computer.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cc252-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc252-117">Remarks</span></span>

<span data-ttu-id="cc252-118">Além dos elementos filho definidos aqui, o elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) também usa elementos filho definidos pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cc252-118">In addition to the child elements defined here, the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc252-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc252-119">Requirements</span></span>



| <span data-ttu-id="cc252-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc252-120">Requirement</span></span> | <span data-ttu-id="cc252-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cc252-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cc252-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc252-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cc252-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc252-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cc252-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc252-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cc252-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc252-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc252-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc252-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc252-127">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="cc252-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="cc252-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="cc252-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





