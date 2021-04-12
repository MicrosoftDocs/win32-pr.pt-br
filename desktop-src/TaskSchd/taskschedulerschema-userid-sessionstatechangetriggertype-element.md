---
title: Elemento UserId (sessionStateChangeTriggerType)
description: Contém o usuário para a sessão de Terminal Server. Quando uma alteração de estado de sessão é detectada para esse usuário, uma tarefa é iniciada.
ms.assetid: 7605f444-b2c9-4bba-a035-f1307c01184f
keywords:
- Elemento UserId Agendador de Tarefas
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd66a05d25ea9b44f124d55ccc0cbb2c628aeeb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499644"
---
# <a name="userid-sessionstatechangetriggertype-element"></a><span data-ttu-id="8c81e-105">Elemento UserId (sessionStateChangeTriggerType)</span><span class="sxs-lookup"><span data-stu-id="8c81e-105">UserId (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="8c81e-106">Contém o usuário para a sessão de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="8c81e-106">Contains the user for the Terminal Server session.</span></span> <span data-ttu-id="8c81e-107">Quando uma alteração de estado de sessão é detectada para esse usuário, uma tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="8c81e-107">When a session state change is detected for this user, a task is started.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="8c81e-108">O elemento **userid** é definido pelo tipo complexo [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8c81e-108">The **UserId** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8c81e-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="8c81e-109">Parent element</span></span>



| <span data-ttu-id="8c81e-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="8c81e-110">Element</span></span>                       | <span data-ttu-id="8c81e-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="8c81e-111">Derived from</span></span>                                                                                           | <span data-ttu-id="8c81e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c81e-112">Description</span></span>                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c81e-113">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="8c81e-113">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="8c81e-114">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="8c81e-114">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="8c81e-115">Especifica um gatilho que inicia uma tarefa quando uma sessão de Terminal Server muda de estado.</span><span class="sxs-lookup"><span data-stu-id="8c81e-115">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8c81e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c81e-116">Remarks</span></span>

<span data-ttu-id="8c81e-117">Para desenvolvimento em C++, consulte [**Propriedade UserID de ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).</span><span class="sxs-lookup"><span data-stu-id="8c81e-117">For C++ development, see [**UserId Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).</span></span>

<span data-ttu-id="8c81e-118">Para desenvolvimento de script, consulte [**SessionStateChangeTrigger. UserID**](sessionstatechangetrigger-userid.md).</span><span class="sxs-lookup"><span data-stu-id="8c81e-118">For script development, see [**SessionStateChangeTrigger.UserId**](sessionstatechangetrigger-userid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c81e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c81e-119">Requirements</span></span>



| <span data-ttu-id="8c81e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c81e-120">Requirement</span></span> | <span data-ttu-id="8c81e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8c81e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8c81e-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c81e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8c81e-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c81e-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8c81e-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c81e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8c81e-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c81e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





