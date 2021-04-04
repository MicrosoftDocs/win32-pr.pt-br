---
title: Tipo complexo comhandletype
description: Define os elementos filho e as informações de sequenciamento para o elemento commanipulador.
ms.assetid: 688e79f3-8b7e-4892-8119-b0a457ce9c7f
keywords:
- tipo complexo comhandletype Agendador de Tarefas
topic_type:
- apiref
api_name:
- comHandlerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d36a92651fc46c0a1950ecff00fa59fe56e1d758
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009156"
---
# <a name="comhandlertype-complex-type"></a><span data-ttu-id="219ee-104">Tipo complexo comhandletype</span><span class="sxs-lookup"><span data-stu-id="219ee-104">comHandlerType Complex Type</span></span>

<span data-ttu-id="219ee-105">Define os elementos filho e as informações de sequenciamento para o elemento [**commanipulador**](taskschedulerschema-comhandler-actiongroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="219ee-105">Defines the child elements and sequencing information for the [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="comHandlerType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="ClassId"
                    type="guidType"
                 />
                <xs:element name="Data"
                    type="dataType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="219ee-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="219ee-106">Child elements</span></span>



| <span data-ttu-id="219ee-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="219ee-107">Element</span></span>                                                               | <span data-ttu-id="219ee-108">Type</span><span class="sxs-lookup"><span data-stu-id="219ee-108">Type</span></span>                                                         | <span data-ttu-id="219ee-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="219ee-109">Description</span></span>                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="219ee-110">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="219ee-110">**ClassId**</span></span>](taskschedulerschema-classid-comhandlertype-element.md) | [<span data-ttu-id="219ee-111">**guidtype**</span><span class="sxs-lookup"><span data-stu-id="219ee-111">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md)  | <span data-ttu-id="219ee-112">Especifica o identificador da classe do manipulador.</span><span class="sxs-lookup"><span data-stu-id="219ee-112">Specifies the identifier of the handler class.</span></span><br/>          |
| [<span data-ttu-id="219ee-113">**Dados**</span><span class="sxs-lookup"><span data-stu-id="219ee-113">**Data**</span></span>](taskschedulerschema-data-comhandlertype-element.md)       | [<span data-ttu-id="219ee-114">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="219ee-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md) | <span data-ttu-id="219ee-115">Especifica dados adicionais associados ao manipulador.</span><span class="sxs-lookup"><span data-stu-id="219ee-115">Specifies additional data associated with the handler.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="219ee-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="219ee-116">Requirements</span></span>



| <span data-ttu-id="219ee-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="219ee-117">Requirement</span></span> | <span data-ttu-id="219ee-118">Valor</span><span class="sxs-lookup"><span data-stu-id="219ee-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="219ee-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="219ee-119">Minimum supported client</span></span><br/> | <span data-ttu-id="219ee-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="219ee-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="219ee-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="219ee-121">Minimum supported server</span></span><br/> | <span data-ttu-id="219ee-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="219ee-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="219ee-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="219ee-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="219ee-124">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="219ee-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="219ee-125">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="219ee-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





