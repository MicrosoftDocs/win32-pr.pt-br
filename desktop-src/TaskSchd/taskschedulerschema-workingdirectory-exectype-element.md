---
title: Elemento WorkingDirectory (exectype)
description: Especifica o diretório em que o executável ou os arquivos usados pelo executável existem.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- Agendador de Tarefas do elemento WorkingDirectory
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8c382d0e60b16d85fbc86f7579a0e700d3dd30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810446"
---
# <a name="workingdirectory-exectype-element"></a><span data-ttu-id="1aa26-104">Elemento WorkingDirectory (exectype)</span><span class="sxs-lookup"><span data-stu-id="1aa26-104">WorkingDirectory (execType) Element</span></span>

<span data-ttu-id="1aa26-105">Especifica o diretório em que o executável ou os arquivos usados pelo executável existem.</span><span class="sxs-lookup"><span data-stu-id="1aa26-105">Specifies the directory where either the executable or those files used by the executable exists.</span></span>

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

<span data-ttu-id="1aa26-106">O elemento **WorkingDirectory** é definido pelo tipo complexo [**exectype**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1aa26-106">The **WorkingDirectory** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1aa26-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="1aa26-107">Parent element</span></span>



| <span data-ttu-id="1aa26-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="1aa26-108">Element</span></span>                                                      | <span data-ttu-id="1aa26-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="1aa26-109">Derived from</span></span>                                                 | <span data-ttu-id="1aa26-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1aa26-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="1aa26-111">**Exec**</span><span class="sxs-lookup"><span data-stu-id="1aa26-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="1aa26-112">**exectype**</span><span class="sxs-lookup"><span data-stu-id="1aa26-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="1aa26-113">Especifica uma ação que executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="1aa26-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1aa26-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1aa26-114">Remarks</span></span>

<span data-ttu-id="1aa26-115">Para o desenvolvimento de script, o diretório de trabalho é especificado pela propriedade [**execaction. WorkingDirectory**](execaction-workingdirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="1aa26-115">For script development, the working directory is specified by the [**ExecAction.WorkingDirectory**](execaction-workingdirectory.md) property.</span></span>

<span data-ttu-id="1aa26-116">Para desenvolvimento em C++, o diretório de trabalho é especificado pela propriedade [**IExecAction:: WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) .</span><span class="sxs-lookup"><span data-stu-id="1aa26-116">For C++ development, the working directory is specified by the [**IExecAction::WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) property.</span></span>

## <a name="examples"></a><span data-ttu-id="1aa26-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1aa26-117">Examples</span></span>

<span data-ttu-id="1aa26-118">O XML a seguir define uma ação de execução.</span><span class="sxs-lookup"><span data-stu-id="1aa26-118">The following XML defines a execution action.</span></span>


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
```



## <a name="requirements"></a><span data-ttu-id="1aa26-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1aa26-119">Requirements</span></span>



| <span data-ttu-id="1aa26-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1aa26-120">Requirement</span></span> | <span data-ttu-id="1aa26-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1aa26-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1aa26-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1aa26-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1aa26-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1aa26-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1aa26-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1aa26-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1aa26-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1aa26-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1aa26-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="1aa26-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa26-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="1aa26-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="1aa26-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="1aa26-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





