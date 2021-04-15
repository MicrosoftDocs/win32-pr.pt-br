---
title: Permitido para autenticar à direita estendida
description: Os controles direitos de acesso de controle que podem ser autenticados em um determinado computador ou serviço.
ms.assetid: 265e6240-0fb5-4037-8c66-05fadc646100
ms.tgt_platform: multiple
keywords:
- Permitido-para autenticar o esquema do AD estendido à direita
topic_type:
- apiref
api_name:
- Allowed-To-Authenticate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2fca1b6f4670fd340170ed5cfd1f0160d61945
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456305"
---
# <a name="allowed-to-authenticate-extended-right"></a><span data-ttu-id="b8022-104">Permitido para autenticar à direita estendida</span><span class="sxs-lookup"><span data-stu-id="b8022-104">Allowed-To-Authenticate extended right</span></span>

<span data-ttu-id="b8022-105">Os controles direitos de acesso de controle que podem ser autenticados em um determinado computador ou serviço.</span><span class="sxs-lookup"><span data-stu-id="b8022-105">The control access right controls who can authenticate to a particular computer or service.</span></span> <span data-ttu-id="b8022-106">Basicamente, ele reside em objetos de computador, usuário e InetOrgPerson.</span><span class="sxs-lookup"><span data-stu-id="b8022-106">It basically lives on computer, user, and InetOrgPerson objects.</span></span> <span data-ttu-id="b8022-107">Ele também será aplicável no objeto de domínio se o acesso for permitido para todo o domínio.</span><span class="sxs-lookup"><span data-stu-id="b8022-107">It is also applicable on the domain object if access is allowed for the entire domain.</span></span> <span data-ttu-id="b8022-108">Ele pode ser aplicado a UOs para permitir que os usuários possam definir ACEs herdáveis em UOs que contenham um conjunto de objetos de usuário ou computador.</span><span class="sxs-lookup"><span data-stu-id="b8022-108">It can be applied to OUs to permit users to be able to set inheritable ACEs on OUs that contain a set of user or computer objects.</span></span>



| <span data-ttu-id="b8022-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8022-109">Entry</span></span> | <span data-ttu-id="b8022-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b8022-110">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="b8022-111">CN</span><span class="sxs-lookup"><span data-stu-id="b8022-111">CN</span></span>           | <span data-ttu-id="b8022-112">Permitido para autenticação</span><span class="sxs-lookup"><span data-stu-id="b8022-112">Allowed-To-Authenticate</span></span>              |
| <span data-ttu-id="b8022-113">Display-Name</span><span class="sxs-lookup"><span data-stu-id="b8022-113">Display-Name</span></span> | <span data-ttu-id="b8022-114">Permissão para autenticar</span><span class="sxs-lookup"><span data-stu-id="b8022-114">Allowed to Authenticate</span></span>              |
| <span data-ttu-id="b8022-115">GUID de direitos</span><span class="sxs-lookup"><span data-stu-id="b8022-115">Rights-GUID</span></span>  | <span data-ttu-id="b8022-116">68b1d179-0d15-4d4f-ab71-46152e79a7bc</span><span class="sxs-lookup"><span data-stu-id="b8022-116">68b1d179-0d15-4d4f-ab71-46152e79a7bc</span></span> |



## <a name="implementations"></a><span data-ttu-id="b8022-117">Implementações</span><span class="sxs-lookup"><span data-stu-id="b8022-117">Implementations</span></span>

-   [<span data-ttu-id="b8022-118">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b8022-118">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b8022-119">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b8022-119">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b8022-120">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b8022-120">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b8022-121">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b8022-121">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b8022-122">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b8022-122">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b8022-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8022-123">Windows Server 2003</span></span>



| <span data-ttu-id="b8022-124">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8022-124">Entry</span></span> | <span data-ttu-id="b8022-125">Valor</span><span class="sxs-lookup"><span data-stu-id="b8022-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8022-126">Applies-To</span><span class="sxs-lookup"><span data-stu-id="b8022-126">Applies-To</span></span>              | [<span data-ttu-id="b8022-127">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b8022-127">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b8022-128">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="b8022-128">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="b8022-129">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="b8022-129">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="b8022-130">Localização-exibição-ID</span><span class="sxs-lookup"><span data-stu-id="b8022-130">Localization-Display-ID</span></span> | <span data-ttu-id="b8022-131">65</span><span class="sxs-lookup"><span data-stu-id="b8022-131">65</span></span>                                                                                                                              |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b8022-132">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b8022-132">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b8022-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8022-133">Entry</span></span> | <span data-ttu-id="b8022-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b8022-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8022-135">Applies-To</span><span class="sxs-lookup"><span data-stu-id="b8022-135">Applies-To</span></span>              | [<span data-ttu-id="b8022-136">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b8022-136">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b8022-137">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="b8022-137">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="b8022-138">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="b8022-138">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="b8022-139">Localização-exibição-ID</span><span class="sxs-lookup"><span data-stu-id="b8022-139">Localization-Display-ID</span></span> | <span data-ttu-id="b8022-140">65</span><span class="sxs-lookup"><span data-stu-id="b8022-140">65</span></span>                                                                                                                              |



## <a name="windows-server-2008"></a><span data-ttu-id="b8022-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8022-141">Windows Server 2008</span></span>



| <span data-ttu-id="b8022-142">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8022-142">Entry</span></span> | <span data-ttu-id="b8022-143">Valor</span><span class="sxs-lookup"><span data-stu-id="b8022-143">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8022-144">Applies-To</span><span class="sxs-lookup"><span data-stu-id="b8022-144">Applies-To</span></span>              | [<span data-ttu-id="b8022-145">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b8022-145">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b8022-146">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="b8022-146">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="b8022-147">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="b8022-147">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="b8022-148">Localização-exibição-ID</span><span class="sxs-lookup"><span data-stu-id="b8022-148">Localization-Display-ID</span></span> | <span data-ttu-id="b8022-149">65</span><span class="sxs-lookup"><span data-stu-id="b8022-149">65</span></span>                                                                                                                              |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b8022-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8022-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b8022-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8022-151">Entry</span></span> | <span data-ttu-id="b8022-152">Valor</span><span class="sxs-lookup"><span data-stu-id="b8022-152">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8022-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="b8022-153">Applies-To</span></span>              | [<span data-ttu-id="b8022-154">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b8022-154">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b8022-155">**Conta de serviço do MS-DS-Managed-Service**</span><span class="sxs-lookup"><span data-stu-id="b8022-155">**ms-DS-Managed-Service-Account**</span></span>](c-msds-managedserviceaccount.md)<br/> [<span data-ttu-id="b8022-156">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="b8022-156">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="b8022-157">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="b8022-157">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="b8022-158">Localização-exibição-ID</span><span class="sxs-lookup"><span data-stu-id="b8022-158">Localization-Display-ID</span></span> | <span data-ttu-id="b8022-159">65</span><span class="sxs-lookup"><span data-stu-id="b8022-159">65</span></span>                                                                                                                                                                                                               |



## <a name="windows-server-2012"></a><span data-ttu-id="b8022-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8022-160">Windows Server 2012</span></span>



| <span data-ttu-id="b8022-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8022-161">Entry</span></span> | <span data-ttu-id="b8022-162">Valor</span><span class="sxs-lookup"><span data-stu-id="b8022-162">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8022-163">Applies-To</span><span class="sxs-lookup"><span data-stu-id="b8022-163">Applies-To</span></span>              | [<span data-ttu-id="b8022-164">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b8022-164">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b8022-165">**Conta de serviço do MS-DS-Managed-Service**</span><span class="sxs-lookup"><span data-stu-id="b8022-165">**ms-DS-Managed-Service-Account**</span></span>](c-msds-managedserviceaccount.md)<br/> [<span data-ttu-id="b8022-166">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="b8022-166">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="b8022-167">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="b8022-167">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="b8022-168">Localização-exibição-ID</span><span class="sxs-lookup"><span data-stu-id="b8022-168">Localization-Display-ID</span></span> | <span data-ttu-id="b8022-169">65</span><span class="sxs-lookup"><span data-stu-id="b8022-169">65</span></span>                                                                                                                                                                                                               |



 

 





