---
title: ms-DS-supported-atributo de tipos de criptografia
description: Os algoritmos de criptografia com suporte do usuário, computador ou contas de confiança. Observe que o KDC usa essas informações ao gerar um tíquete de serviço para essa conta.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- ms-DS-supported-tipo de criptografia-esquema do AD Schema
- atributo msDS-SupportedEncryptionTypes do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab16959d1f1cd4405cb661a6026f3734a134f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105769103"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a><span data-ttu-id="32e31-105">ms-DS-supported-atributo de tipos de criptografia</span><span class="sxs-lookup"><span data-stu-id="32e31-105">ms-DS-Supported-Encryption-Types attribute</span></span>

<span data-ttu-id="32e31-106">Os algoritmos de criptografia com suporte do usuário, computador ou contas de confiança.</span><span class="sxs-lookup"><span data-stu-id="32e31-106">The encryption algorithms supported by user, computer or trust accounts.</span></span>

> [!Note]  
> <span data-ttu-id="32e31-107">O KDC usa essas informações ao gerar um tíquete de serviço para essa conta.</span><span class="sxs-lookup"><span data-stu-id="32e31-107">The KDC uses this information while generating a service ticket for this account.</span></span> <span data-ttu-id="32e31-108">Os serviços e computadores podem atualizar automaticamente esse atributo em suas respectivas contas no Active Directory e, portanto, precisam de acesso de gravação a esse atributo.</span><span class="sxs-lookup"><span data-stu-id="32e31-108">Services and Computers can automatically update this attribute on their respective accounts in Active Directory, and therefore need write access to this attribute.</span></span>

 



| <span data-ttu-id="32e31-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="32e31-109">Entry</span></span> | <span data-ttu-id="32e31-110">Valor</span><span class="sxs-lookup"><span data-stu-id="32e31-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="32e31-111">CN</span><span class="sxs-lookup"><span data-stu-id="32e31-111">CN</span></span>                | <span data-ttu-id="32e31-112">ms-DS-supported-tipos de criptografia</span><span class="sxs-lookup"><span data-stu-id="32e31-112">ms-DS-Supported-Encryption-Types</span></span>     |
| <span data-ttu-id="32e31-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="32e31-113">Ldap-Display-Name</span></span> | <span data-ttu-id="32e31-114">msDS-SupportedEncryptionTypes</span><span class="sxs-lookup"><span data-stu-id="32e31-114">msDS-SupportedEncryptionTypes</span></span>        |
| <span data-ttu-id="32e31-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="32e31-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="32e31-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="32e31-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="32e31-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="32e31-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="32e31-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="32e31-118">Attribute-Id</span></span>      | <span data-ttu-id="32e31-119">1.2.840.113556.1.4.1963</span><span class="sxs-lookup"><span data-stu-id="32e31-119">1.2.840.113556.1.4.1963</span></span>              |
| <span data-ttu-id="32e31-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="32e31-120">System-Id-Guid</span></span>    | <span data-ttu-id="32e31-121">20119867-1d04-4ab7-9371-cfc3d5df0afd</span><span class="sxs-lookup"><span data-stu-id="32e31-121">20119867-1d04-4ab7-9371-cfc3d5df0afd</span></span> |
| <span data-ttu-id="32e31-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="32e31-122">Syntax</span></span>            | [<span data-ttu-id="32e31-123">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="32e31-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="32e31-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="32e31-124">Implementations</span></span>

-   [<span data-ttu-id="32e31-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="32e31-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="32e31-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="32e31-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="32e31-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="32e31-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="32e31-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32e31-128">Windows Server 2008</span></span>



| <span data-ttu-id="32e31-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="32e31-129">Entry</span></span> | <span data-ttu-id="32e31-130">Valor</span><span class="sxs-lookup"><span data-stu-id="32e31-130">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32e31-131">ID do link</span><span class="sxs-lookup"><span data-stu-id="32e31-131">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="32e31-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32e31-132">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="32e31-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="32e31-133">System-Only</span></span>            | <span data-ttu-id="32e31-134">Falso</span><span class="sxs-lookup"><span data-stu-id="32e31-134">False</span></span>                                                                                  |
| <span data-ttu-id="32e31-135">É de valor único</span><span class="sxs-lookup"><span data-stu-id="32e31-135">Is-Single-Valued</span></span>       | <span data-ttu-id="32e31-136">True</span><span class="sxs-lookup"><span data-stu-id="32e31-136">True</span></span>                                                                                   |
| <span data-ttu-id="32e31-137">É indexado</span><span class="sxs-lookup"><span data-stu-id="32e31-137">Is Indexed</span></span>             | <span data-ttu-id="32e31-138">Falso</span><span class="sxs-lookup"><span data-stu-id="32e31-138">False</span></span>                                                                                  |
| <span data-ttu-id="32e31-139">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="32e31-139">In Global Catalog</span></span>      | <span data-ttu-id="32e31-140">Falso</span><span class="sxs-lookup"><span data-stu-id="32e31-140">False</span></span>                                                                                  |
| <span data-ttu-id="32e31-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32e31-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="32e31-142">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="32e31-142">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="32e31-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32e31-143">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="32e31-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32e31-144">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="32e31-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32e31-145">Search-Flags</span></span>           | <span data-ttu-id="32e31-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32e31-146">0x00000000</span></span>                                                                             |
| <span data-ttu-id="32e31-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32e31-147">System-Flags</span></span>           | <span data-ttu-id="32e31-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32e31-148">0x00000010</span></span>                                                                             |
| <span data-ttu-id="32e31-149">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="32e31-149">Classes used in</span></span>        | [<span data-ttu-id="32e31-150">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="32e31-150">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="32e31-151">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="32e31-151">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="32e31-152">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="32e31-152">Windows Server 2008 R2</span></span>



| <span data-ttu-id="32e31-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="32e31-153">Entry</span></span> | <span data-ttu-id="32e31-154">Valor</span><span class="sxs-lookup"><span data-stu-id="32e31-154">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32e31-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="32e31-155">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="32e31-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32e31-156">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="32e31-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="32e31-157">System-Only</span></span>            | <span data-ttu-id="32e31-158">Falso</span><span class="sxs-lookup"><span data-stu-id="32e31-158">False</span></span>                                                                                  |
| <span data-ttu-id="32e31-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="32e31-159">Is-Single-Valued</span></span>       | <span data-ttu-id="32e31-160">True</span><span class="sxs-lookup"><span data-stu-id="32e31-160">True</span></span>                                                                                   |
| <span data-ttu-id="32e31-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="32e31-161">Is Indexed</span></span>             | <span data-ttu-id="32e31-162">Falso</span><span class="sxs-lookup"><span data-stu-id="32e31-162">False</span></span>                                                                                  |
| <span data-ttu-id="32e31-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="32e31-163">In Global Catalog</span></span>      | <span data-ttu-id="32e31-164">Falso</span><span class="sxs-lookup"><span data-stu-id="32e31-164">False</span></span>                                                                                  |
| <span data-ttu-id="32e31-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32e31-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="32e31-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="32e31-166">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="32e31-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32e31-167">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="32e31-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32e31-168">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="32e31-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32e31-169">Search-Flags</span></span>           | <span data-ttu-id="32e31-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32e31-170">0x00000000</span></span>                                                                             |
| <span data-ttu-id="32e31-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32e31-171">System-Flags</span></span>           | <span data-ttu-id="32e31-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32e31-172">0x00000010</span></span>                                                                             |
| <span data-ttu-id="32e31-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="32e31-173">Classes used in</span></span>        | [<span data-ttu-id="32e31-174">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="32e31-174">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="32e31-175">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="32e31-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="32e31-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="32e31-176">Windows Server 2012</span></span>



| <span data-ttu-id="32e31-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="32e31-177">Entry</span></span> | <span data-ttu-id="32e31-178">Valor</span><span class="sxs-lookup"><span data-stu-id="32e31-178">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32e31-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="32e31-179">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="32e31-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32e31-180">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="32e31-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="32e31-181">System-Only</span></span>            | <span data-ttu-id="32e31-182">Falso</span><span class="sxs-lookup"><span data-stu-id="32e31-182">False</span></span>                                                                                  |
| <span data-ttu-id="32e31-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="32e31-183">Is-Single-Valued</span></span>       | <span data-ttu-id="32e31-184">True</span><span class="sxs-lookup"><span data-stu-id="32e31-184">True</span></span>                                                                                   |
| <span data-ttu-id="32e31-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="32e31-185">Is Indexed</span></span>             | <span data-ttu-id="32e31-186">Falso</span><span class="sxs-lookup"><span data-stu-id="32e31-186">False</span></span>                                                                                  |
| <span data-ttu-id="32e31-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="32e31-187">In Global Catalog</span></span>      | <span data-ttu-id="32e31-188">Falso</span><span class="sxs-lookup"><span data-stu-id="32e31-188">False</span></span>                                                                                  |
| <span data-ttu-id="32e31-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32e31-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="32e31-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="32e31-190">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="32e31-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32e31-191">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="32e31-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32e31-192">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="32e31-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32e31-193">Search-Flags</span></span>           | <span data-ttu-id="32e31-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32e31-194">0x00000000</span></span>                                                                             |
| <span data-ttu-id="32e31-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32e31-195">System-Flags</span></span>           | <span data-ttu-id="32e31-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32e31-196">0x00000010</span></span>                                                                             |
| <span data-ttu-id="32e31-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="32e31-197">Classes used in</span></span>        | [<span data-ttu-id="32e31-198">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="32e31-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="32e31-199">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="32e31-199">**User**</span></span>](c-user.md)<br/> |



 

 





