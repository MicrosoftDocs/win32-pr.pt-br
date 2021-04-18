---
title: UAS-Compat atributo
description: Indica se o Gerenciador de contas de segurança impedirá tamanhos de dados para tornar Active Directory compatíveis com o UAS (sistema de conta de usuário) do LanManager.
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- Esquema de UAS-Compat do atributo AD
- Esquema de AD do atributo uASCompat
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6bbf1088f48c697b03c4ef423930be2dbd24617
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755887"
---
# <a name="uas-compat-attribute"></a><span data-ttu-id="67d5b-105">UAS-Compat atributo</span><span class="sxs-lookup"><span data-stu-id="67d5b-105">UAS-Compat attribute</span></span>

<span data-ttu-id="67d5b-106">Indica se o Gerenciador de contas de segurança impedirá tamanhos de dados para tornar Active Directory compatíveis com o UAS (sistema de conta de usuário) do LanManager.</span><span class="sxs-lookup"><span data-stu-id="67d5b-106">Indicates if the security account manager will enforce data sizes to make Active Directory compatible with the LanManager User Account System (UAS).</span></span> <span data-ttu-id="67d5b-107">Se esse valor for 0, nenhum limite será imposto.</span><span class="sxs-lookup"><span data-stu-id="67d5b-107">If this value is 0, no limits are enforced.</span></span> <span data-ttu-id="67d5b-108">Se esse valor for 1, os limites a seguir serão impostos.</span><span class="sxs-lookup"><span data-stu-id="67d5b-108">If this value is 1, the following limits are enforced.</span></span>



| <span data-ttu-id="67d5b-109">Valor</span><span class="sxs-lookup"><span data-stu-id="67d5b-109">Value</span></span>                          | <span data-ttu-id="67d5b-110">Comprimento</span><span class="sxs-lookup"><span data-stu-id="67d5b-110">Length</span></span>                         |
|--------------------------------|--------------------------------|
| <span data-ttu-id="67d5b-111">Senha</span><span class="sxs-lookup"><span data-stu-id="67d5b-111">Password</span></span><br/>            | <span data-ttu-id="67d5b-112">0 a 14 caracteres</span><span class="sxs-lookup"><span data-stu-id="67d5b-112">0 to 14 characters</span></span><br/>  |
| <span data-ttu-id="67d5b-113">Nome da Conta</span><span class="sxs-lookup"><span data-stu-id="67d5b-113">Account Name</span></span><br/>        | <span data-ttu-id="67d5b-114">de 0 a 20 caracteres</span><span class="sxs-lookup"><span data-stu-id="67d5b-114">0 to 20 characters</span></span><br/>  |
| <span data-ttu-id="67d5b-115">Nome de domínio</span><span class="sxs-lookup"><span data-stu-id="67d5b-115">Domain Name</span></span><br/>         | <span data-ttu-id="67d5b-116">de 0 a 15 caracteres</span><span class="sxs-lookup"><span data-stu-id="67d5b-116">0 to 15 characters</span></span><br/>  |
| <span data-ttu-id="67d5b-117">Nome do Computador</span><span class="sxs-lookup"><span data-stu-id="67d5b-117">Computer Name</span></span><br/>       | <span data-ttu-id="67d5b-118">de 0 a 15 caracteres</span><span class="sxs-lookup"><span data-stu-id="67d5b-118">0 to 15 characters</span></span><br/>  |
| <span data-ttu-id="67d5b-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="67d5b-119">Comments</span></span><br/>            | <span data-ttu-id="67d5b-120">de 0 a 48 caracteres</span><span class="sxs-lookup"><span data-stu-id="67d5b-120">0 to 48 characters</span></span><br/>  |
| <span data-ttu-id="67d5b-121">Diretório Base</span><span class="sxs-lookup"><span data-stu-id="67d5b-121">Home Directory</span></span><br/>      | <span data-ttu-id="67d5b-122">de 0 a 256 caracteres</span><span class="sxs-lookup"><span data-stu-id="67d5b-122">0 to 256 characters</span></span><br/> |
| <span data-ttu-id="67d5b-123">Caminho do script</span><span class="sxs-lookup"><span data-stu-id="67d5b-123">Script Path</span></span><br/>         | <span data-ttu-id="67d5b-124">de 0 a 256 caracteres</span><span class="sxs-lookup"><span data-stu-id="67d5b-124">0 to 256 characters</span></span><br/> |
| <span data-ttu-id="67d5b-125">Unidades de tempo por semana</span><span class="sxs-lookup"><span data-stu-id="67d5b-125">Time Units Per Week</span></span><br/> | <span data-ttu-id="67d5b-126">168 bits (21 bytes)</span><span class="sxs-lookup"><span data-stu-id="67d5b-126">168 bits (21 bytes)</span></span><br/> |



 



| <span data-ttu-id="67d5b-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="67d5b-127">Entry</span></span> | <span data-ttu-id="67d5b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="67d5b-128">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="67d5b-129">CN</span><span class="sxs-lookup"><span data-stu-id="67d5b-129">CN</span></span>                | <span data-ttu-id="67d5b-130">UAS-Compat</span><span class="sxs-lookup"><span data-stu-id="67d5b-130">UAS-Compat</span></span>                           |
| <span data-ttu-id="67d5b-131">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="67d5b-131">Ldap-Display-Name</span></span> | <span data-ttu-id="67d5b-132">uASCompat</span><span class="sxs-lookup"><span data-stu-id="67d5b-132">uASCompat</span></span>                            |
| <span data-ttu-id="67d5b-133">Tamanho</span><span class="sxs-lookup"><span data-stu-id="67d5b-133">Size</span></span>              | \-                                   |
| <span data-ttu-id="67d5b-134">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="67d5b-134">Update Privilege</span></span>  | <span data-ttu-id="67d5b-135">Executado por um administrador.</span><span class="sxs-lookup"><span data-stu-id="67d5b-135">Performed by an administrator.</span></span>       |
| <span data-ttu-id="67d5b-136">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="67d5b-136">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="67d5b-137">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="67d5b-137">Attribute-Id</span></span>      | <span data-ttu-id="67d5b-138">1.2.840.113556.1.4.155</span><span class="sxs-lookup"><span data-stu-id="67d5b-138">1.2.840.113556.1.4.155</span></span>               |
| <span data-ttu-id="67d5b-139">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="67d5b-139">System-Id-Guid</span></span>    | <span data-ttu-id="67d5b-140">bf967a61-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="67d5b-140">bf967a61-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="67d5b-141">Syntax</span><span class="sxs-lookup"><span data-stu-id="67d5b-141">Syntax</span></span>            | [<span data-ttu-id="67d5b-142">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="67d5b-142">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="67d5b-143">Implementações</span><span class="sxs-lookup"><span data-stu-id="67d5b-143">Implementations</span></span>

-   [<span data-ttu-id="67d5b-144">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="67d5b-144">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="67d5b-145">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="67d5b-145">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="67d5b-146">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="67d5b-146">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="67d5b-147">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="67d5b-147">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="67d5b-148">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="67d5b-148">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="67d5b-149">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="67d5b-149">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="67d5b-150">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="67d5b-150">Windows 2000 Server</span></span>



| <span data-ttu-id="67d5b-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="67d5b-151">Entry</span></span> | <span data-ttu-id="67d5b-152">Valor</span><span class="sxs-lookup"><span data-stu-id="67d5b-152">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="67d5b-153">ID do link</span><span class="sxs-lookup"><span data-stu-id="67d5b-153">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="67d5b-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67d5b-154">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="67d5b-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="67d5b-155">System-Only</span></span>            | <span data-ttu-id="67d5b-156">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-156">False</span></span>                                                 |
| <span data-ttu-id="67d5b-157">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67d5b-157">Is-Single-Valued</span></span>       | <span data-ttu-id="67d5b-158">True</span><span class="sxs-lookup"><span data-stu-id="67d5b-158">True</span></span>                                                  |
| <span data-ttu-id="67d5b-159">É indexado</span><span class="sxs-lookup"><span data-stu-id="67d5b-159">Is Indexed</span></span>             | <span data-ttu-id="67d5b-160">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-160">False</span></span>                                                 |
| <span data-ttu-id="67d5b-161">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67d5b-161">In Global Catalog</span></span>      | <span data-ttu-id="67d5b-162">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-162">False</span></span>                                                 |
| <span data-ttu-id="67d5b-163">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67d5b-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="67d5b-164">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67d5b-164">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="67d5b-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67d5b-165">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="67d5b-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67d5b-166">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="67d5b-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67d5b-167">Search-Flags</span></span>           | <span data-ttu-id="67d5b-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67d5b-168">0x00000000</span></span>                                            |
| <span data-ttu-id="67d5b-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67d5b-169">System-Flags</span></span>           | <span data-ttu-id="67d5b-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67d5b-170">0x00000010</span></span>                                            |
| <span data-ttu-id="67d5b-171">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67d5b-171">Classes used in</span></span>        | [<span data-ttu-id="67d5b-172">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="67d5b-172">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="67d5b-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="67d5b-173">Windows Server 2003</span></span>



| <span data-ttu-id="67d5b-174">Entrada</span><span class="sxs-lookup"><span data-stu-id="67d5b-174">Entry</span></span> | <span data-ttu-id="67d5b-175">Valor</span><span class="sxs-lookup"><span data-stu-id="67d5b-175">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="67d5b-176">ID do link</span><span class="sxs-lookup"><span data-stu-id="67d5b-176">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="67d5b-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67d5b-177">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="67d5b-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="67d5b-178">System-Only</span></span>            | <span data-ttu-id="67d5b-179">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-179">False</span></span>                                                 |
| <span data-ttu-id="67d5b-180">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67d5b-180">Is-Single-Valued</span></span>       | <span data-ttu-id="67d5b-181">True</span><span class="sxs-lookup"><span data-stu-id="67d5b-181">True</span></span>                                                  |
| <span data-ttu-id="67d5b-182">É indexado</span><span class="sxs-lookup"><span data-stu-id="67d5b-182">Is Indexed</span></span>             | <span data-ttu-id="67d5b-183">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-183">False</span></span>                                                 |
| <span data-ttu-id="67d5b-184">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67d5b-184">In Global Catalog</span></span>      | <span data-ttu-id="67d5b-185">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-185">False</span></span>                                                 |
| <span data-ttu-id="67d5b-186">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67d5b-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="67d5b-187">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67d5b-187">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="67d5b-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67d5b-188">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="67d5b-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67d5b-189">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="67d5b-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67d5b-190">Search-Flags</span></span>           | <span data-ttu-id="67d5b-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67d5b-191">0x00000000</span></span>                                            |
| <span data-ttu-id="67d5b-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67d5b-192">System-Flags</span></span>           | <span data-ttu-id="67d5b-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67d5b-193">0x00000010</span></span>                                            |
| <span data-ttu-id="67d5b-194">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67d5b-194">Classes used in</span></span>        | [<span data-ttu-id="67d5b-195">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="67d5b-195">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="67d5b-196">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="67d5b-196">Windows Server 2003 R2</span></span>



| <span data-ttu-id="67d5b-197">Entrada</span><span class="sxs-lookup"><span data-stu-id="67d5b-197">Entry</span></span> | <span data-ttu-id="67d5b-198">Valor</span><span class="sxs-lookup"><span data-stu-id="67d5b-198">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="67d5b-199">ID do link</span><span class="sxs-lookup"><span data-stu-id="67d5b-199">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="67d5b-200">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67d5b-200">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="67d5b-201">System-Only</span><span class="sxs-lookup"><span data-stu-id="67d5b-201">System-Only</span></span>            | <span data-ttu-id="67d5b-202">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-202">False</span></span>                                                 |
| <span data-ttu-id="67d5b-203">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67d5b-203">Is-Single-Valued</span></span>       | <span data-ttu-id="67d5b-204">True</span><span class="sxs-lookup"><span data-stu-id="67d5b-204">True</span></span>                                                  |
| <span data-ttu-id="67d5b-205">É indexado</span><span class="sxs-lookup"><span data-stu-id="67d5b-205">Is Indexed</span></span>             | <span data-ttu-id="67d5b-206">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-206">False</span></span>                                                 |
| <span data-ttu-id="67d5b-207">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67d5b-207">In Global Catalog</span></span>      | <span data-ttu-id="67d5b-208">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-208">False</span></span>                                                 |
| <span data-ttu-id="67d5b-209">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67d5b-209">NT-Security-Descriptor</span></span> | <span data-ttu-id="67d5b-210">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67d5b-210">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="67d5b-211">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67d5b-211">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="67d5b-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67d5b-212">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="67d5b-213">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67d5b-213">Search-Flags</span></span>           | <span data-ttu-id="67d5b-214">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67d5b-214">0x00000000</span></span>                                            |
| <span data-ttu-id="67d5b-215">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67d5b-215">System-Flags</span></span>           | <span data-ttu-id="67d5b-216">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67d5b-216">0x00000010</span></span>                                            |
| <span data-ttu-id="67d5b-217">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67d5b-217">Classes used in</span></span>        | [<span data-ttu-id="67d5b-218">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="67d5b-218">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="67d5b-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67d5b-219">Windows Server 2008</span></span>



| <span data-ttu-id="67d5b-220">Entrada</span><span class="sxs-lookup"><span data-stu-id="67d5b-220">Entry</span></span> | <span data-ttu-id="67d5b-221">Valor</span><span class="sxs-lookup"><span data-stu-id="67d5b-221">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="67d5b-222">ID do link</span><span class="sxs-lookup"><span data-stu-id="67d5b-222">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="67d5b-223">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67d5b-223">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="67d5b-224">System-Only</span><span class="sxs-lookup"><span data-stu-id="67d5b-224">System-Only</span></span>            | <span data-ttu-id="67d5b-225">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-225">False</span></span>                                                 |
| <span data-ttu-id="67d5b-226">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67d5b-226">Is-Single-Valued</span></span>       | <span data-ttu-id="67d5b-227">True</span><span class="sxs-lookup"><span data-stu-id="67d5b-227">True</span></span>                                                  |
| <span data-ttu-id="67d5b-228">É indexado</span><span class="sxs-lookup"><span data-stu-id="67d5b-228">Is Indexed</span></span>             | <span data-ttu-id="67d5b-229">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-229">False</span></span>                                                 |
| <span data-ttu-id="67d5b-230">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67d5b-230">In Global Catalog</span></span>      | <span data-ttu-id="67d5b-231">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-231">False</span></span>                                                 |
| <span data-ttu-id="67d5b-232">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67d5b-232">NT-Security-Descriptor</span></span> | <span data-ttu-id="67d5b-233">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67d5b-233">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="67d5b-234">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67d5b-234">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="67d5b-235">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67d5b-235">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="67d5b-236">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67d5b-236">Search-Flags</span></span>           | <span data-ttu-id="67d5b-237">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67d5b-237">0x00000000</span></span>                                            |
| <span data-ttu-id="67d5b-238">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67d5b-238">System-Flags</span></span>           | <span data-ttu-id="67d5b-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67d5b-239">0x00000010</span></span>                                            |
| <span data-ttu-id="67d5b-240">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67d5b-240">Classes used in</span></span>        | [<span data-ttu-id="67d5b-241">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="67d5b-241">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="67d5b-242">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="67d5b-242">Windows Server 2008 R2</span></span>



| <span data-ttu-id="67d5b-243">Entrada</span><span class="sxs-lookup"><span data-stu-id="67d5b-243">Entry</span></span> | <span data-ttu-id="67d5b-244">Valor</span><span class="sxs-lookup"><span data-stu-id="67d5b-244">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="67d5b-245">ID do link</span><span class="sxs-lookup"><span data-stu-id="67d5b-245">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="67d5b-246">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67d5b-246">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="67d5b-247">System-Only</span><span class="sxs-lookup"><span data-stu-id="67d5b-247">System-Only</span></span>            | <span data-ttu-id="67d5b-248">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-248">False</span></span>                                                 |
| <span data-ttu-id="67d5b-249">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67d5b-249">Is-Single-Valued</span></span>       | <span data-ttu-id="67d5b-250">True</span><span class="sxs-lookup"><span data-stu-id="67d5b-250">True</span></span>                                                  |
| <span data-ttu-id="67d5b-251">É indexado</span><span class="sxs-lookup"><span data-stu-id="67d5b-251">Is Indexed</span></span>             | <span data-ttu-id="67d5b-252">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-252">False</span></span>                                                 |
| <span data-ttu-id="67d5b-253">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67d5b-253">In Global Catalog</span></span>      | <span data-ttu-id="67d5b-254">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-254">False</span></span>                                                 |
| <span data-ttu-id="67d5b-255">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67d5b-255">NT-Security-Descriptor</span></span> | <span data-ttu-id="67d5b-256">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67d5b-256">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="67d5b-257">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67d5b-257">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="67d5b-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67d5b-258">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="67d5b-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67d5b-259">Search-Flags</span></span>           | <span data-ttu-id="67d5b-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67d5b-260">0x00000000</span></span>                                            |
| <span data-ttu-id="67d5b-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67d5b-261">System-Flags</span></span>           | <span data-ttu-id="67d5b-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67d5b-262">0x00000010</span></span>                                            |
| <span data-ttu-id="67d5b-263">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67d5b-263">Classes used in</span></span>        | [<span data-ttu-id="67d5b-264">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="67d5b-264">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="67d5b-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="67d5b-265">Windows Server 2012</span></span>



| <span data-ttu-id="67d5b-266">Entrada</span><span class="sxs-lookup"><span data-stu-id="67d5b-266">Entry</span></span> | <span data-ttu-id="67d5b-267">Valor</span><span class="sxs-lookup"><span data-stu-id="67d5b-267">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="67d5b-268">ID do link</span><span class="sxs-lookup"><span data-stu-id="67d5b-268">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="67d5b-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67d5b-269">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="67d5b-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="67d5b-270">System-Only</span></span>            | <span data-ttu-id="67d5b-271">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-271">False</span></span>                                                 |
| <span data-ttu-id="67d5b-272">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67d5b-272">Is-Single-Valued</span></span>       | <span data-ttu-id="67d5b-273">True</span><span class="sxs-lookup"><span data-stu-id="67d5b-273">True</span></span>                                                  |
| <span data-ttu-id="67d5b-274">É indexado</span><span class="sxs-lookup"><span data-stu-id="67d5b-274">Is Indexed</span></span>             | <span data-ttu-id="67d5b-275">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-275">False</span></span>                                                 |
| <span data-ttu-id="67d5b-276">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67d5b-276">In Global Catalog</span></span>      | <span data-ttu-id="67d5b-277">Falso</span><span class="sxs-lookup"><span data-stu-id="67d5b-277">False</span></span>                                                 |
| <span data-ttu-id="67d5b-278">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67d5b-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="67d5b-279">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67d5b-279">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="67d5b-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67d5b-280">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="67d5b-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67d5b-281">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="67d5b-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67d5b-282">Search-Flags</span></span>           | <span data-ttu-id="67d5b-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67d5b-283">0x00000000</span></span>                                            |
| <span data-ttu-id="67d5b-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67d5b-284">System-Flags</span></span>           | <span data-ttu-id="67d5b-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67d5b-285">0x00000010</span></span>                                            |
| <span data-ttu-id="67d5b-286">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67d5b-286">Classes used in</span></span>        | [<span data-ttu-id="67d5b-287">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="67d5b-287">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





