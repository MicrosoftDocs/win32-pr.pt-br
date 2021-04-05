---
title: Elemento data (comhandletype)
description: Especifica dados adicionais associados ao manipulador.
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
keywords:
- Agendador de Tarefas de elemento de dados
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d009005dc2bb889c8bd9e34e84d853665310330a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918903"
---
# <a name="data-comhandlertype-element"></a><span data-ttu-id="63231-104">Elemento data (comhandletype)</span><span class="sxs-lookup"><span data-stu-id="63231-104">Data (comHandlerType) Element</span></span>

<span data-ttu-id="63231-105">Especifica dados adicionais associados ao manipulador.</span><span class="sxs-lookup"><span data-stu-id="63231-105">Specifies additional data associated with the handler.</span></span>

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

<span data-ttu-id="63231-106">O elemento de **dados** é definido pelo tipo complexo [**comhandletype**](taskschedulerschema-comhandlertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="63231-106">The **Data** element is defined by the [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="63231-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="63231-107">Parent element</span></span>



| <span data-ttu-id="63231-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="63231-108">Element</span></span>                                                                  | <span data-ttu-id="63231-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="63231-109">Derived from</span></span>                                                             | <span data-ttu-id="63231-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="63231-110">Description</span></span>                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="63231-111">**Commanipulador**</span><span class="sxs-lookup"><span data-stu-id="63231-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md) | [<span data-ttu-id="63231-112">**comhandletype**</span><span class="sxs-lookup"><span data-stu-id="63231-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md) | <span data-ttu-id="63231-113">Especifica uma ação que dispara um manipulador.</span><span class="sxs-lookup"><span data-stu-id="63231-113">Specifies an action that fires a handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="63231-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="63231-114">Remarks</span></span>

<span data-ttu-id="63231-115">Os aplicativos definem os dados do manipulador usando a propriedade [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) da interface [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .</span><span class="sxs-lookup"><span data-stu-id="63231-115">Applications define the handler data using the [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) property of the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="63231-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63231-116">Requirements</span></span>



| <span data-ttu-id="63231-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="63231-117">Requirement</span></span> | <span data-ttu-id="63231-118">Valor</span><span class="sxs-lookup"><span data-stu-id="63231-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="63231-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63231-119">Minimum supported client</span></span><br/> | <span data-ttu-id="63231-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63231-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="63231-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63231-121">Minimum supported server</span></span><br/> | <span data-ttu-id="63231-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63231-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63231-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="63231-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63231-124">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="63231-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





