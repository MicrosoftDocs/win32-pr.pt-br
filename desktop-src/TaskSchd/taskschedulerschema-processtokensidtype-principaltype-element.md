---
title: Elemento ProcessTokenSidType (PrincipalType)
description: Especifica o tipo de SID (identificação de segurança) do processo da tarefa.
ms.assetid: d9bffa92-c0dc-4332-a29c-7f2710ec34e3
keywords:
- Agendador de Tarefas do elemento ProcessTokenSidType
topic_type:
- apiref
api_name:
- ProcessTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875da055f2719afca454d225c3bebd13b404b3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085873"
---
# <a name="processtokensidtype-principaltype-element"></a><span data-ttu-id="984ec-104">Elemento ProcessTokenSidType (PrincipalType)</span><span class="sxs-lookup"><span data-stu-id="984ec-104">ProcessTokenSidType (principalType) Element</span></span>

<span data-ttu-id="984ec-105">Especifica o tipo de SID (identificação de segurança) do processo da tarefa.</span><span class="sxs-lookup"><span data-stu-id="984ec-105">Specifies the process security identify (SID) type of the task.</span></span>

``` syntax
<xs:element name="ProcessTokenSidType"
    type="processTokenSidType"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="984ec-106">O elemento **ProcessTokenSidType** é definido pelo tipo complexo de [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="984ec-106">The **ProcessTokenSidType** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="984ec-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="984ec-107">Parent element</span></span>



| <span data-ttu-id="984ec-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="984ec-108">Element</span></span>                                                                  | <span data-ttu-id="984ec-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="984ec-109">Derived from</span></span>                                                           | <span data-ttu-id="984ec-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="984ec-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="984ec-111">**Beneficiário**</span><span class="sxs-lookup"><span data-stu-id="984ec-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="984ec-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="984ec-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="984ec-113">Especifica as credenciais de segurança para uma entidade.</span><span class="sxs-lookup"><span data-stu-id="984ec-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="984ec-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="984ec-114">Remarks</span></span>

<span data-ttu-id="984ec-115">Para desenvolvimento em C++, o tipo de SID de processo é especificado usando a propriedade [**IPrincipal2::P rocesstokensidtype**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) .</span><span class="sxs-lookup"><span data-stu-id="984ec-115">For C++ development, the process SID type is specified by using the [**IPrincipal2::ProcessTokenSidType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) property.</span></span>

## <a name="examples"></a><span data-ttu-id="984ec-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="984ec-116">Examples</span></span>

<span data-ttu-id="984ec-117">O XML a seguir define o tipo de SID de processo da tarefa.</span><span class="sxs-lookup"><span data-stu-id="984ec-117">The following XML defines the process SID type of the task.</span></span>


```XML
<Principal>
    <GroupId>NT AUTHORITY\LOCAL SERVICE</GroupId>
    <ProcessTokenSidType>None</ProcessTokenSidType>
</Principal>
```



## <a name="requirements"></a><span data-ttu-id="984ec-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="984ec-118">Requirements</span></span>



| <span data-ttu-id="984ec-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="984ec-119">Requirement</span></span> | <span data-ttu-id="984ec-120">Valor</span><span class="sxs-lookup"><span data-stu-id="984ec-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="984ec-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="984ec-121">Minimum supported client</span></span><br/> | <span data-ttu-id="984ec-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="984ec-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="984ec-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="984ec-123">Minimum supported server</span></span><br/> | <span data-ttu-id="984ec-124">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="984ec-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="984ec-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="984ec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="984ec-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="984ec-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





