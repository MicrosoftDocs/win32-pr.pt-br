---
title: Tipo complexo TaskListtype
description: Define uma lista de tarefas que são usadas para identificar os componentes de um aplicativo.
ms.assetid: 41a46967-7c5b-4555-9f65-bd9582c0c492
keywords:
- Log de eventos de tipo complexo TaskListtype
topic_type:
- apiref
api_name:
- TaskListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad427743242ada8901e904fc4e03620ccc72f405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369190"
---
# <a name="tasklisttype-complex-type"></a><span data-ttu-id="9475f-104">Tipo complexo TaskListtype</span><span class="sxs-lookup"><span data-stu-id="9475f-104">TaskListType Complex Type</span></span>

<span data-ttu-id="9475f-105">Define uma lista de tarefas que são usadas para identificar os componentes de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9475f-105">Defines a list of tasks that are used to identify the components of an application.</span></span>

``` syntax
<xs:complexType name="TaskListType">
    <xs:sequence>
        <xs:element name="task"
            type="TaskType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="9475f-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9475f-106">Child elements</span></span>



| <span data-ttu-id="9475f-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="9475f-107">Element</span></span>                                                       | <span data-ttu-id="9475f-108">Type</span><span class="sxs-lookup"><span data-stu-id="9475f-108">Type</span></span>                                                         | <span data-ttu-id="9475f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="9475f-109">Description</span></span>                                                       |
|---------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="9475f-110">**agenda**</span><span class="sxs-lookup"><span data-stu-id="9475f-110">**task**</span></span>](eventmanifestschema-task-tasklisttype-element.md) | [<span data-ttu-id="9475f-111">**TaskType**</span><span class="sxs-lookup"><span data-stu-id="9475f-111">**TaskType**</span></span>](eventmanifestschema-tasktype-complextype.md) | <span data-ttu-id="9475f-112">Define um componente ou subcomponente de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9475f-112">Defines a component or subcomponent of an application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9475f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9475f-113">Requirements</span></span>



| <span data-ttu-id="9475f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9475f-114">Requirement</span></span> | <span data-ttu-id="9475f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9475f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9475f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9475f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9475f-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9475f-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9475f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9475f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9475f-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9475f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





