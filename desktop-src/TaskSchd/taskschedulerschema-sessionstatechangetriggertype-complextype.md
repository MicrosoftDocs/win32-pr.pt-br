---
title: Tipo complexo sessionStateChangeTriggerType
description: Define os elementos usados para criar um gatilho de tarefa para conexão ou desconexão do console, conexão remota ou desconexão ou bloqueio de estação de trabalho ou notificações de desbloqueio.
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- Agendador de Tarefas tipo complexo sessionStateChangeTriggerType
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8eb3ad02aef3f5bbbc078f8eafa52f3439819cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295908"
---
# <a name="sessionstatechangetriggertype-complex-type"></a><span data-ttu-id="d7d6a-104">Tipo complexo sessionStateChangeTriggerType</span><span class="sxs-lookup"><span data-stu-id="d7d6a-104">sessionStateChangeTriggerType Complex Type</span></span>

<span data-ttu-id="d7d6a-105">Define os elementos usados para criar um gatilho de tarefa para conexão ou desconexão do console, conexão remota ou desconexão ou bloqueio de estação de trabalho ou notificações de desbloqueio.</span><span class="sxs-lookup"><span data-stu-id="d7d6a-105">Defines the elements used to create a task trigger for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.</span></span>

``` syntax
<xs:complexType name="sessionStateChangeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="StateChange"
                    type="sessionStateChangeType"
                    minOccurs="1"
                    maxOccurs="1"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d7d6a-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d7d6a-106">Child elements</span></span>



| <span data-ttu-id="d7d6a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="d7d6a-107">Element</span></span>                                                                                      | <span data-ttu-id="d7d6a-108">Type</span><span class="sxs-lookup"><span data-stu-id="d7d6a-108">Type</span></span>                                                                                    | <span data-ttu-id="d7d6a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7d6a-109">Description</span></span>                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7d6a-110">**Retardo**</span><span class="sxs-lookup"><span data-stu-id="d7d6a-110">**Delay**</span></span>](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | <span data-ttu-id="d7d6a-111">duration</span><span class="sxs-lookup"><span data-stu-id="d7d6a-111">duration</span></span>                                                                                | <span data-ttu-id="d7d6a-112">Especifica um valor que indica o comprimento do atraso antes que uma tarefa seja iniciada quando uma alteração de estado de sessão de Terminal Server for detectada.</span><span class="sxs-lookup"><span data-stu-id="d7d6a-112">Specifies a value that indicates the length of the delay before a task is started when a Terminal Server session state change is detected.</span></span><br/> |
| [<span data-ttu-id="d7d6a-113">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="d7d6a-113">**StateChange**</span></span>](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [<span data-ttu-id="d7d6a-114">**sessionStateChangeType**</span><span class="sxs-lookup"><span data-stu-id="d7d6a-114">**sessionStateChangeType**</span></span>](taskschedulerschema-sessionstatechangetype-simpletype.md) | <span data-ttu-id="d7d6a-115">Especifica o tipo de Terminal Server alteração de sessão que dispararia uma inicialização de tarefa.</span><span class="sxs-lookup"><span data-stu-id="d7d6a-115">Specifies the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                     |
| [<span data-ttu-id="d7d6a-116">**ID**</span><span class="sxs-lookup"><span data-stu-id="d7d6a-116">**UserId**</span></span>](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [<span data-ttu-id="d7d6a-117">**não vazio**</span><span class="sxs-lookup"><span data-stu-id="d7d6a-117">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                 | <span data-ttu-id="d7d6a-118">Especifica o usuário para a sessão de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="d7d6a-118">Specifies the user for the Terminal Server session.</span></span> <span data-ttu-id="d7d6a-119">Quando uma alteração de estado de sessão é detectada para esse usuário, uma tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="d7d6a-119">When a session state change is detected for this user, a task is started.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="d7d6a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7d6a-120">Requirements</span></span>



| <span data-ttu-id="d7d6a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7d6a-121">Requirement</span></span> | <span data-ttu-id="d7d6a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d7d6a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d7d6a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7d6a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d7d6a-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7d6a-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d7d6a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7d6a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d7d6a-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d7d6a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





