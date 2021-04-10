---
title: Tipo complexo registrationInfoType
description: Define os elementos filho e as informações de sequenciamento para o elemento RegistrationInfo.
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- Agendador de Tarefas tipo complexo registrationInfoType
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe98a06daf84ec753c26903cc09787cec65c8d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918742"
---
# <a name="registrationinfotype-complex-type"></a><span data-ttu-id="0533b-104">Tipo complexo registrationInfoType</span><span class="sxs-lookup"><span data-stu-id="0533b-104">registrationInfoType Complex Type</span></span>

<span data-ttu-id="0533b-105">Define os elementos filho e as informações de sequenciamento para o elemento [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0533b-105">Defines the child elements and sequencing information for the [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="registrationInfoType">
    <xs:all>
        <xs:element name="URI"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="SecurityDescriptor"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Source"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Date"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Author"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Version"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Description"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Documentation"
            type="string"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="0533b-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0533b-106">Child elements</span></span>



| <span data-ttu-id="0533b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="0533b-107">Element</span></span>                                                                                           | <span data-ttu-id="0533b-108">Type</span><span class="sxs-lookup"><span data-stu-id="0533b-108">Type</span></span>     | <span data-ttu-id="0533b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0533b-109">Description</span></span>                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0533b-110">**Autor**</span><span class="sxs-lookup"><span data-stu-id="0533b-110">**Author**</span></span>](taskschedulerschema-author-registrationinfotype-element.md)                         | <span data-ttu-id="0533b-111">string</span><span class="sxs-lookup"><span data-stu-id="0533b-111">string</span></span>   | <span data-ttu-id="0533b-112">Especifica o autor da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0533b-112">Specifies the author of the task.</span></span><br/>                                                                       |
| [<span data-ttu-id="0533b-113">**Date**</span><span class="sxs-lookup"><span data-stu-id="0533b-113">**Date**</span></span>](taskschedulerschema-date-registrationinfotype-element.md)                             | <span data-ttu-id="0533b-114">dateTime</span><span class="sxs-lookup"><span data-stu-id="0533b-114">dateTime</span></span> | <span data-ttu-id="0533b-115">Especifica a data e a hora em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="0533b-115">Specifies the date and time when the task is registered.</span></span><br/>                                                |
| [<span data-ttu-id="0533b-116">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0533b-116">**Description**</span></span>](taskschedulerschema-description-registrationinfotype-element.md)               | <span data-ttu-id="0533b-117">string</span><span class="sxs-lookup"><span data-stu-id="0533b-117">string</span></span>   | <span data-ttu-id="0533b-118">Especifica a descrição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0533b-118">Specifies the description of the task.</span></span><br/>                                                                  |
| [<span data-ttu-id="0533b-119">**Documentação**</span><span class="sxs-lookup"><span data-stu-id="0533b-119">**Documentation**</span></span>](taskschedulerschema-documentation-registrationinfotype-element.md)           | <span data-ttu-id="0533b-120">string</span><span class="sxs-lookup"><span data-stu-id="0533b-120">string</span></span>   | <span data-ttu-id="0533b-121">Especifica qualquer documentação adicional para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="0533b-121">Specifies any additional documentation for the task.</span></span><br/>                                                    |
| [<span data-ttu-id="0533b-122">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0533b-122">**SecurityDescriptor**</span></span>](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | <span data-ttu-id="0533b-123">string</span><span class="sxs-lookup"><span data-stu-id="0533b-123">string</span></span>   | <span data-ttu-id="0533b-124">Especifica o descritor de segurança da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0533b-124">Specifies the security descriptor of the task.</span></span><br/>                                                          |
| [<span data-ttu-id="0533b-125">**Original**</span><span class="sxs-lookup"><span data-stu-id="0533b-125">**Source**</span></span>](taskschedulerschema-source-registrationinfotype-element.md)                         | <span data-ttu-id="0533b-126">string</span><span class="sxs-lookup"><span data-stu-id="0533b-126">string</span></span>   | <span data-ttu-id="0533b-127">Especifica de onde a tarefa foi originada.</span><span class="sxs-lookup"><span data-stu-id="0533b-127">Specifies where the task originated from.</span></span> <span data-ttu-id="0533b-128">Por exemplo, de um componente, serviço, aplicativo ou usuário.</span><span class="sxs-lookup"><span data-stu-id="0533b-128">For example, from a component, service, application, or user.</span></span><br/> |
| [<span data-ttu-id="0533b-129">**URI**</span><span class="sxs-lookup"><span data-stu-id="0533b-129">**URI**</span></span>](taskschedulerschema-uri-registrationinfotype-element.md)                               | <span data-ttu-id="0533b-130">anyURI</span><span class="sxs-lookup"><span data-stu-id="0533b-130">anyURI</span></span>   | <span data-ttu-id="0533b-131">Especifica o URI da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0533b-131">Specifies the URI of the task.</span></span><br/>                                                                          |
| [<span data-ttu-id="0533b-132">**Versão**</span><span class="sxs-lookup"><span data-stu-id="0533b-132">**Version**</span></span>](taskschedulerschema-version-registrationinfotype-element.md)                       | <span data-ttu-id="0533b-133">string</span><span class="sxs-lookup"><span data-stu-id="0533b-133">string</span></span>   | <span data-ttu-id="0533b-134">Especifica o número de versão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0533b-134">Specifies the version number of the task.</span></span><br/>                                                               |



## <a name="requirements"></a><span data-ttu-id="0533b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0533b-135">Requirements</span></span>



| <span data-ttu-id="0533b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0533b-136">Requirement</span></span> | <span data-ttu-id="0533b-137">Valor</span><span class="sxs-lookup"><span data-stu-id="0533b-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0533b-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0533b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0533b-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0533b-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0533b-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0533b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0533b-141">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0533b-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0533b-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="0533b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0533b-143">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="0533b-143">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="0533b-144">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="0533b-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





