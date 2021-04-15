---
title: Elemento ClassID (comhandletype)
description: Especifica o identificador da classe do manipulador.
ms.assetid: 38ebcc39-85f2-4f61-8cb6-556c242a63d9
keywords:
- Elemento ClassID Agendador de Tarefas
topic_type:
- apiref
api_name:
- ClassId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89af2f39ae6a4a529fe7a728cf4b821245aa034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455987"
---
# <a name="classid-comhandlertype-element"></a><span data-ttu-id="46e9f-104">Elemento ClassID (comhandletype)</span><span class="sxs-lookup"><span data-stu-id="46e9f-104">ClassId (comHandlerType) Element</span></span>

<span data-ttu-id="46e9f-105">Especifica o identificador da classe do manipulador.</span><span class="sxs-lookup"><span data-stu-id="46e9f-105">Specifies the identifier of the handler class.</span></span>

``` syntax
<xs:element name="ClassId"
    type="guidType"
 />
```

<span data-ttu-id="46e9f-106">O elemento **ClassID** é definido pelo tipo complexo [**comhandletype**](taskschedulerschema-comhandlertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="46e9f-106">The **ClassId** element is defined by the [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="46e9f-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="46e9f-107">Parent element</span></span>



| <span data-ttu-id="46e9f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="46e9f-108">Element</span></span>                                                                  | <span data-ttu-id="46e9f-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="46e9f-109">Derived from</span></span>                                                             | <span data-ttu-id="46e9f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="46e9f-110">Description</span></span>                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="46e9f-111">**Commanipulador**</span><span class="sxs-lookup"><span data-stu-id="46e9f-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md) | [<span data-ttu-id="46e9f-112">**comhandletype**</span><span class="sxs-lookup"><span data-stu-id="46e9f-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md) | <span data-ttu-id="46e9f-113">Especifica uma ação que dispara um manipulador.</span><span class="sxs-lookup"><span data-stu-id="46e9f-113">Specifies an action that fires a handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="46e9f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="46e9f-114">Remarks</span></span>

<span data-ttu-id="46e9f-115">Os aplicativos definem o identificador de classe usando a propriedade [**ClassID**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) da interface [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .</span><span class="sxs-lookup"><span data-stu-id="46e9f-115">Applications define the class identifier using the [**ClassId**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) property of the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="46e9f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46e9f-116">Requirements</span></span>



| <span data-ttu-id="46e9f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="46e9f-117">Requirement</span></span> | <span data-ttu-id="46e9f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="46e9f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="46e9f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46e9f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="46e9f-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46e9f-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="46e9f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46e9f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="46e9f-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46e9f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46e9f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="46e9f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e9f-124">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="46e9f-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





