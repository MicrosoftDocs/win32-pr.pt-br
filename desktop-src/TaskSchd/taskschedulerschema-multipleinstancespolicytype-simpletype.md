---
title: Tipo simples de multipleInstancesPolicyType
description: Define as constantes de política de instância para o elemento MultipleInstancesPolicy (settingstype).
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- Agendador de Tarefas tipo simples de multipleInstancesPolicyType
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29a3523ef16224836ada474fb32265084453479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918664"
---
# <a name="multipleinstancespolicytype-simple-type"></a><span data-ttu-id="dd293-104">Tipo simples de multipleInstancesPolicyType</span><span class="sxs-lookup"><span data-stu-id="dd293-104">multipleInstancesPolicyType Simple Type</span></span>

<span data-ttu-id="dd293-105">Define as constantes de política de instância para o elemento [**MultipleInstancesPolicy (settingstype)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="dd293-105">Defines the instance policy constants for the [**MultipleInstancesPolicy (settingsType)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="multipleInstancesPolicyType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="Parallel"
         />
        <xs:enumeration
            value="Queue"
         />
        <xs:enumeration
            value="IgnoreNew"
         />
        <xs:enumeration
            value="StopExisting"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="dd293-106">Valores de enumeração</span><span class="sxs-lookup"><span data-stu-id="dd293-106">Enumeration values</span></span>

<span data-ttu-id="dd293-107">O tipo simples **multipleInstancesPolicyType** define os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="dd293-107">The **multipleInstancesPolicyType** simple type defines the following values.</span></span>



| <span data-ttu-id="dd293-108">Valor</span><span class="sxs-lookup"><span data-stu-id="dd293-108">Value</span></span>        | <span data-ttu-id="dd293-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd293-109">Description</span></span>                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd293-110">Paralelo</span><span class="sxs-lookup"><span data-stu-id="dd293-110">Parallel</span></span>     | <span data-ttu-id="dd293-111">Inicia a nova instância enquanto uma instância existente está em execução.</span><span class="sxs-lookup"><span data-stu-id="dd293-111">Starts new instance while an existing instance is running.</span></span><br/>                           |
| <span data-ttu-id="dd293-112">Fila</span><span class="sxs-lookup"><span data-stu-id="dd293-112">Queue</span></span>        | <span data-ttu-id="dd293-113">Inicia a nova instância da tarefa depois que todas as outras instâncias da tarefa são concluídas.</span><span class="sxs-lookup"><span data-stu-id="dd293-113">Starts new instance of task after all other instances of the task are complete.</span></span><br/>      |
| <span data-ttu-id="dd293-114">IgnoreNew</span><span class="sxs-lookup"><span data-stu-id="dd293-114">IgnoreNew</span></span>    | <span data-ttu-id="dd293-115">Padrão.</span><span class="sxs-lookup"><span data-stu-id="dd293-115">Default.</span></span> <span data-ttu-id="dd293-116">Não iniciará nova instância se uma instância existente da tarefa estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="dd293-116">Does not start new instance if an existing instance of the task is running.</span></span><br/> |
| <span data-ttu-id="dd293-117">StopExisting</span><span class="sxs-lookup"><span data-stu-id="dd293-117">StopExisting</span></span> | <span data-ttu-id="dd293-118">Interrompe uma instância existente da tarefa antes de iniciar nova instância.</span><span class="sxs-lookup"><span data-stu-id="dd293-118">Stops an existing instance of the task before it starts new instance.</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="dd293-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd293-119">Requirements</span></span>



| <span data-ttu-id="dd293-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd293-120">Requirement</span></span> | <span data-ttu-id="dd293-121">Valor</span><span class="sxs-lookup"><span data-stu-id="dd293-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dd293-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd293-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dd293-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd293-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dd293-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd293-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dd293-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dd293-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd293-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd293-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd293-127">Tipos simples de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="dd293-127">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="dd293-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="dd293-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





