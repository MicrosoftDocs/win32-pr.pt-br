---
title: Tipo de Weekly Complex
description: Define o elemento filho e as informações de sequenciamento para o elemento Week.
ms.assetid: c9e8814c-b8f9-426d-943d-ca3efa5d914b
keywords:
- tipo complexo de weektype Agendador de Tarefas
topic_type:
- apiref
api_name:
- weeksType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 597cc72c043a478a414187f63a9aa89516dee658
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086112"
---
# <a name="weekstype-complex-type"></a><span data-ttu-id="97c3a-104">Tipo de Weekly Complex</span><span class="sxs-lookup"><span data-stu-id="97c3a-104">weeksType Complex Type</span></span>

<span data-ttu-id="97c3a-105">Define o elemento filho e as informações de sequenciamento para o elemento [**Week**](taskschedulerschema-week-weekstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="97c3a-105">Defines the child element and sequencing information for the [**Week**](taskschedulerschema-week-weekstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="weeksType">
    <xs:sequence>
        <xs:element name="Week"
            type="weekType"
            minOccurs="0"
            maxOccurs="5"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="97c3a-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="97c3a-106">Child elements</span></span>



| <span data-ttu-id="97c3a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="97c3a-107">Element</span></span>                                                    | <span data-ttu-id="97c3a-108">Type</span><span class="sxs-lookup"><span data-stu-id="97c3a-108">Type</span></span>                                                        | <span data-ttu-id="97c3a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="97c3a-109">Description</span></span>                                             |
|------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="97c3a-110">**Semana**</span><span class="sxs-lookup"><span data-stu-id="97c3a-110">**Week**</span></span>](taskschedulerschema-week-weekstype-element.md) | [<span data-ttu-id="97c3a-111">**weektype**</span><span class="sxs-lookup"><span data-stu-id="97c3a-111">**weekType**</span></span>](taskschedulerschema-weektype-simpletype.md) | <span data-ttu-id="97c3a-112">Especifica a semana em que a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="97c3a-112">Specifies the week in which the task is run.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="97c3a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97c3a-113">Requirements</span></span>



| <span data-ttu-id="97c3a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="97c3a-114">Requirement</span></span> | <span data-ttu-id="97c3a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="97c3a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="97c3a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97c3a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="97c3a-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97c3a-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="97c3a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97c3a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="97c3a-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="97c3a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97c3a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="97c3a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c3a-121">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="97c3a-121">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





