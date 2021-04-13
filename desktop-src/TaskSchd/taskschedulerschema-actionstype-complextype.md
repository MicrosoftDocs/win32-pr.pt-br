---
title: Tipo de ActionType complexo
description: Define os elementos filho e o atributo para o elemento actions.
ms.assetid: 01577b65-4bfa-4b9f-b9b9-6b2b0dbd582a
keywords:
- tipo de ActionType complexo Agendador de Tarefas
topic_type:
- apiref
api_name:
- actionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ebc2cf95803f6e4a02d4ec00d7aa767aa4e8a8a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369789"
---
# <a name="actionstype-complex-type"></a><span data-ttu-id="01f6a-104">Tipo de ActionType complexo</span><span class="sxs-lookup"><span data-stu-id="01f6a-104">actionsType Complex Type</span></span>

<span data-ttu-id="01f6a-105">Define os elementos filho e o atributo para o elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="01f6a-105">Defines the child elements and attribute for the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="actionsType">
    <xs:sequence>
        <xs:group
            maxOccurs="32"
            ref="actionGroup"
         />
    </xs:sequence>
    <xs:attribute name="Context"
        type="IDREF"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="01f6a-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="01f6a-106">Attributes</span></span>



| <span data-ttu-id="01f6a-107">Nome</span><span class="sxs-lookup"><span data-stu-id="01f6a-107">Name</span></span>    | <span data-ttu-id="01f6a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="01f6a-108">Type</span></span>  | <span data-ttu-id="01f6a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="01f6a-109">Description</span></span>                                                                                          |
|---------|-------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01f6a-110">Contexto</span><span class="sxs-lookup"><span data-stu-id="01f6a-110">Context</span></span> | <span data-ttu-id="01f6a-111">IDREF</span><span class="sxs-lookup"><span data-stu-id="01f6a-111">IDREF</span></span> | <span data-ttu-id="01f6a-112">O identificador principal do usado, que é o contexto de segurança das ações da tarefa.</span><span class="sxs-lookup"><span data-stu-id="01f6a-112">Principal identifier of the used who is the security context for the actions of the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="01f6a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01f6a-113">Requirements</span></span>



| <span data-ttu-id="01f6a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="01f6a-114">Requirement</span></span> | <span data-ttu-id="01f6a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="01f6a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="01f6a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01f6a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="01f6a-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01f6a-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="01f6a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01f6a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="01f6a-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="01f6a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01f6a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="01f6a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f6a-121">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="01f6a-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="01f6a-122">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="01f6a-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





