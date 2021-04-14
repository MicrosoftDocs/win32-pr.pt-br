---
title: Tipo complexo de PrincipalType
description: Define o atributo, os elementos filho e as informações de sequenciamento para o elemento principal.
ms.assetid: 0f39d0a7-c9c9-402f-afe1-4378466ac1b6
keywords:
- tipo complexo de PrincipalType Agendador de Tarefas
topic_type:
- apiref
api_name:
- principalType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 037013a4b40984df41e52aa13be69c1247b1c05c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455630"
---
# <a name="principaltype-complex-type"></a><span data-ttu-id="15299-104">Tipo complexo de PrincipalType</span><span class="sxs-lookup"><span data-stu-id="15299-104">principalType Complex Type</span></span>

<span data-ttu-id="15299-105">Define o atributo, os elementos filho e as informações de sequenciamento para o elemento [**principal**](taskschedulerschema-principal-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="15299-105">Defines the attribute, child elements, and sequencing information for the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element.</span></span>

``` syntax
<xs:complexType name="principalType">
    <xs:all>
        <xs:element name="UserId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="LogonType"
            type="logonType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="GroupId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="DisplayName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunLevel"
            type="runLevelType"
            minOccurs="0"
         />
        <xs:element name="ProcessTokenSidType"
            type="processTokenSidType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="RequiredPrivileges"
            type="requiredPrivilegesType"
            minOccurs="0"
         />
    </xs:all>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="15299-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="15299-106">Child elements</span></span>



| <span data-ttu-id="15299-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="15299-107">Element</span></span>                                                                                             | <span data-ttu-id="15299-108">Type</span><span class="sxs-lookup"><span data-stu-id="15299-108">Type</span></span>                                                                                     | <span data-ttu-id="15299-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="15299-109">Description</span></span>                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15299-110">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="15299-110">**DisplayName**</span></span>](taskschedulerschema-displayname-principaltype-element.md)                        | <span data-ttu-id="15299-111">string</span><span class="sxs-lookup"><span data-stu-id="15299-111">string</span></span>                                                                                   | <span data-ttu-id="15299-112">Especifica o nome da entidade de segurança que é exibida na interface do usuário do Agendador de Tarefas (UI).</span><span class="sxs-lookup"><span data-stu-id="15299-112">Specifies the name of the principal that is displayed in the Task Scheduler user interface (UI).</span></span><br/>                 |
| [<span data-ttu-id="15299-113">**GroupId**</span><span class="sxs-lookup"><span data-stu-id="15299-113">**GroupId**</span></span>](taskschedulerschema-groupid-principaltype-element.md)                                | [<span data-ttu-id="15299-114">**não vazio**</span><span class="sxs-lookup"><span data-stu-id="15299-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                  | <span data-ttu-id="15299-115">Especifica o identificador do grupo de usuários que é necessário para executar tarefas associadas à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="15299-115">Specifies the identifier of the user group that is required to run tasks that are associated with the principal.</span></span><br/> |
| [<span data-ttu-id="15299-116">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="15299-116">**LogonType**</span></span>](taskschedulerschema-logontype-principaltype-element.md)                            | [<span data-ttu-id="15299-117">**logonType**</span><span class="sxs-lookup"><span data-stu-id="15299-117">**logonType**</span></span>](taskschedulerschema-logontype-simpletype.md)                            | <span data-ttu-id="15299-118">Especifica o método de logon de segurança que é necessário para executar tarefas associadas à entidade.</span><span class="sxs-lookup"><span data-stu-id="15299-118">Specifies the security logon method that is required to run tasks that are associated with the principal.</span></span><br/>        |
| [<span data-ttu-id="15299-119">**ProcessTokenSidType**</span><span class="sxs-lookup"><span data-stu-id="15299-119">**ProcessTokenSidType**</span></span>](taskschedulerschema-processtokensidtype-principaltype-element.md)        | [<span data-ttu-id="15299-120">**processTokenSidType**</span><span class="sxs-lookup"><span data-stu-id="15299-120">**processTokenSidType**</span></span>](taskschedulerschema-processtokensidtype-simpletype.md)        | <span data-ttu-id="15299-121">Especifica os tipos de SID (identificador de segurança do processo) que podem ser usados pelas tarefas.</span><span class="sxs-lookup"><span data-stu-id="15299-121">Specifies the types of process security identifier (SID) that can be used by tasks.</span></span><br/>                              |
| [<span data-ttu-id="15299-122">**RequiredPrivileges**</span><span class="sxs-lookup"><span data-stu-id="15299-122">**RequiredPrivileges**</span></span>](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [<span data-ttu-id="15299-123">**requiredPrivilegesType**</span><span class="sxs-lookup"><span data-stu-id="15299-123">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md) | <span data-ttu-id="15299-124">Especifica os privilégios necessários para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="15299-124">Specifies the required privileges to run the task.</span></span><br/>                                                               |
| [<span data-ttu-id="15299-125">**RunLevel**</span><span class="sxs-lookup"><span data-stu-id="15299-125">**RunLevel**</span></span>](taskschedulerschema-runlevel-principaltype-element.md)                              | [<span data-ttu-id="15299-126">**runLevelType**</span><span class="sxs-lookup"><span data-stu-id="15299-126">**runLevelType**</span></span>](taskschedulerschema-runleveltype-simpletype.md)                      | <span data-ttu-id="15299-127">Especifica o nível de permissão em que a tarefa será executada.</span><span class="sxs-lookup"><span data-stu-id="15299-127">Specifies the permission level that the task will be run at.</span></span><br/>                                                     |
| [<span data-ttu-id="15299-128">**ID**</span><span class="sxs-lookup"><span data-stu-id="15299-128">**UserId**</span></span>](taskschedulerschema-userid-principaltype-element.md)                                  | [<span data-ttu-id="15299-129">**não vazio**</span><span class="sxs-lookup"><span data-stu-id="15299-129">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                  | <span data-ttu-id="15299-130">Especifica o identificador de usuário que é necessário para executar tarefas associadas à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="15299-130">Specifies the user identifier that is required to run tasks that are associated with the principal.</span></span><br/>              |



## <a name="attributes"></a><span data-ttu-id="15299-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="15299-131">Attributes</span></span>



| <span data-ttu-id="15299-132">Nome</span><span class="sxs-lookup"><span data-stu-id="15299-132">Name</span></span> | <span data-ttu-id="15299-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="15299-133">Type</span></span> | <span data-ttu-id="15299-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="15299-134">Description</span></span>                                           |
|------|------|-------------------------------------------------------|
| <span data-ttu-id="15299-135">id</span><span class="sxs-lookup"><span data-stu-id="15299-135">id</span></span>   | <span data-ttu-id="15299-136">ID</span><span class="sxs-lookup"><span data-stu-id="15299-136">ID</span></span>   | <span data-ttu-id="15299-137">Especifica o identificador da entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="15299-137">Specifies the identifier of the principal.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="15299-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15299-138">Requirements</span></span>



| <span data-ttu-id="15299-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="15299-139">Requirement</span></span> | <span data-ttu-id="15299-140">Valor</span><span class="sxs-lookup"><span data-stu-id="15299-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="15299-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15299-141">Minimum supported client</span></span><br/> | <span data-ttu-id="15299-142">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="15299-142">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="15299-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15299-143">Minimum supported server</span></span><br/> | <span data-ttu-id="15299-144">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="15299-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="15299-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="15299-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15299-146">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="15299-146">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="15299-147">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="15299-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





