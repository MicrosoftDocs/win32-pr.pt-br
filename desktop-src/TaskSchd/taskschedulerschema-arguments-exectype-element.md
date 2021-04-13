---
title: Elemento Arguments (exectype)
description: Especifica os argumentos associados à operação de linha de comando.
ms.assetid: 37207c4f-941c-4cbf-9a81-5876b224a7c1
keywords:
- Elemento Arguments Agendador de Tarefas
topic_type:
- apiref
api_name:
- Arguments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff35465fbad1de82d096b583499ea6cdafe93ca7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499513"
---
# <a name="arguments-exectype-element"></a><span data-ttu-id="c4fa0-104">Elemento Arguments (exectype)</span><span class="sxs-lookup"><span data-stu-id="c4fa0-104">Arguments (execType) Element</span></span>

<span data-ttu-id="c4fa0-105">Especifica os argumentos associados à operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="c4fa0-105">Specifies the arguments associated with the command-line operation.</span></span>

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

<span data-ttu-id="c4fa0-106">O elemento **arguments** é definido pelo tipo complexo [**exectype**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c4fa0-106">The **Arguments** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c4fa0-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="c4fa0-107">Parent element</span></span>



| <span data-ttu-id="c4fa0-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c4fa0-108">Element</span></span>                                                      | <span data-ttu-id="c4fa0-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="c4fa0-109">Derived from</span></span>                                                 | <span data-ttu-id="c4fa0-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4fa0-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="c4fa0-111">**Exec**</span><span class="sxs-lookup"><span data-stu-id="c4fa0-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="c4fa0-112">**exectype**</span><span class="sxs-lookup"><span data-stu-id="c4fa0-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="c4fa0-113">Especifica uma ação que executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="c4fa0-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c4fa0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4fa0-114">Remarks</span></span>

<span data-ttu-id="c4fa0-115">Para desenvolvimento em C++, consulte a [**Propriedade Arguments de IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span><span class="sxs-lookup"><span data-stu-id="c4fa0-115">For C++ development, see the [**Arguments property of IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span></span>

<span data-ttu-id="c4fa0-116">Para desenvolvimento de script, consulte [**execaction. Arguments**](execaction-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="c4fa0-116">For script development, see [**ExecAction.Arguments**](execaction-arguments.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c4fa0-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c4fa0-117">Examples</span></span>

<span data-ttu-id="c4fa0-118">Para obter um exemplo completo do XML para uma tarefa que usa uma ação executável, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="c4fa0-118">For a complete example of the XML for a task that uses an executable action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4fa0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4fa0-119">Requirements</span></span>



| <span data-ttu-id="c4fa0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4fa0-120">Requirement</span></span> | <span data-ttu-id="c4fa0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c4fa0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c4fa0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4fa0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c4fa0-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4fa0-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c4fa0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4fa0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c4fa0-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c4fa0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c4fa0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4fa0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4fa0-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="c4fa0-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





