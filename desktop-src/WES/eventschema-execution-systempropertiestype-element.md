---
title: Elemento Execution (SystemPropertiesType)
description: Contém informações sobre o processo e o thread que registrou o evento.
ms.assetid: 4d2feb0d-a3e6-479c-aa34-cd95a708add5
keywords:
- Elemento de execução EventLog
topic_type:
- apiref
api_name:
- Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64137153ffb0f1ba9816f060f0d5af0a2c6ee8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644364"
---
# <a name="execution-systempropertiestype-element"></a><span data-ttu-id="d033f-104">Elemento Execution (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="d033f-104">Execution (SystemPropertiesType) Element</span></span>

<span data-ttu-id="d033f-105">Contém informações sobre o processo e o thread que registrou o evento.</span><span class="sxs-lookup"><span data-stu-id="d033f-105">Contains information about the process and thread that logged the event.</span></span>

``` syntax
<xs:element name="Execution">
    <xs:complexType>
        <xs:attribute name="ProcessID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ThreadID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ProcessorID"
            type="unsignedByte"
            use="optional"
         />
        <xs:attribute name="SessionID"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="KernelTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="UserTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="ProcessorTime"
            type="unsignedInt"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="d033f-106">O elemento **Execution** é definido pelo tipo complexo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d033f-106">The **Execution** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="d033f-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="d033f-107">Attributes</span></span>



| <span data-ttu-id="d033f-108">Nome</span><span class="sxs-lookup"><span data-stu-id="d033f-108">Name</span></span>          | <span data-ttu-id="d033f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d033f-109">Type</span></span>         | <span data-ttu-id="d033f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d033f-110">Description</span></span>                                                                                               |
|---------------|--------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d033f-111">Kerneltime</span><span class="sxs-lookup"><span data-stu-id="d033f-111">KernelTime</span></span>    | <span data-ttu-id="d033f-112">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d033f-112">unsignedInt</span></span>  | <span data-ttu-id="d033f-113">Tempo de execução decorrido para instruções do modo kernel, em unidades de tempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="d033f-113">Elapsed execution time for kernel-mode instructions, in CPU time units.</span></span><br/>                        |
| <span data-ttu-id="d033f-114">ProcessID</span><span class="sxs-lookup"><span data-stu-id="d033f-114">ProcessID</span></span>     | <span data-ttu-id="d033f-115">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d033f-115">unsignedInt</span></span>  | <span data-ttu-id="d033f-116">Identifica o processo que gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="d033f-116">Identifies the process that generated the event.</span></span><br/>                                               |
| <span data-ttu-id="d033f-117">Processador</span><span class="sxs-lookup"><span data-stu-id="d033f-117">ProcessorID</span></span>   | <span data-ttu-id="d033f-118">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="d033f-118">unsignedByte</span></span> | <span data-ttu-id="d033f-119">O número de identificação do processador que processou o evento.</span><span class="sxs-lookup"><span data-stu-id="d033f-119">The identification number for the processor that processed the event.</span></span><br/>                          |
| <span data-ttu-id="d033f-120">Processadortime</span><span class="sxs-lookup"><span data-stu-id="d033f-120">ProcessorTime</span></span> | <span data-ttu-id="d033f-121">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d033f-121">unsignedInt</span></span>  | <span data-ttu-id="d033f-122">Para sessões privadas do ETW, o tempo de execução decorrido para as instruções do modo de usuário, em tiques de CPU.</span><span class="sxs-lookup"><span data-stu-id="d033f-122">For ETW private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.</span></span><br/> |
| <span data-ttu-id="d033f-123">SessionID</span><span class="sxs-lookup"><span data-stu-id="d033f-123">SessionID</span></span>     | <span data-ttu-id="d033f-124">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d033f-124">unsignedInt</span></span>  | <span data-ttu-id="d033f-125">O número de identificação da sessão do Terminal Server na qual o evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="d033f-125">The identification number for the terminal server session in which the event occurred.</span></span><br/>         |
| <span data-ttu-id="d033f-126">ThreadID</span><span class="sxs-lookup"><span data-stu-id="d033f-126">ThreadID</span></span>      | <span data-ttu-id="d033f-127">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d033f-127">unsignedInt</span></span>  | <span data-ttu-id="d033f-128">Identifica o thread que gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="d033f-128">Identifies the thread that generated the event.</span></span><br/>                                                |
| <span data-ttu-id="d033f-129">Usertime</span><span class="sxs-lookup"><span data-stu-id="d033f-129">UserTime</span></span>      | <span data-ttu-id="d033f-130">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d033f-130">unsignedInt</span></span>  | <span data-ttu-id="d033f-131">Tempo de execução decorrido para instruções do modo de usuário, em unidades de tempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="d033f-131">Elapsed execution time for user-mode instructions, in CPU time units.</span></span><br/>                          |



## <a name="requirements"></a><span data-ttu-id="d033f-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d033f-132">Requirements</span></span>



| <span data-ttu-id="d033f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d033f-133">Requirement</span></span> | <span data-ttu-id="d033f-134">Valor</span><span class="sxs-lookup"><span data-stu-id="d033f-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d033f-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d033f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d033f-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d033f-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d033f-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d033f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d033f-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d033f-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d033f-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="d033f-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="d033f-140">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="d033f-140">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d033f-141">**SystemPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="d033f-141">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)
</dt> <dt>

<span data-ttu-id="d033f-142">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="d033f-142">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d033f-143">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="d033f-143">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





