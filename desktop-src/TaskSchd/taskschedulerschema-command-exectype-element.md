---
title: Elemento Command (exectype)
description: Especifica o arquivo ou documento executável a ser executado.
ms.assetid: dedf8627-926c-43c6-8add-21ff298d697a
keywords:
- Elemento de comando Agendador de Tarefas
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9d27eb5b40d652035882efc311d9735bcbdd23e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369825"
---
# <a name="command-exectype-element"></a><span data-ttu-id="a8173-104">Elemento Command (exectype)</span><span class="sxs-lookup"><span data-stu-id="a8173-104">Command (execType) Element</span></span>

<span data-ttu-id="a8173-105">Especifica o arquivo ou documento executável a ser executado.</span><span class="sxs-lookup"><span data-stu-id="a8173-105">Specifies the executable file or document to be run.</span></span>

``` syntax
<xs:element name="Command"
    type="pathType"
 />
```

<span data-ttu-id="a8173-106">O elemento **Command** é definido pelo tipo complexo [**exectype**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a8173-106">The **Command** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a8173-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a8173-107">Parent element</span></span>



| <span data-ttu-id="a8173-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8173-108">Element</span></span>                                                      | <span data-ttu-id="a8173-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="a8173-109">Derived from</span></span>                                                 | <span data-ttu-id="a8173-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8173-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="a8173-111">**Exec**</span><span class="sxs-lookup"><span data-stu-id="a8173-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="a8173-112">**exectype**</span><span class="sxs-lookup"><span data-stu-id="a8173-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="a8173-113">Especifica uma ação que executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a8173-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a8173-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8173-114">Remarks</span></span>

<span data-ttu-id="a8173-115">Para desenvolvimento em C++, consulte a [**Propriedade Arguments de IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span><span class="sxs-lookup"><span data-stu-id="a8173-115">For C++ development, see the [**Arguments property of IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span></span>

<span data-ttu-id="a8173-116">Para desenvolvimento de script, consulte [**execaction. Arguments**](execaction-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="a8173-116">For script development, see [**ExecAction.Arguments**](execaction-arguments.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a8173-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a8173-117">Examples</span></span>

<span data-ttu-id="a8173-118">Para obter um exemplo completo do XML para uma tarefa que usa uma ação executável, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="a8173-118">For a complete example of the XML for a task that uses an executable action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8173-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8173-119">Requirements</span></span>



| <span data-ttu-id="a8173-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8173-120">Requirement</span></span> | <span data-ttu-id="a8173-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a8173-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8173-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8173-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a8173-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8173-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8173-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8173-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a8173-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8173-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8173-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8173-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8173-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="a8173-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





