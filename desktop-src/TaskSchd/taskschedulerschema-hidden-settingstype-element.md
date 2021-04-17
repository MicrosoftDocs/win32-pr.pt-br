---
title: Elemento oculto (settingstype)
description: Especifica que a tarefa não será visível na interface do usuário por padrão.
ms.assetid: a08c270f-6d4e-4473-9538-c1e1e21b3b10
keywords:
- Elemento oculto Agendador de Tarefas
topic_type:
- apiref
api_name:
- Hidden
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef5ad479fe3107ed8fa79f0f86307254a9f33c4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789838"
---
# <a name="hidden-settingstype-element"></a><span data-ttu-id="d8801-104">Elemento oculto (settingstype)</span><span class="sxs-lookup"><span data-stu-id="d8801-104">Hidden (settingsType) Element</span></span>

<span data-ttu-id="d8801-105">Especifica que a tarefa não será visível na interface do usuário por padrão.</span><span class="sxs-lookup"><span data-stu-id="d8801-105">Specifies that the task will not be visible in the UI by default.</span></span> <span data-ttu-id="d8801-106">No entanto, os administradores podem substituir essa configuração por meio do uso de um "comutador mestre" que torna todas as tarefas visíveis na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="d8801-106">However, administrators can override this setting through the use of a "master switch" that makes all tasks visible in the UI.</span></span>

``` syntax
<xs:element name="Hidden"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="d8801-107">O elemento **Hidden** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d8801-107">The **Hidden** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d8801-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="d8801-108">Parent element</span></span>



| <span data-ttu-id="d8801-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="d8801-109">Element</span></span>                                                           | <span data-ttu-id="d8801-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="d8801-110">Derived from</span></span>                                                         | <span data-ttu-id="d8801-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8801-111">Description</span></span>                                                                    |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="d8801-112">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="d8801-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="d8801-113">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="d8801-113">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="d8801-114">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="d8801-114">Contains the settings that Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d8801-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8801-115">Remarks</span></span>

<span data-ttu-id="d8801-116">Para desenvolvimento em C++, consulte [**Propriedade Hidden de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).</span><span class="sxs-lookup"><span data-stu-id="d8801-116">For C++ development, see [**Hidden Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).</span></span>

<span data-ttu-id="d8801-117">Para desenvolvimento de script, consulte [**TaskSettings. Hidden**](tasksettings-hidden.md).</span><span class="sxs-lookup"><span data-stu-id="d8801-117">For script development, see [**TaskSettings.Hidden**](tasksettings-hidden.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8801-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8801-118">Requirements</span></span>



| <span data-ttu-id="d8801-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8801-119">Requirement</span></span> | <span data-ttu-id="d8801-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d8801-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d8801-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8801-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d8801-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8801-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d8801-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8801-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d8801-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d8801-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8801-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8801-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8801-126">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="d8801-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





