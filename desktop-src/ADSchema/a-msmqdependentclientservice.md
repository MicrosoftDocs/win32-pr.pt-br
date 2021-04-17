---
title: Atributo de serviço de cliente dependente do MSMQ
description: Indica se este servidor fornece serviços de clientes dependentes.
ms.assetid: a5902799-b2df-4679-9dd6-f75630dadfb4
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo do serviço de cliente dependente do MSMQ
- Esquema de AD do atributo mSMQDependentClientService
topic_type:
- apiref
api_name:
- MSMQ-Dependent-Client-Service
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a3865eab51c2dbd37fec75a533a0e7ed9334ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105750995"
---
# <a name="msmq-dependent-client-service-attribute"></a><span data-ttu-id="2c5a6-105">Atributo de serviço de cliente dependente do MSMQ</span><span class="sxs-lookup"><span data-stu-id="2c5a6-105">MSMQ-Dependent-Client-Service attribute</span></span>

<span data-ttu-id="2c5a6-106">Indica se este servidor fornece serviços de clientes dependentes.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-106">Indicates whether this server provides dependent clients services.</span></span>



| <span data-ttu-id="2c5a6-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="2c5a6-107">Entry</span></span> | <span data-ttu-id="2c5a6-108">Valor</span><span class="sxs-lookup"><span data-stu-id="2c5a6-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2c5a6-109">CN</span><span class="sxs-lookup"><span data-stu-id="2c5a6-109">CN</span></span>                | <span data-ttu-id="2c5a6-110">Serviço de cliente dependente do MSMQ</span><span class="sxs-lookup"><span data-stu-id="2c5a6-110">MSMQ-Dependent-Client-Service</span></span>        |
| <span data-ttu-id="2c5a6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2c5a6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2c5a6-112">mSMQDependentClientService</span><span class="sxs-lookup"><span data-stu-id="2c5a6-112">mSMQDependentClientService</span></span>           |
| <span data-ttu-id="2c5a6-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="2c5a6-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="2c5a6-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="2c5a6-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="2c5a6-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="2c5a6-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2c5a6-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2c5a6-116">Attribute-Id</span></span>      | <span data-ttu-id="2c5a6-117">1.2.840.113556.1.4.1239</span><span class="sxs-lookup"><span data-stu-id="2c5a6-117">1.2.840.113556.1.4.1239</span></span>              |
| <span data-ttu-id="2c5a6-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2c5a6-118">System-Id-Guid</span></span>    | <span data-ttu-id="2c5a6-119">2df90d83-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="2c5a6-119">2df90d83-009f-11d2-aa4c-00c04fd7d83a</span></span> |
| <span data-ttu-id="2c5a6-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c5a6-120">Syntax</span></span>            | [<span data-ttu-id="2c5a6-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2c5a6-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="2c5a6-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="2c5a6-122">Implementations</span></span>

-   [<span data-ttu-id="2c5a6-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2c5a6-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2c5a6-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2c5a6-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2c5a6-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2c5a6-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2c5a6-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2c5a6-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2c5a6-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2c5a6-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2c5a6-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2c5a6-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2c5a6-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2c5a6-129">Windows 2000 Server</span></span>



| <span data-ttu-id="2c5a6-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="2c5a6-130">Entry</span></span> | <span data-ttu-id="2c5a6-131">Valor</span><span class="sxs-lookup"><span data-stu-id="2c5a6-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="2c5a6-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="2c5a6-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="2c5a6-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c5a6-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="2c5a6-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c5a6-134">System-Only</span></span>            | <span data-ttu-id="2c5a6-135">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-135">False</span></span>                                              |
| <span data-ttu-id="2c5a6-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2c5a6-136">Is-Single-Valued</span></span>       | <span data-ttu-id="2c5a6-137">True</span><span class="sxs-lookup"><span data-stu-id="2c5a6-137">True</span></span>                                               |
| <span data-ttu-id="2c5a6-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="2c5a6-138">Is Indexed</span></span>             | <span data-ttu-id="2c5a6-139">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-139">False</span></span>                                              |
| <span data-ttu-id="2c5a6-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2c5a6-140">In Global Catalog</span></span>      | <span data-ttu-id="2c5a6-141">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-141">False</span></span>                                              |
| <span data-ttu-id="2c5a6-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2c5a6-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c5a6-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2c5a6-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="2c5a6-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c5a6-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="2c5a6-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c5a6-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="2c5a6-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c5a6-146">Search-Flags</span></span>           | <span data-ttu-id="2c5a6-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c5a6-147">0x00000000</span></span>                                         |
| <span data-ttu-id="2c5a6-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c5a6-148">System-Flags</span></span>           | <span data-ttu-id="2c5a6-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c5a6-149">0x00000010</span></span>                                         |
| <span data-ttu-id="2c5a6-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2c5a6-150">Classes used in</span></span>        | [<span data-ttu-id="2c5a6-151">**Configurações do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="2c5a6-151">**MSMQ-Settings**</span></span>](c-msmqsettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2c5a6-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2c5a6-152">Windows Server 2003</span></span>



| <span data-ttu-id="2c5a6-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="2c5a6-153">Entry</span></span> | <span data-ttu-id="2c5a6-154">Valor</span><span class="sxs-lookup"><span data-stu-id="2c5a6-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="2c5a6-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="2c5a6-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="2c5a6-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c5a6-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="2c5a6-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c5a6-157">System-Only</span></span>            | <span data-ttu-id="2c5a6-158">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-158">False</span></span>                                              |
| <span data-ttu-id="2c5a6-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2c5a6-159">Is-Single-Valued</span></span>       | <span data-ttu-id="2c5a6-160">True</span><span class="sxs-lookup"><span data-stu-id="2c5a6-160">True</span></span>                                               |
| <span data-ttu-id="2c5a6-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="2c5a6-161">Is Indexed</span></span>             | <span data-ttu-id="2c5a6-162">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-162">False</span></span>                                              |
| <span data-ttu-id="2c5a6-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2c5a6-163">In Global Catalog</span></span>      | <span data-ttu-id="2c5a6-164">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-164">False</span></span>                                              |
| <span data-ttu-id="2c5a6-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2c5a6-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c5a6-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2c5a6-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="2c5a6-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c5a6-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="2c5a6-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c5a6-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="2c5a6-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c5a6-169">Search-Flags</span></span>           | <span data-ttu-id="2c5a6-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c5a6-170">0x00000000</span></span>                                         |
| <span data-ttu-id="2c5a6-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c5a6-171">System-Flags</span></span>           | <span data-ttu-id="2c5a6-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c5a6-172">0x00000010</span></span>                                         |
| <span data-ttu-id="2c5a6-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2c5a6-173">Classes used in</span></span>        | [<span data-ttu-id="2c5a6-174">**Configurações do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="2c5a6-174">**MSMQ-Settings**</span></span>](c-msmqsettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2c5a6-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2c5a6-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2c5a6-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="2c5a6-176">Entry</span></span> | <span data-ttu-id="2c5a6-177">Valor</span><span class="sxs-lookup"><span data-stu-id="2c5a6-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="2c5a6-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="2c5a6-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="2c5a6-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c5a6-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="2c5a6-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c5a6-180">System-Only</span></span>            | <span data-ttu-id="2c5a6-181">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-181">False</span></span>                                              |
| <span data-ttu-id="2c5a6-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2c5a6-182">Is-Single-Valued</span></span>       | <span data-ttu-id="2c5a6-183">True</span><span class="sxs-lookup"><span data-stu-id="2c5a6-183">True</span></span>                                               |
| <span data-ttu-id="2c5a6-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="2c5a6-184">Is Indexed</span></span>             | <span data-ttu-id="2c5a6-185">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-185">False</span></span>                                              |
| <span data-ttu-id="2c5a6-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2c5a6-186">In Global Catalog</span></span>      | <span data-ttu-id="2c5a6-187">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-187">False</span></span>                                              |
| <span data-ttu-id="2c5a6-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2c5a6-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c5a6-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2c5a6-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="2c5a6-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c5a6-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="2c5a6-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c5a6-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="2c5a6-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c5a6-192">Search-Flags</span></span>           | <span data-ttu-id="2c5a6-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c5a6-193">0x00000000</span></span>                                         |
| <span data-ttu-id="2c5a6-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c5a6-194">System-Flags</span></span>           | <span data-ttu-id="2c5a6-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c5a6-195">0x00000010</span></span>                                         |
| <span data-ttu-id="2c5a6-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2c5a6-196">Classes used in</span></span>        | [<span data-ttu-id="2c5a6-197">**Configurações do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="2c5a6-197">**MSMQ-Settings**</span></span>](c-msmqsettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2c5a6-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c5a6-198">Windows Server 2008</span></span>



| <span data-ttu-id="2c5a6-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="2c5a6-199">Entry</span></span> | <span data-ttu-id="2c5a6-200">Valor</span><span class="sxs-lookup"><span data-stu-id="2c5a6-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="2c5a6-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="2c5a6-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="2c5a6-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c5a6-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="2c5a6-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c5a6-203">System-Only</span></span>            | <span data-ttu-id="2c5a6-204">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-204">False</span></span>                                              |
| <span data-ttu-id="2c5a6-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2c5a6-205">Is-Single-Valued</span></span>       | <span data-ttu-id="2c5a6-206">True</span><span class="sxs-lookup"><span data-stu-id="2c5a6-206">True</span></span>                                               |
| <span data-ttu-id="2c5a6-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="2c5a6-207">Is Indexed</span></span>             | <span data-ttu-id="2c5a6-208">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-208">False</span></span>                                              |
| <span data-ttu-id="2c5a6-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2c5a6-209">In Global Catalog</span></span>      | <span data-ttu-id="2c5a6-210">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-210">False</span></span>                                              |
| <span data-ttu-id="2c5a6-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2c5a6-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c5a6-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2c5a6-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="2c5a6-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c5a6-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="2c5a6-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c5a6-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="2c5a6-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c5a6-215">Search-Flags</span></span>           | <span data-ttu-id="2c5a6-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c5a6-216">0x00000000</span></span>                                         |
| <span data-ttu-id="2c5a6-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c5a6-217">System-Flags</span></span>           | <span data-ttu-id="2c5a6-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c5a6-218">0x00000010</span></span>                                         |
| <span data-ttu-id="2c5a6-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2c5a6-219">Classes used in</span></span>        | [<span data-ttu-id="2c5a6-220">**Configurações do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="2c5a6-220">**MSMQ-Settings**</span></span>](c-msmqsettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2c5a6-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2c5a6-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2c5a6-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="2c5a6-222">Entry</span></span> | <span data-ttu-id="2c5a6-223">Valor</span><span class="sxs-lookup"><span data-stu-id="2c5a6-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="2c5a6-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="2c5a6-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="2c5a6-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c5a6-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="2c5a6-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c5a6-226">System-Only</span></span>            | <span data-ttu-id="2c5a6-227">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-227">False</span></span>                                              |
| <span data-ttu-id="2c5a6-228">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2c5a6-228">Is-Single-Valued</span></span>       | <span data-ttu-id="2c5a6-229">True</span><span class="sxs-lookup"><span data-stu-id="2c5a6-229">True</span></span>                                               |
| <span data-ttu-id="2c5a6-230">É indexado</span><span class="sxs-lookup"><span data-stu-id="2c5a6-230">Is Indexed</span></span>             | <span data-ttu-id="2c5a6-231">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-231">False</span></span>                                              |
| <span data-ttu-id="2c5a6-232">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2c5a6-232">In Global Catalog</span></span>      | <span data-ttu-id="2c5a6-233">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-233">False</span></span>                                              |
| <span data-ttu-id="2c5a6-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2c5a6-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c5a6-235">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2c5a6-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="2c5a6-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c5a6-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="2c5a6-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c5a6-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="2c5a6-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c5a6-238">Search-Flags</span></span>           | <span data-ttu-id="2c5a6-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c5a6-239">0x00000000</span></span>                                         |
| <span data-ttu-id="2c5a6-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c5a6-240">System-Flags</span></span>           | <span data-ttu-id="2c5a6-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c5a6-241">0x00000010</span></span>                                         |
| <span data-ttu-id="2c5a6-242">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2c5a6-242">Classes used in</span></span>        | [<span data-ttu-id="2c5a6-243">**Configurações do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="2c5a6-243">**MSMQ-Settings**</span></span>](c-msmqsettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2c5a6-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c5a6-244">Windows Server 2012</span></span>



| <span data-ttu-id="2c5a6-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="2c5a6-245">Entry</span></span> | <span data-ttu-id="2c5a6-246">Valor</span><span class="sxs-lookup"><span data-stu-id="2c5a6-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="2c5a6-247">ID do link</span><span class="sxs-lookup"><span data-stu-id="2c5a6-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="2c5a6-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c5a6-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="2c5a6-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c5a6-249">System-Only</span></span>            | <span data-ttu-id="2c5a6-250">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-250">False</span></span>                                              |
| <span data-ttu-id="2c5a6-251">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2c5a6-251">Is-Single-Valued</span></span>       | <span data-ttu-id="2c5a6-252">True</span><span class="sxs-lookup"><span data-stu-id="2c5a6-252">True</span></span>                                               |
| <span data-ttu-id="2c5a6-253">É indexado</span><span class="sxs-lookup"><span data-stu-id="2c5a6-253">Is Indexed</span></span>             | <span data-ttu-id="2c5a6-254">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-254">False</span></span>                                              |
| <span data-ttu-id="2c5a6-255">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2c5a6-255">In Global Catalog</span></span>      | <span data-ttu-id="2c5a6-256">Falso</span><span class="sxs-lookup"><span data-stu-id="2c5a6-256">False</span></span>                                              |
| <span data-ttu-id="2c5a6-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2c5a6-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c5a6-258">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2c5a6-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="2c5a6-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c5a6-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="2c5a6-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c5a6-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="2c5a6-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c5a6-261">Search-Flags</span></span>           | <span data-ttu-id="2c5a6-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c5a6-262">0x00000000</span></span>                                         |
| <span data-ttu-id="2c5a6-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c5a6-263">System-Flags</span></span>           | <span data-ttu-id="2c5a6-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c5a6-264">0x00000010</span></span>                                         |
| <span data-ttu-id="2c5a6-265">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2c5a6-265">Classes used in</span></span>        | [<span data-ttu-id="2c5a6-266">**Configurações do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="2c5a6-266">**MSMQ-Settings**</span></span>](c-msmqsettings.md)<br/> |



 

 





