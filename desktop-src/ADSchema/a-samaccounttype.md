---
title: SAM-atributo de tipo de conta
description: Esse atributo contém informações sobre cada objeto de tipo de conta.
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- SAM-tipo de conta do atributo AD Schema
- Esquema de AD do atributo sAMAccountType
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51de46dac0faabcc248159f7dcabafcd6060725
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919425"
---
# <a name="sam-account-type-attribute"></a><span data-ttu-id="d08a3-105">SAM-atributo de tipo de conta</span><span class="sxs-lookup"><span data-stu-id="d08a3-105">SAM-Account-Type attribute</span></span>

<span data-ttu-id="d08a3-106">Esse atributo contém informações sobre cada objeto de tipo de conta.</span><span class="sxs-lookup"><span data-stu-id="d08a3-106">This attribute contains information about every account type object.</span></span> <span data-ttu-id="d08a3-107">Você pode enumerar uma lista de tipos de conta ou pode usar a API de informações de exibição para criar uma lista.</span><span class="sxs-lookup"><span data-stu-id="d08a3-107">You can enumerate a list of account types or you can use the Display Information API to create a list.</span></span> <span data-ttu-id="d08a3-108">Como computadores, contas de usuário normais e contas de confiança também podem ser enumerados como objetos de usuário, os valores dessas contas devem ser um intervalo contíguo.</span><span class="sxs-lookup"><span data-stu-id="d08a3-108">Because computers, normal user accounts, and trust accounts can also be enumerated as user objects, the values for these accounts must be a contiguous range.</span></span>

<span data-ttu-id="d08a3-109">Os valores possíveis para esse atributo são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d08a3-109">The possible values for this attribute are the following:</span></span>

-   <span data-ttu-id="d08a3-110">\_Objeto de domínio Sam \_ 0x0</span><span class="sxs-lookup"><span data-stu-id="d08a3-110">SAM\_DOMAIN\_OBJECT 0x0</span></span>
-   <span data-ttu-id="d08a3-111">\_Objeto de grupo Sam \_ 0x10000000</span><span class="sxs-lookup"><span data-stu-id="d08a3-111">SAM\_GROUP\_OBJECT 0x10000000</span></span>
-   <span data-ttu-id="d08a3-112">SAM \_ \_ objeto de \_ grupo não segurança \_ 0x10000001</span><span class="sxs-lookup"><span data-stu-id="d08a3-112">SAM\_NON\_SECURITY\_GROUP\_OBJECT 0x10000001</span></span>
-   <span data-ttu-id="d08a3-113">\_Objeto de alias Sam \_ 0x20000000</span><span class="sxs-lookup"><span data-stu-id="d08a3-113">SAM\_ALIAS\_OBJECT 0x20000000</span></span>
-   <span data-ttu-id="d08a3-114">\_Objeto de \_ alias de não segurança Sam \_ \_ 0x20000001</span><span class="sxs-lookup"><span data-stu-id="d08a3-114">SAM\_NON\_SECURITY\_ALIAS\_OBJECT 0x20000001</span></span>
-   <span data-ttu-id="d08a3-115">\_Objeto de usuário Sam \_ 0x30000000</span><span class="sxs-lookup"><span data-stu-id="d08a3-115">SAM\_USER\_OBJECT 0x30000000</span></span>
-   <span data-ttu-id="d08a3-116">\_Conta de usuário normal do Sam \_ \_ 0x30000000</span><span class="sxs-lookup"><span data-stu-id="d08a3-116">SAM\_NORMAL\_USER\_ACCOUNT 0x30000000</span></span>
-   <span data-ttu-id="d08a3-117">0x30000001 da conta do \_ computador Sam \_</span><span class="sxs-lookup"><span data-stu-id="d08a3-117">SAM\_MACHINE\_ACCOUNT 0x30000001</span></span>
-   <span data-ttu-id="d08a3-118">\_0x30000002 de \_ conta confiável Sam</span><span class="sxs-lookup"><span data-stu-id="d08a3-118">SAM\_TRUST\_ACCOUNT 0x30000002</span></span>
-   <span data-ttu-id="d08a3-119">\_Grupo básico do aplicativo Sam \_ \_ 0x40000000</span><span class="sxs-lookup"><span data-stu-id="d08a3-119">SAM\_APP\_BASIC\_GROUP 0x40000000</span></span>
-   <span data-ttu-id="d08a3-120">\_Grupo de consulta do aplicativo Sam \_ \_ 0x40000001</span><span class="sxs-lookup"><span data-stu-id="d08a3-120">SAM\_APP\_QUERY\_GROUP 0x40000001</span></span>
-   <span data-ttu-id="d08a3-121">\_Tipo de conta Sam máx. \_ \_ 0x7FFFFFFF</span><span class="sxs-lookup"><span data-stu-id="d08a3-121">SAM\_ACCOUNT\_TYPE\_MAX 0x7fffffff</span></span>



| <span data-ttu-id="d08a3-122">Entrada</span><span class="sxs-lookup"><span data-stu-id="d08a3-122">Entry</span></span> | <span data-ttu-id="d08a3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d08a3-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d08a3-124">CN</span><span class="sxs-lookup"><span data-stu-id="d08a3-124">CN</span></span>                | <span data-ttu-id="d08a3-125">SAM-tipo de conta</span><span class="sxs-lookup"><span data-stu-id="d08a3-125">SAM-Account-Type</span></span>                                                |
| <span data-ttu-id="d08a3-126">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d08a3-126">Ldap-Display-Name</span></span> | <span data-ttu-id="d08a3-127">sAMAccountType</span><span class="sxs-lookup"><span data-stu-id="d08a3-127">sAMAccountType</span></span>                                                  |
| <span data-ttu-id="d08a3-128">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d08a3-128">Size</span></span>              | \-                                                              |
| <span data-ttu-id="d08a3-129">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="d08a3-129">Update Privilege</span></span>  | <span data-ttu-id="d08a3-130">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="d08a3-130">This value is set by the system.</span></span>                                |
| <span data-ttu-id="d08a3-131">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="d08a3-131">Update Frequency</span></span>  | <span data-ttu-id="d08a3-132">Isso é definido pelo sistema operacional quando o objeto é criado.</span><span class="sxs-lookup"><span data-stu-id="d08a3-132">This is set by the operating system when the object is created.</span></span> |
| <span data-ttu-id="d08a3-133">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d08a3-133">Attribute-Id</span></span>      | <span data-ttu-id="d08a3-134">1.2.840.113556.1.4.302</span><span class="sxs-lookup"><span data-stu-id="d08a3-134">1.2.840.113556.1.4.302</span></span>                                          |
| <span data-ttu-id="d08a3-135">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d08a3-135">System-Id-Guid</span></span>    | <span data-ttu-id="d08a3-136">6e7b626c-64f2-11d0-afd2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="d08a3-136">6e7b626c-64f2-11d0-afd2-00c04fd930c9</span></span>                            |
| <span data-ttu-id="d08a3-137">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d08a3-137">Syntax</span></span>            | [<span data-ttu-id="d08a3-138">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="d08a3-138">**Enumeration**</span></span>](s-enumeration.md)                            |



## <a name="implementations"></a><span data-ttu-id="d08a3-139">Implementações</span><span class="sxs-lookup"><span data-stu-id="d08a3-139">Implementations</span></span>

-   [<span data-ttu-id="d08a3-140">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d08a3-140">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d08a3-141">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d08a3-141">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d08a3-142">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d08a3-142">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d08a3-143">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d08a3-143">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d08a3-144">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d08a3-144">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d08a3-145">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d08a3-145">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d08a3-146">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d08a3-146">Windows 2000 Server</span></span>



| <span data-ttu-id="d08a3-147">Entrada</span><span class="sxs-lookup"><span data-stu-id="d08a3-147">Entry</span></span> | <span data-ttu-id="d08a3-148">Valor</span><span class="sxs-lookup"><span data-stu-id="d08a3-148">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d08a3-149">ID do link</span><span class="sxs-lookup"><span data-stu-id="d08a3-149">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d08a3-150">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d08a3-150">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d08a3-151">System-Only</span><span class="sxs-lookup"><span data-stu-id="d08a3-151">System-Only</span></span>            | <span data-ttu-id="d08a3-152">Falso</span><span class="sxs-lookup"><span data-stu-id="d08a3-152">False</span></span>                                                        |
| <span data-ttu-id="d08a3-153">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d08a3-153">Is-Single-Valued</span></span>       | <span data-ttu-id="d08a3-154">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-154">True</span></span>                                                         |
| <span data-ttu-id="d08a3-155">É indexado</span><span class="sxs-lookup"><span data-stu-id="d08a3-155">Is Indexed</span></span>             | <span data-ttu-id="d08a3-156">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-156">True</span></span>                                                         |
| <span data-ttu-id="d08a3-157">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d08a3-157">In Global Catalog</span></span>      | <span data-ttu-id="d08a3-158">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-158">True</span></span>                                                         |
| <span data-ttu-id="d08a3-159">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d08a3-159">NT-Security-Descriptor</span></span> | <span data-ttu-id="d08a3-160">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d08a3-160">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d08a3-161">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d08a3-161">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d08a3-162">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d08a3-162">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d08a3-163">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d08a3-163">Search-Flags</span></span>           | <span data-ttu-id="d08a3-164">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d08a3-164">0x00000001</span></span>                                                   |
| <span data-ttu-id="d08a3-165">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d08a3-165">System-Flags</span></span>           | <span data-ttu-id="d08a3-166">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d08a3-166">0x00000012</span></span>                                                   |
| <span data-ttu-id="d08a3-167">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d08a3-167">Classes used in</span></span>        | [<span data-ttu-id="d08a3-168">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="d08a3-168">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d08a3-169">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d08a3-169">Windows Server 2003</span></span>



| <span data-ttu-id="d08a3-170">Entrada</span><span class="sxs-lookup"><span data-stu-id="d08a3-170">Entry</span></span> | <span data-ttu-id="d08a3-171">Valor</span><span class="sxs-lookup"><span data-stu-id="d08a3-171">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d08a3-172">ID do link</span><span class="sxs-lookup"><span data-stu-id="d08a3-172">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d08a3-173">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d08a3-173">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d08a3-174">System-Only</span><span class="sxs-lookup"><span data-stu-id="d08a3-174">System-Only</span></span>            | <span data-ttu-id="d08a3-175">Falso</span><span class="sxs-lookup"><span data-stu-id="d08a3-175">False</span></span>                                                        |
| <span data-ttu-id="d08a3-176">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d08a3-176">Is-Single-Valued</span></span>       | <span data-ttu-id="d08a3-177">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-177">True</span></span>                                                         |
| <span data-ttu-id="d08a3-178">É indexado</span><span class="sxs-lookup"><span data-stu-id="d08a3-178">Is Indexed</span></span>             | <span data-ttu-id="d08a3-179">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-179">True</span></span>                                                         |
| <span data-ttu-id="d08a3-180">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d08a3-180">In Global Catalog</span></span>      | <span data-ttu-id="d08a3-181">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-181">True</span></span>                                                         |
| <span data-ttu-id="d08a3-182">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d08a3-182">NT-Security-Descriptor</span></span> | <span data-ttu-id="d08a3-183">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d08a3-183">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d08a3-184">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d08a3-184">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d08a3-185">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d08a3-185">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d08a3-186">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d08a3-186">Search-Flags</span></span>           | <span data-ttu-id="d08a3-187">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d08a3-187">0x00000001</span></span>                                                   |
| <span data-ttu-id="d08a3-188">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d08a3-188">System-Flags</span></span>           | <span data-ttu-id="d08a3-189">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d08a3-189">0x00000012</span></span>                                                   |
| <span data-ttu-id="d08a3-190">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d08a3-190">Classes used in</span></span>        | [<span data-ttu-id="d08a3-191">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="d08a3-191">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d08a3-192">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d08a3-192">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d08a3-193">Entrada</span><span class="sxs-lookup"><span data-stu-id="d08a3-193">Entry</span></span> | <span data-ttu-id="d08a3-194">Valor</span><span class="sxs-lookup"><span data-stu-id="d08a3-194">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d08a3-195">ID do link</span><span class="sxs-lookup"><span data-stu-id="d08a3-195">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d08a3-196">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d08a3-196">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d08a3-197">System-Only</span><span class="sxs-lookup"><span data-stu-id="d08a3-197">System-Only</span></span>            | <span data-ttu-id="d08a3-198">Falso</span><span class="sxs-lookup"><span data-stu-id="d08a3-198">False</span></span>                                                        |
| <span data-ttu-id="d08a3-199">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d08a3-199">Is-Single-Valued</span></span>       | <span data-ttu-id="d08a3-200">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-200">True</span></span>                                                         |
| <span data-ttu-id="d08a3-201">É indexado</span><span class="sxs-lookup"><span data-stu-id="d08a3-201">Is Indexed</span></span>             | <span data-ttu-id="d08a3-202">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-202">True</span></span>                                                         |
| <span data-ttu-id="d08a3-203">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d08a3-203">In Global Catalog</span></span>      | <span data-ttu-id="d08a3-204">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-204">True</span></span>                                                         |
| <span data-ttu-id="d08a3-205">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d08a3-205">NT-Security-Descriptor</span></span> | <span data-ttu-id="d08a3-206">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d08a3-206">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d08a3-207">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d08a3-207">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d08a3-208">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d08a3-208">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d08a3-209">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d08a3-209">Search-Flags</span></span>           | <span data-ttu-id="d08a3-210">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d08a3-210">0x00000001</span></span>                                                   |
| <span data-ttu-id="d08a3-211">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d08a3-211">System-Flags</span></span>           | <span data-ttu-id="d08a3-212">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d08a3-212">0x00000012</span></span>                                                   |
| <span data-ttu-id="d08a3-213">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d08a3-213">Classes used in</span></span>        | [<span data-ttu-id="d08a3-214">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="d08a3-214">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d08a3-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d08a3-215">Windows Server 2008</span></span>



| <span data-ttu-id="d08a3-216">Entrada</span><span class="sxs-lookup"><span data-stu-id="d08a3-216">Entry</span></span> | <span data-ttu-id="d08a3-217">Valor</span><span class="sxs-lookup"><span data-stu-id="d08a3-217">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d08a3-218">ID do link</span><span class="sxs-lookup"><span data-stu-id="d08a3-218">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d08a3-219">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d08a3-219">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d08a3-220">System-Only</span><span class="sxs-lookup"><span data-stu-id="d08a3-220">System-Only</span></span>            | <span data-ttu-id="d08a3-221">Falso</span><span class="sxs-lookup"><span data-stu-id="d08a3-221">False</span></span>                                                        |
| <span data-ttu-id="d08a3-222">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d08a3-222">Is-Single-Valued</span></span>       | <span data-ttu-id="d08a3-223">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-223">True</span></span>                                                         |
| <span data-ttu-id="d08a3-224">É indexado</span><span class="sxs-lookup"><span data-stu-id="d08a3-224">Is Indexed</span></span>             | <span data-ttu-id="d08a3-225">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-225">True</span></span>                                                         |
| <span data-ttu-id="d08a3-226">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d08a3-226">In Global Catalog</span></span>      | <span data-ttu-id="d08a3-227">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-227">True</span></span>                                                         |
| <span data-ttu-id="d08a3-228">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d08a3-228">NT-Security-Descriptor</span></span> | <span data-ttu-id="d08a3-229">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d08a3-229">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d08a3-230">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d08a3-230">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d08a3-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d08a3-231">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d08a3-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d08a3-232">Search-Flags</span></span>           | <span data-ttu-id="d08a3-233">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d08a3-233">0x00000001</span></span>                                                   |
| <span data-ttu-id="d08a3-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d08a3-234">System-Flags</span></span>           | <span data-ttu-id="d08a3-235">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d08a3-235">0x00000012</span></span>                                                   |
| <span data-ttu-id="d08a3-236">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d08a3-236">Classes used in</span></span>        | [<span data-ttu-id="d08a3-237">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="d08a3-237">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d08a3-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d08a3-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d08a3-239">Entrada</span><span class="sxs-lookup"><span data-stu-id="d08a3-239">Entry</span></span> | <span data-ttu-id="d08a3-240">Valor</span><span class="sxs-lookup"><span data-stu-id="d08a3-240">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d08a3-241">ID do link</span><span class="sxs-lookup"><span data-stu-id="d08a3-241">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d08a3-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d08a3-242">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d08a3-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="d08a3-243">System-Only</span></span>            | <span data-ttu-id="d08a3-244">Falso</span><span class="sxs-lookup"><span data-stu-id="d08a3-244">False</span></span>                                                        |
| <span data-ttu-id="d08a3-245">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d08a3-245">Is-Single-Valued</span></span>       | <span data-ttu-id="d08a3-246">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-246">True</span></span>                                                         |
| <span data-ttu-id="d08a3-247">É indexado</span><span class="sxs-lookup"><span data-stu-id="d08a3-247">Is Indexed</span></span>             | <span data-ttu-id="d08a3-248">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-248">True</span></span>                                                         |
| <span data-ttu-id="d08a3-249">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d08a3-249">In Global Catalog</span></span>      | <span data-ttu-id="d08a3-250">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-250">True</span></span>                                                         |
| <span data-ttu-id="d08a3-251">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d08a3-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="d08a3-252">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d08a3-252">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d08a3-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d08a3-253">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d08a3-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d08a3-254">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d08a3-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d08a3-255">Search-Flags</span></span>           | <span data-ttu-id="d08a3-256">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d08a3-256">0x00000001</span></span>                                                   |
| <span data-ttu-id="d08a3-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d08a3-257">System-Flags</span></span>           | <span data-ttu-id="d08a3-258">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d08a3-258">0x00000012</span></span>                                                   |
| <span data-ttu-id="d08a3-259">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d08a3-259">Classes used in</span></span>        | [<span data-ttu-id="d08a3-260">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="d08a3-260">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d08a3-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d08a3-261">Windows Server 2012</span></span>



| <span data-ttu-id="d08a3-262">Entrada</span><span class="sxs-lookup"><span data-stu-id="d08a3-262">Entry</span></span> | <span data-ttu-id="d08a3-263">Valor</span><span class="sxs-lookup"><span data-stu-id="d08a3-263">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d08a3-264">ID do link</span><span class="sxs-lookup"><span data-stu-id="d08a3-264">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d08a3-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d08a3-265">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d08a3-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="d08a3-266">System-Only</span></span>            | <span data-ttu-id="d08a3-267">Falso</span><span class="sxs-lookup"><span data-stu-id="d08a3-267">False</span></span>                                                        |
| <span data-ttu-id="d08a3-268">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d08a3-268">Is-Single-Valued</span></span>       | <span data-ttu-id="d08a3-269">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-269">True</span></span>                                                         |
| <span data-ttu-id="d08a3-270">É indexado</span><span class="sxs-lookup"><span data-stu-id="d08a3-270">Is Indexed</span></span>             | <span data-ttu-id="d08a3-271">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-271">True</span></span>                                                         |
| <span data-ttu-id="d08a3-272">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d08a3-272">In Global Catalog</span></span>      | <span data-ttu-id="d08a3-273">True</span><span class="sxs-lookup"><span data-stu-id="d08a3-273">True</span></span>                                                         |
| <span data-ttu-id="d08a3-274">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d08a3-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="d08a3-275">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d08a3-275">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d08a3-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d08a3-276">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d08a3-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d08a3-277">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d08a3-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d08a3-278">Search-Flags</span></span>           | <span data-ttu-id="d08a3-279">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d08a3-279">0x00000001</span></span>                                                   |
| <span data-ttu-id="d08a3-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d08a3-280">System-Flags</span></span>           | <span data-ttu-id="d08a3-281">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d08a3-281">0x00000012</span></span>                                                   |
| <span data-ttu-id="d08a3-282">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d08a3-282">Classes used in</span></span>        | [<span data-ttu-id="d08a3-283">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="d08a3-283">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





