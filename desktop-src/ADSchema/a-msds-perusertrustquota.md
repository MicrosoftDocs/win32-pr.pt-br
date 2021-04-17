---
title: Atributo MS-DS-per-user-Trust-quota
description: Usado para impor uma cota por usuário para criar Trusted-Domain objetos que são autorizados pelo direito de acesso de novo controle, criar-entrada-floresta-Trust.
ms.assetid: 3b198b24-5282-4d13-8d35-88f34c11ce94
ms.tgt_platform: multiple
keywords:
- Esquema do AD de atributos do MS-DS-per-user-Trust-quota
- atributo msDS-PerUserTrustQuota do AD Schema
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3bd6ffcac01de8997f806e6aa8a8e3bd6afbb66
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105753023"
---
# <a name="ms-ds-per-user-trust-quota-attribute"></a><span data-ttu-id="69eed-105">Atributo MS-DS-per-user-Trust-quota</span><span class="sxs-lookup"><span data-stu-id="69eed-105">MS-DS-Per-User-Trust-Quota attribute</span></span>

<span data-ttu-id="69eed-106">Usado para impor uma cota por usuário para criar Trusted-Domain objetos que são autorizados pelo direito de acesso de novo controle, criar-entrada-floresta-Trust.</span><span class="sxs-lookup"><span data-stu-id="69eed-106">Used to enforce a per-user quota for creating Trusted-Domain objects that are authorized by the new control access right, Create-Inbound-Forest-Trust.</span></span> <span data-ttu-id="69eed-107">Esse atributo limita o número de objetos Trusted-Domain que podem ser criados por um único usuário não administrador.</span><span class="sxs-lookup"><span data-stu-id="69eed-107">This attribute limits the number of Trusted-Domain objects that can be created by a single non-admin user.</span></span>



| <span data-ttu-id="69eed-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="69eed-108">Entry</span></span> | <span data-ttu-id="69eed-109">Valor</span><span class="sxs-lookup"><span data-stu-id="69eed-109">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="69eed-110">CN</span><span class="sxs-lookup"><span data-stu-id="69eed-110">CN</span></span>                | <span data-ttu-id="69eed-111">MS-DS-por usuário-Trust-quota</span><span class="sxs-lookup"><span data-stu-id="69eed-111">MS-DS-Per-User-Trust-Quota</span></span>                |
| <span data-ttu-id="69eed-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="69eed-112">Ldap-Display-Name</span></span> | <span data-ttu-id="69eed-113">msDS-PerUserTrustQuota</span><span class="sxs-lookup"><span data-stu-id="69eed-113">msDS-PerUserTrustQuota</span></span>                    |
| <span data-ttu-id="69eed-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="69eed-114">Size</span></span>              | \-                                        |
| <span data-ttu-id="69eed-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="69eed-115">Update Privilege</span></span>  | <span data-ttu-id="69eed-116">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="69eed-116">Domain administrator</span></span>                      |
| <span data-ttu-id="69eed-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="69eed-117">Update Frequency</span></span>  | <span data-ttu-id="69eed-118">Na criação da floresta e raramente depois disso.</span><span class="sxs-lookup"><span data-stu-id="69eed-118">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="69eed-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="69eed-119">Attribute-Id</span></span>      | <span data-ttu-id="69eed-120">1.2.840.113556.1.4.1788</span><span class="sxs-lookup"><span data-stu-id="69eed-120">1.2.840.113556.1.4.1788</span></span>                   |
| <span data-ttu-id="69eed-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="69eed-121">System-Id-Guid</span></span>    | <span data-ttu-id="69eed-122">d161adf0-ca24-4993-a3aa-8b2c981302e8</span><span class="sxs-lookup"><span data-stu-id="69eed-122">d161adf0-ca24-4993-a3aa-8b2c981302e8</span></span>      |
| <span data-ttu-id="69eed-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="69eed-123">Syntax</span></span>            | [<span data-ttu-id="69eed-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="69eed-124">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="69eed-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="69eed-125">Implementations</span></span>

-   [<span data-ttu-id="69eed-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="69eed-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="69eed-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="69eed-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="69eed-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="69eed-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="69eed-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="69eed-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="69eed-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="69eed-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="69eed-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69eed-131">Windows Server 2003</span></span>



| <span data-ttu-id="69eed-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="69eed-132">Entry</span></span> | <span data-ttu-id="69eed-133">Valor</span><span class="sxs-lookup"><span data-stu-id="69eed-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69eed-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="69eed-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69eed-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69eed-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69eed-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="69eed-136">System-Only</span></span>            | <span data-ttu-id="69eed-137">Falso</span><span class="sxs-lookup"><span data-stu-id="69eed-137">False</span></span>                                        |
| <span data-ttu-id="69eed-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69eed-138">Is-Single-Valued</span></span>       | <span data-ttu-id="69eed-139">True</span><span class="sxs-lookup"><span data-stu-id="69eed-139">True</span></span>                                         |
| <span data-ttu-id="69eed-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="69eed-140">Is Indexed</span></span>             | <span data-ttu-id="69eed-141">Falso</span><span class="sxs-lookup"><span data-stu-id="69eed-141">False</span></span>                                        |
| <span data-ttu-id="69eed-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69eed-142">In Global Catalog</span></span>      | <span data-ttu-id="69eed-143">Falso</span><span class="sxs-lookup"><span data-stu-id="69eed-143">False</span></span>                                        |
| <span data-ttu-id="69eed-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69eed-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="69eed-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69eed-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69eed-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69eed-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69eed-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69eed-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69eed-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69eed-148">Search-Flags</span></span>           | <span data-ttu-id="69eed-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69eed-149">0x00000000</span></span>                                   |
| <span data-ttu-id="69eed-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69eed-150">System-Flags</span></span>           | <span data-ttu-id="69eed-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69eed-151">0x00000010</span></span>                                   |
| <span data-ttu-id="69eed-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69eed-152">Classes used in</span></span>        | [<span data-ttu-id="69eed-153">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="69eed-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="69eed-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="69eed-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="69eed-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="69eed-155">Entry</span></span> | <span data-ttu-id="69eed-156">Valor</span><span class="sxs-lookup"><span data-stu-id="69eed-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69eed-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="69eed-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69eed-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69eed-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69eed-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="69eed-159">System-Only</span></span>            | <span data-ttu-id="69eed-160">Falso</span><span class="sxs-lookup"><span data-stu-id="69eed-160">False</span></span>                                        |
| <span data-ttu-id="69eed-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69eed-161">Is-Single-Valued</span></span>       | <span data-ttu-id="69eed-162">True</span><span class="sxs-lookup"><span data-stu-id="69eed-162">True</span></span>                                         |
| <span data-ttu-id="69eed-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="69eed-163">Is Indexed</span></span>             | <span data-ttu-id="69eed-164">Falso</span><span class="sxs-lookup"><span data-stu-id="69eed-164">False</span></span>                                        |
| <span data-ttu-id="69eed-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69eed-165">In Global Catalog</span></span>      | <span data-ttu-id="69eed-166">Falso</span><span class="sxs-lookup"><span data-stu-id="69eed-166">False</span></span>                                        |
| <span data-ttu-id="69eed-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69eed-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="69eed-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69eed-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69eed-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69eed-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69eed-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69eed-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69eed-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69eed-171">Search-Flags</span></span>           | <span data-ttu-id="69eed-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69eed-172">0x00000000</span></span>                                   |
| <span data-ttu-id="69eed-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69eed-173">System-Flags</span></span>           | <span data-ttu-id="69eed-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69eed-174">0x00000010</span></span>                                   |
| <span data-ttu-id="69eed-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69eed-175">Classes used in</span></span>        | [<span data-ttu-id="69eed-176">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="69eed-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="69eed-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69eed-177">Windows Server 2008</span></span>



| <span data-ttu-id="69eed-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="69eed-178">Entry</span></span> | <span data-ttu-id="69eed-179">Valor</span><span class="sxs-lookup"><span data-stu-id="69eed-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69eed-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="69eed-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69eed-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69eed-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69eed-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="69eed-182">System-Only</span></span>            | <span data-ttu-id="69eed-183">Falso</span><span class="sxs-lookup"><span data-stu-id="69eed-183">False</span></span>                                        |
| <span data-ttu-id="69eed-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69eed-184">Is-Single-Valued</span></span>       | <span data-ttu-id="69eed-185">True</span><span class="sxs-lookup"><span data-stu-id="69eed-185">True</span></span>                                         |
| <span data-ttu-id="69eed-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="69eed-186">Is Indexed</span></span>             | <span data-ttu-id="69eed-187">Falso</span><span class="sxs-lookup"><span data-stu-id="69eed-187">False</span></span>                                        |
| <span data-ttu-id="69eed-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69eed-188">In Global Catalog</span></span>      | <span data-ttu-id="69eed-189">Falso</span><span class="sxs-lookup"><span data-stu-id="69eed-189">False</span></span>                                        |
| <span data-ttu-id="69eed-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69eed-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="69eed-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69eed-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69eed-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69eed-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69eed-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69eed-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69eed-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69eed-194">Search-Flags</span></span>           | <span data-ttu-id="69eed-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69eed-195">0x00000000</span></span>                                   |
| <span data-ttu-id="69eed-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69eed-196">System-Flags</span></span>           | <span data-ttu-id="69eed-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69eed-197">0x00000010</span></span>                                   |
| <span data-ttu-id="69eed-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69eed-198">Classes used in</span></span>        | [<span data-ttu-id="69eed-199">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="69eed-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="69eed-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69eed-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="69eed-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="69eed-201">Entry</span></span> | <span data-ttu-id="69eed-202">Valor</span><span class="sxs-lookup"><span data-stu-id="69eed-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69eed-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="69eed-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69eed-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69eed-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69eed-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="69eed-205">System-Only</span></span>            | <span data-ttu-id="69eed-206">Falso</span><span class="sxs-lookup"><span data-stu-id="69eed-206">False</span></span>                                        |
| <span data-ttu-id="69eed-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69eed-207">Is-Single-Valued</span></span>       | <span data-ttu-id="69eed-208">True</span><span class="sxs-lookup"><span data-stu-id="69eed-208">True</span></span>                                         |
| <span data-ttu-id="69eed-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="69eed-209">Is Indexed</span></span>             | <span data-ttu-id="69eed-210">Falso</span><span class="sxs-lookup"><span data-stu-id="69eed-210">False</span></span>                                        |
| <span data-ttu-id="69eed-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69eed-211">In Global Catalog</span></span>      | <span data-ttu-id="69eed-212">Falso</span><span class="sxs-lookup"><span data-stu-id="69eed-212">False</span></span>                                        |
| <span data-ttu-id="69eed-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69eed-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="69eed-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69eed-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69eed-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69eed-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69eed-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69eed-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69eed-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69eed-217">Search-Flags</span></span>           | <span data-ttu-id="69eed-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69eed-218">0x00000000</span></span>                                   |
| <span data-ttu-id="69eed-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69eed-219">System-Flags</span></span>           | <span data-ttu-id="69eed-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69eed-220">0x00000010</span></span>                                   |
| <span data-ttu-id="69eed-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69eed-221">Classes used in</span></span>        | [<span data-ttu-id="69eed-222">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="69eed-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="69eed-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69eed-223">Windows Server 2012</span></span>



| <span data-ttu-id="69eed-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="69eed-224">Entry</span></span> | <span data-ttu-id="69eed-225">Valor</span><span class="sxs-lookup"><span data-stu-id="69eed-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69eed-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="69eed-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69eed-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69eed-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69eed-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="69eed-228">System-Only</span></span>            | <span data-ttu-id="69eed-229">Falso</span><span class="sxs-lookup"><span data-stu-id="69eed-229">False</span></span>                                        |
| <span data-ttu-id="69eed-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69eed-230">Is-Single-Valued</span></span>       | <span data-ttu-id="69eed-231">True</span><span class="sxs-lookup"><span data-stu-id="69eed-231">True</span></span>                                         |
| <span data-ttu-id="69eed-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="69eed-232">Is Indexed</span></span>             | <span data-ttu-id="69eed-233">Falso</span><span class="sxs-lookup"><span data-stu-id="69eed-233">False</span></span>                                        |
| <span data-ttu-id="69eed-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69eed-234">In Global Catalog</span></span>      | <span data-ttu-id="69eed-235">Falso</span><span class="sxs-lookup"><span data-stu-id="69eed-235">False</span></span>                                        |
| <span data-ttu-id="69eed-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69eed-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="69eed-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69eed-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69eed-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69eed-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69eed-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69eed-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69eed-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69eed-240">Search-Flags</span></span>           | <span data-ttu-id="69eed-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69eed-241">0x00000000</span></span>                                   |
| <span data-ttu-id="69eed-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69eed-242">System-Flags</span></span>           | <span data-ttu-id="69eed-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69eed-243">0x00000010</span></span>                                   |
| <span data-ttu-id="69eed-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69eed-244">Classes used in</span></span>        | [<span data-ttu-id="69eed-245">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="69eed-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





