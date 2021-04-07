---
title: atributo MS-TS-Profile-Path
description: Caminho do perfil de serviços de terminal especifica um caminho de perfil móvel ou obrigatório a ser usado quando o usuário fizer logon no servidor de terminal. O caminho do perfil está no seguinte formato de caminho de rede \\ \\ ServerName \\ ProfilesFolderName \\ nome de usuário.
ms.assetid: 9b13f91d-c3ee-4862-800c-fda831dce859
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo MS-TS-Profile-Path
- Esquema de AD do atributo msTSProfilePath
topic_type:
- apiref
api_name:
- ms-TS-Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67243c2ef588bd1470a50417c0948b1ea4ea7fa9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919455"
---
# <a name="ms-ts-profile-path-attribute"></a><span data-ttu-id="52890-106">atributo MS-TS-Profile-Path</span><span class="sxs-lookup"><span data-stu-id="52890-106">ms-TS-Profile-Path attribute</span></span>

<span data-ttu-id="52890-107">Caminho do perfil de serviços de terminal especifica um caminho de perfil móvel ou obrigatório a ser usado quando o usuário fizer logon no servidor de terminal.</span><span class="sxs-lookup"><span data-stu-id="52890-107">Terminal Services Profile Path specifies a roaming or mandatory profile path to use when the user logs on to the terminal server.</span></span> <span data-ttu-id="52890-108">O caminho do perfil está no seguinte formato de caminho de rede: **\\\\** _nomedoservidor_ *_\\_* _ProfilesFolderName_ *_\\_* _username_.</span><span class="sxs-lookup"><span data-stu-id="52890-108">The profile path is in the following network path format: **\\\\**_ServerName_*_\\_*_ProfilesFolderName_*_\\_*_UserName_.</span></span>



| <span data-ttu-id="52890-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="52890-109">Entry</span></span> | <span data-ttu-id="52890-110">Valor</span><span class="sxs-lookup"><span data-stu-id="52890-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="52890-111">CN</span><span class="sxs-lookup"><span data-stu-id="52890-111">CN</span></span>                | <span data-ttu-id="52890-112">MS-TS-Profile-Path</span><span class="sxs-lookup"><span data-stu-id="52890-112">ms-TS-Profile-Path</span></span>                          |
| <span data-ttu-id="52890-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="52890-113">Ldap-Display-Name</span></span> | <span data-ttu-id="52890-114">msTSProfilePath</span><span class="sxs-lookup"><span data-stu-id="52890-114">msTSProfilePath</span></span>                             |
| <span data-ttu-id="52890-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="52890-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="52890-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="52890-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="52890-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="52890-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="52890-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="52890-118">Attribute-Id</span></span>      | <span data-ttu-id="52890-119">1.2.840.113556.1.4.1976</span><span class="sxs-lookup"><span data-stu-id="52890-119">1.2.840.113556.1.4.1976</span></span>                     |
| <span data-ttu-id="52890-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="52890-120">System-Id-Guid</span></span>    | <span data-ttu-id="52890-121">e65c30db-316c-4060-a3a0-387b083f09cd</span><span class="sxs-lookup"><span data-stu-id="52890-121">e65c30db-316c-4060-a3a0-387b083f09cd</span></span>        |
| <span data-ttu-id="52890-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="52890-122">Syntax</span></span>            | [<span data-ttu-id="52890-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="52890-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="52890-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="52890-124">Implementations</span></span>

-   [<span data-ttu-id="52890-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="52890-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="52890-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="52890-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="52890-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="52890-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="52890-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52890-128">Windows Server 2008</span></span>



| <span data-ttu-id="52890-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="52890-129">Entry</span></span> | <span data-ttu-id="52890-130">Valor</span><span class="sxs-lookup"><span data-stu-id="52890-130">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="52890-131">ID do link</span><span class="sxs-lookup"><span data-stu-id="52890-131">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="52890-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52890-132">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="52890-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="52890-133">System-Only</span></span>            | <span data-ttu-id="52890-134">Falso</span><span class="sxs-lookup"><span data-stu-id="52890-134">False</span></span>                             |
| <span data-ttu-id="52890-135">É de valor único</span><span class="sxs-lookup"><span data-stu-id="52890-135">Is-Single-Valued</span></span>       | <span data-ttu-id="52890-136">True</span><span class="sxs-lookup"><span data-stu-id="52890-136">True</span></span>                              |
| <span data-ttu-id="52890-137">É indexado</span><span class="sxs-lookup"><span data-stu-id="52890-137">Is Indexed</span></span>             | <span data-ttu-id="52890-138">Falso</span><span class="sxs-lookup"><span data-stu-id="52890-138">False</span></span>                             |
| <span data-ttu-id="52890-139">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="52890-139">In Global Catalog</span></span>      | <span data-ttu-id="52890-140">Falso</span><span class="sxs-lookup"><span data-stu-id="52890-140">False</span></span>                             |
| <span data-ttu-id="52890-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="52890-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="52890-142">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="52890-142">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="52890-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52890-143">Range-Lower</span></span>            | <span data-ttu-id="52890-144">0</span><span class="sxs-lookup"><span data-stu-id="52890-144">0</span></span>                                 |
| <span data-ttu-id="52890-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52890-145">Range-Upper</span></span>            | <span data-ttu-id="52890-146">32767</span><span class="sxs-lookup"><span data-stu-id="52890-146">32767</span></span>                             |
| <span data-ttu-id="52890-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52890-147">Search-Flags</span></span>           | <span data-ttu-id="52890-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52890-148">0x00000000</span></span>                        |
| <span data-ttu-id="52890-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52890-149">System-Flags</span></span>           | <span data-ttu-id="52890-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="52890-150">0x00000010</span></span>                        |
| <span data-ttu-id="52890-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="52890-151">Classes used in</span></span>        | [<span data-ttu-id="52890-152">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="52890-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="52890-153">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="52890-153">Windows Server 2008 R2</span></span>



| <span data-ttu-id="52890-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="52890-154">Entry</span></span> | <span data-ttu-id="52890-155">Valor</span><span class="sxs-lookup"><span data-stu-id="52890-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="52890-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="52890-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="52890-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52890-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="52890-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="52890-158">System-Only</span></span>            | <span data-ttu-id="52890-159">Falso</span><span class="sxs-lookup"><span data-stu-id="52890-159">False</span></span>                             |
| <span data-ttu-id="52890-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="52890-160">Is-Single-Valued</span></span>       | <span data-ttu-id="52890-161">True</span><span class="sxs-lookup"><span data-stu-id="52890-161">True</span></span>                              |
| <span data-ttu-id="52890-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="52890-162">Is Indexed</span></span>             | <span data-ttu-id="52890-163">Falso</span><span class="sxs-lookup"><span data-stu-id="52890-163">False</span></span>                             |
| <span data-ttu-id="52890-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="52890-164">In Global Catalog</span></span>      | <span data-ttu-id="52890-165">Falso</span><span class="sxs-lookup"><span data-stu-id="52890-165">False</span></span>                             |
| <span data-ttu-id="52890-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="52890-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="52890-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="52890-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="52890-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52890-168">Range-Lower</span></span>            | <span data-ttu-id="52890-169">0</span><span class="sxs-lookup"><span data-stu-id="52890-169">0</span></span>                                 |
| <span data-ttu-id="52890-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52890-170">Range-Upper</span></span>            | <span data-ttu-id="52890-171">32767</span><span class="sxs-lookup"><span data-stu-id="52890-171">32767</span></span>                             |
| <span data-ttu-id="52890-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52890-172">Search-Flags</span></span>           | <span data-ttu-id="52890-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52890-173">0x00000000</span></span>                        |
| <span data-ttu-id="52890-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52890-174">System-Flags</span></span>           | <span data-ttu-id="52890-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="52890-175">0x00000010</span></span>                        |
| <span data-ttu-id="52890-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="52890-176">Classes used in</span></span>        | [<span data-ttu-id="52890-177">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="52890-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="52890-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="52890-178">Windows Server 2012</span></span>



| <span data-ttu-id="52890-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="52890-179">Entry</span></span> | <span data-ttu-id="52890-180">Valor</span><span class="sxs-lookup"><span data-stu-id="52890-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="52890-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="52890-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="52890-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52890-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="52890-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="52890-183">System-Only</span></span>            | <span data-ttu-id="52890-184">Falso</span><span class="sxs-lookup"><span data-stu-id="52890-184">False</span></span>                             |
| <span data-ttu-id="52890-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="52890-185">Is-Single-Valued</span></span>       | <span data-ttu-id="52890-186">True</span><span class="sxs-lookup"><span data-stu-id="52890-186">True</span></span>                              |
| <span data-ttu-id="52890-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="52890-187">Is Indexed</span></span>             | <span data-ttu-id="52890-188">Falso</span><span class="sxs-lookup"><span data-stu-id="52890-188">False</span></span>                             |
| <span data-ttu-id="52890-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="52890-189">In Global Catalog</span></span>      | <span data-ttu-id="52890-190">Falso</span><span class="sxs-lookup"><span data-stu-id="52890-190">False</span></span>                             |
| <span data-ttu-id="52890-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="52890-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="52890-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="52890-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="52890-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52890-193">Range-Lower</span></span>            | <span data-ttu-id="52890-194">0</span><span class="sxs-lookup"><span data-stu-id="52890-194">0</span></span>                                 |
| <span data-ttu-id="52890-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52890-195">Range-Upper</span></span>            | <span data-ttu-id="52890-196">32767</span><span class="sxs-lookup"><span data-stu-id="52890-196">32767</span></span>                             |
| <span data-ttu-id="52890-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52890-197">Search-Flags</span></span>           | <span data-ttu-id="52890-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52890-198">0x00000000</span></span>                        |
| <span data-ttu-id="52890-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52890-199">System-Flags</span></span>           | <span data-ttu-id="52890-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="52890-200">0x00000010</span></span>                        |
| <span data-ttu-id="52890-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="52890-201">Classes used in</span></span>        | [<span data-ttu-id="52890-202">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="52890-202">**User**</span></span>](c-user.md)<br/> |



 

 





