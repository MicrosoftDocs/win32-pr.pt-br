---
title: Mapeamento de interface do usuário de objeto de computador
description: As tabelas a seguir listam os elementos das folhas de propriedades de objeto de computador no snap-in Active Directory usuários e computadores.
ms.assetid: e2a7a42d-e854-43fc-a36b-f3031c1685a7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2a2b3ed4ec8cbf3c1af59e024fc5e04bc68ae8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640428"
---
# <a name="computer-object-user-interface-mapping"></a><span data-ttu-id="6662a-103">Mapeamento de interface do usuário de objeto de computador</span><span class="sxs-lookup"><span data-stu-id="6662a-103">Computer Object User Interface Mapping</span></span>

<span data-ttu-id="6662a-104">As tabelas a seguir listam os elementos das folhas de propriedades de objeto de computador no snap-in Active Directory usuários e computadores.</span><span class="sxs-lookup"><span data-stu-id="6662a-104">The following tables list elements of the Computer object property sheets in the Active Directory Users and Computers snap-in.</span></span>

## <a name="general-property-sheet"></a><span data-ttu-id="6662a-105">Folha de propriedades geral</span><span class="sxs-lookup"><span data-stu-id="6662a-105">General Property Sheet</span></span>

<span data-ttu-id="6662a-106">A tabela a seguir lista os rótulos de interface do usuário da folha de propriedades **geral** .</span><span class="sxs-lookup"><span data-stu-id="6662a-106">The following table lists the UI labels of the **General** property sheet.</span></span>



| <span data-ttu-id="6662a-107">Rótulo da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="6662a-107">UI label</span></span>                         | <span data-ttu-id="6662a-108">Active Directory Domain Services atributo</span><span class="sxs-lookup"><span data-stu-id="6662a-108">Active Directory Domain Services attribute</span></span> | <span data-ttu-id="6662a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="6662a-109">Comments</span></span>                                         |
|----------------------------------|--------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="6662a-110">Nome do computador (anterior ao Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="6662a-110">Computer Name (pre-Windows 2000)</span></span> | <span data-ttu-id="6662a-111">sAMAccountName</span><span class="sxs-lookup"><span data-stu-id="6662a-111">sAMAccountName</span></span>                             |                                                  |
| <span data-ttu-id="6662a-112">Nome DNS</span><span class="sxs-lookup"><span data-stu-id="6662a-112">DNS Name</span></span>                         | <span data-ttu-id="6662a-113">dNSHostName</span><span class="sxs-lookup"><span data-stu-id="6662a-113">dNSHostName</span></span>                                |                                                  |
| <span data-ttu-id="6662a-114">Função</span><span class="sxs-lookup"><span data-stu-id="6662a-114">Role</span></span>                             | <span data-ttu-id="6662a-115">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="6662a-115">userAccountControl</span></span>                         | <span data-ttu-id="6662a-116">Alterna um bit no bitmask userAccountControl.</span><span class="sxs-lookup"><span data-stu-id="6662a-116">Toggles a bit in the userAccountControl bitmask.</span></span> |
| <span data-ttu-id="6662a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="6662a-117">Description</span></span>                      | <span data-ttu-id="6662a-118">descrição</span><span class="sxs-lookup"><span data-stu-id="6662a-118">description</span></span>                                |                                                  |
| <span data-ttu-id="6662a-119">Confiar no computador para delegação</span><span class="sxs-lookup"><span data-stu-id="6662a-119">Trust Computer for delegation</span></span>    | <span data-ttu-id="6662a-120">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="6662a-120">userAccountControl</span></span>                         | <span data-ttu-id="6662a-121">Alterna um bit no bitmask userAccountControl.</span><span class="sxs-lookup"><span data-stu-id="6662a-121">Toggles a bit in the userAccountControl bitmask.</span></span> |



 

## <a name="location-property-sheet"></a><span data-ttu-id="6662a-122">Folha de propriedades de localização</span><span class="sxs-lookup"><span data-stu-id="6662a-122">Location Property Sheet</span></span>

<span data-ttu-id="6662a-123">A tabela a seguir lista os rótulos de interface do usuário da folha de propriedades **local** .</span><span class="sxs-lookup"><span data-stu-id="6662a-123">The following table lists the UI labels of the **Location** property sheet.</span></span>



| <span data-ttu-id="6662a-124">Rótulo da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="6662a-124">UI label</span></span> | <span data-ttu-id="6662a-125">Active Directory Domain Services atributo</span><span class="sxs-lookup"><span data-stu-id="6662a-125">Active Directory Domain Services attribute</span></span> |
|----------|--------------------------------------------|
| <span data-ttu-id="6662a-126">Local</span><span class="sxs-lookup"><span data-stu-id="6662a-126">Location</span></span> | <span data-ttu-id="6662a-127">local</span><span class="sxs-lookup"><span data-stu-id="6662a-127">location</span></span>                                   |



 

## <a name="member-of-property-sheet"></a><span data-ttu-id="6662a-128">Membro da folha de propriedades</span><span class="sxs-lookup"><span data-stu-id="6662a-128">Member Of Property Sheet</span></span>

<span data-ttu-id="6662a-129">A tabela a seguir lista os rótulos de interface de usuário do **membro da folha de** Propriedades.</span><span class="sxs-lookup"><span data-stu-id="6662a-129">The following table lists the UI labels of the **Member Of** property sheet.</span></span>



| <span data-ttu-id="6662a-130">Rótulo da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="6662a-130">UI label</span></span>          | <span data-ttu-id="6662a-131">Active Directory Domain Services atributo</span><span class="sxs-lookup"><span data-stu-id="6662a-131">Active Directory Domain Services attribute</span></span> | <span data-ttu-id="6662a-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="6662a-132">Comments</span></span>                                                                                                                                                                   |
|-------------------|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6662a-133">Membro de</span><span class="sxs-lookup"><span data-stu-id="6662a-133">Member of</span></span>         | <span data-ttu-id="6662a-134">memberOf</span><span class="sxs-lookup"><span data-stu-id="6662a-134">memberOf</span></span>                                   | <span data-ttu-id="6662a-135">Inclui todos os grupos na lista de interface do usuário, exceto o grupo primário, que é representado no anúncio por meio do atributo [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) .</span><span class="sxs-lookup"><span data-stu-id="6662a-135">Includes all of the groups in the UI list, except the primary group, which is represented in the AD through the [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) attribute.</span></span> |
| <span data-ttu-id="6662a-136">Definir grupo primário</span><span class="sxs-lookup"><span data-stu-id="6662a-136">Set Primary Group</span></span> | <span data-ttu-id="6662a-137">primaryGroupID</span><span class="sxs-lookup"><span data-stu-id="6662a-137">primaryGroupID</span></span>                             | <span data-ttu-id="6662a-138">LDAP: vinculado a [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) do grupo primário.</span><span class="sxs-lookup"><span data-stu-id="6662a-138">LDAP: Tied to [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) of the primary group.</span></span>                                                                                  |



 

## <a name="operating-system-property-sheet"></a><span data-ttu-id="6662a-139">Folha de propriedades do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="6662a-139">Operating System Property Sheet</span></span>

<span data-ttu-id="6662a-140">A tabela a seguir lista os rótulos de interface do usuário da folha de propriedades do **sistema operacional** .</span><span class="sxs-lookup"><span data-stu-id="6662a-140">The following table lists the UI labels of the **Operating System** property sheet.</span></span>



| <span data-ttu-id="6662a-141">Rótulo da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="6662a-141">UI label</span></span>     | <span data-ttu-id="6662a-142">Active Directory Domain Services atributo</span><span class="sxs-lookup"><span data-stu-id="6662a-142">Active Directory Domain Services attribute</span></span> |
|--------------|--------------------------------------------|
| <span data-ttu-id="6662a-143">Nome</span><span class="sxs-lookup"><span data-stu-id="6662a-143">Name</span></span>         | <span data-ttu-id="6662a-144">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="6662a-144">operatingSystem</span></span>                            |
| <span data-ttu-id="6662a-145">Versão</span><span class="sxs-lookup"><span data-stu-id="6662a-145">Version</span></span>      | <span data-ttu-id="6662a-146">operatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="6662a-146">operatingSystemVersion</span></span>                     |
| <span data-ttu-id="6662a-147">Service Pack</span><span class="sxs-lookup"><span data-stu-id="6662a-147">Service Pack</span></span> | <span data-ttu-id="6662a-148">operatingSystemServicePack</span><span class="sxs-lookup"><span data-stu-id="6662a-148">operatingSystemServicePack</span></span>                 |



 

 

 