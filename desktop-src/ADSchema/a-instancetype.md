---
title: Instance-Type atributo
description: Um campo de bits que determina como o objeto é instanciado em um servidor específico.
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- Esquema de Instance-Type do atributo AD
- atributo do AD de atributos InstanceType
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e31eec3c5a7a189f4623e8e77badb3b1e83e0cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645483"
---
# <a name="instance-type-attribute"></a><span data-ttu-id="f8ce9-105">Instance-Type atributo</span><span class="sxs-lookup"><span data-stu-id="f8ce9-105">Instance-Type attribute</span></span>

<span data-ttu-id="f8ce9-106">Um campo de bits que determina como o objeto é instanciado em um servidor específico.</span><span class="sxs-lookup"><span data-stu-id="f8ce9-106">A bitfield that dictates how the object is instantiated on a particular server.</span></span> <span data-ttu-id="f8ce9-107">O valor desse atributo pode diferir em réplicas diferentes, mesmo que as réplicas estejam em sincronia.</span><span class="sxs-lookup"><span data-stu-id="f8ce9-107">The value of this attribute can differ on different replicas even if the replicas are in sync.</span></span>

<span data-ttu-id="f8ce9-108">Esse atributo pode ser zero ou uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f8ce9-108">This attribute can be zero or a combination of one or more of the following values.</span></span>

| <span data-ttu-id="f8ce9-109">Valor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-109">Value</span></span>      | <span data-ttu-id="f8ce9-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8ce9-110">Description</span></span>                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ce9-111">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f8ce9-111">0x00000001</span></span> | <span data-ttu-id="f8ce9-112">O cabeçalho do contexto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="f8ce9-112">The head of naming context.</span></span>                                                                        |
| <span data-ttu-id="f8ce9-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f8ce9-113">0x00000002</span></span> | <span data-ttu-id="f8ce9-114">Esta réplica não está instanciada.</span><span class="sxs-lookup"><span data-stu-id="f8ce9-114">This replica is not instantiated.</span></span>                                                                  |
| <span data-ttu-id="f8ce9-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="f8ce9-115">0x00000004</span></span> | <span data-ttu-id="f8ce9-116">O objeto é gravável neste diretório.</span><span class="sxs-lookup"><span data-stu-id="f8ce9-116">The object is writable on this directory.</span></span>                                                          |
| <span data-ttu-id="f8ce9-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f8ce9-117">0x00000008</span></span> | <span data-ttu-id="f8ce9-118">O contexto de nomenclatura acima deste diretório é mantido.</span><span class="sxs-lookup"><span data-stu-id="f8ce9-118">The naming context above this one on this directory is held.</span></span>                                       |
| <span data-ttu-id="f8ce9-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8ce9-119">0x00000010</span></span> | <span data-ttu-id="f8ce9-120">O contexto de nomenclatura está no processo de ser construído pela primeira vez usando a replicação.</span><span class="sxs-lookup"><span data-stu-id="f8ce9-120">The naming context is in the process of being constructed for the first time by using replication.</span></span> |
| <span data-ttu-id="f8ce9-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="f8ce9-121">0x00000020</span></span> | <span data-ttu-id="f8ce9-122">O contexto de nomenclatura está no processo de ser removido do DSA local.</span><span class="sxs-lookup"><span data-stu-id="f8ce9-122">The naming context is in the process of being removed from the local DSA.</span></span>                          |



 



| <span data-ttu-id="f8ce9-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8ce9-123">Entry</span></span> | <span data-ttu-id="f8ce9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-124">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="f8ce9-125">CN</span><span class="sxs-lookup"><span data-stu-id="f8ce9-125">CN</span></span>                | <span data-ttu-id="f8ce9-126">Instance-Type</span><span class="sxs-lookup"><span data-stu-id="f8ce9-126">Instance-Type</span></span>                                  |
| <span data-ttu-id="f8ce9-127">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f8ce9-127">Ldap-Display-Name</span></span> | <span data-ttu-id="f8ce9-128">instanceType</span><span class="sxs-lookup"><span data-stu-id="f8ce9-128">instanceType</span></span>                                   |
| <span data-ttu-id="f8ce9-129">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f8ce9-129">Size</span></span>              | <span data-ttu-id="f8ce9-130">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="f8ce9-130">4 bytes.</span></span>                                       |
| <span data-ttu-id="f8ce9-131">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f8ce9-131">Update Privilege</span></span>  | <span data-ttu-id="f8ce9-132">Esse valor é definido pelo administrador do esquema.</span><span class="sxs-lookup"><span data-stu-id="f8ce9-132">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="f8ce9-133">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f8ce9-133">Update Frequency</span></span>  | <span data-ttu-id="f8ce9-134">Quando o objeto é criado.</span><span class="sxs-lookup"><span data-stu-id="f8ce9-134">When the object is created.</span></span>                    |
| <span data-ttu-id="f8ce9-135">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f8ce9-135">Attribute-Id</span></span>      | <span data-ttu-id="f8ce9-136">1.2.840.113556.1.2.1</span><span class="sxs-lookup"><span data-stu-id="f8ce9-136">1.2.840.113556.1.2.1</span></span>                           |
| <span data-ttu-id="f8ce9-137">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f8ce9-137">System-Id-Guid</span></span>    | <span data-ttu-id="f8ce9-138">bf96798c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f8ce9-138">bf96798c-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="f8ce9-139">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8ce9-139">Syntax</span></span>            | [<span data-ttu-id="f8ce9-140">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="f8ce9-140">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="f8ce9-141">Implementações</span><span class="sxs-lookup"><span data-stu-id="f8ce9-141">Implementations</span></span>

-   [<span data-ttu-id="f8ce9-142">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f8ce9-142">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f8ce9-143">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f8ce9-143">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f8ce9-144">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f8ce9-144">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f8ce9-145">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f8ce9-145">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f8ce9-146">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f8ce9-146">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f8ce9-147">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f8ce9-147">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f8ce9-148">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f8ce9-148">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f8ce9-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f8ce9-149">Windows 2000 Server</span></span>



| <span data-ttu-id="f8ce9-150">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8ce9-150">Entry</span></span> | <span data-ttu-id="f8ce9-151">Valor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-151">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f8ce9-152">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8ce9-152">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f8ce9-153">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8ce9-153">MAPI-Id</span></span>                | <span data-ttu-id="f8ce9-154">0x80BD</span><span class="sxs-lookup"><span data-stu-id="f8ce9-154">0x80BD</span></span>                          |
| <span data-ttu-id="f8ce9-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8ce9-155">System-Only</span></span>            | <span data-ttu-id="f8ce9-156">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-156">True</span></span>                            |
| <span data-ttu-id="f8ce9-157">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8ce9-157">Is-Single-Valued</span></span>       | <span data-ttu-id="f8ce9-158">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-158">True</span></span>                            |
| <span data-ttu-id="f8ce9-159">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8ce9-159">Is Indexed</span></span>             | <span data-ttu-id="f8ce9-160">Falso</span><span class="sxs-lookup"><span data-stu-id="f8ce9-160">False</span></span>                           |
| <span data-ttu-id="f8ce9-161">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8ce9-161">In Global Catalog</span></span>      | <span data-ttu-id="f8ce9-162">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-162">True</span></span>                            |
| <span data-ttu-id="f8ce9-163">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8ce9-164">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8ce9-164">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f8ce9-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8ce9-165">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f8ce9-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8ce9-166">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f8ce9-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ce9-167">Search-Flags</span></span>           | <span data-ttu-id="f8ce9-168">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f8ce9-168">0x00000008</span></span>                      |
| <span data-ttu-id="f8ce9-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ce9-169">System-Flags</span></span>           | <span data-ttu-id="f8ce9-170">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f8ce9-170">0x00000012</span></span>                      |
| <span data-ttu-id="f8ce9-171">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8ce9-171">Classes used in</span></span>        | [<span data-ttu-id="f8ce9-172">**Início**</span><span class="sxs-lookup"><span data-stu-id="f8ce9-172">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f8ce9-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f8ce9-173">Windows Server 2003</span></span>



| <span data-ttu-id="f8ce9-174">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8ce9-174">Entry</span></span> | <span data-ttu-id="f8ce9-175">Valor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-175">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f8ce9-176">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8ce9-176">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f8ce9-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8ce9-177">MAPI-Id</span></span>                | <span data-ttu-id="f8ce9-178">0x80BD</span><span class="sxs-lookup"><span data-stu-id="f8ce9-178">0x80BD</span></span>                          |
| <span data-ttu-id="f8ce9-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8ce9-179">System-Only</span></span>            | <span data-ttu-id="f8ce9-180">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-180">True</span></span>                            |
| <span data-ttu-id="f8ce9-181">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8ce9-181">Is-Single-Valued</span></span>       | <span data-ttu-id="f8ce9-182">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-182">True</span></span>                            |
| <span data-ttu-id="f8ce9-183">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8ce9-183">Is Indexed</span></span>             | <span data-ttu-id="f8ce9-184">Falso</span><span class="sxs-lookup"><span data-stu-id="f8ce9-184">False</span></span>                           |
| <span data-ttu-id="f8ce9-185">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8ce9-185">In Global Catalog</span></span>      | <span data-ttu-id="f8ce9-186">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-186">True</span></span>                            |
| <span data-ttu-id="f8ce9-187">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8ce9-188">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8ce9-188">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f8ce9-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8ce9-189">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f8ce9-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8ce9-190">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f8ce9-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ce9-191">Search-Flags</span></span>           | <span data-ttu-id="f8ce9-192">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f8ce9-192">0x00000008</span></span>                      |
| <span data-ttu-id="f8ce9-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ce9-193">System-Flags</span></span>           | <span data-ttu-id="f8ce9-194">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f8ce9-194">0x00000012</span></span>                      |
| <span data-ttu-id="f8ce9-195">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8ce9-195">Classes used in</span></span>        | [<span data-ttu-id="f8ce9-196">**Início**</span><span class="sxs-lookup"><span data-stu-id="f8ce9-196">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f8ce9-197">ADAM</span><span class="sxs-lookup"><span data-stu-id="f8ce9-197">ADAM</span></span>



| <span data-ttu-id="f8ce9-198">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8ce9-198">Entry</span></span> | <span data-ttu-id="f8ce9-199">Valor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-199">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f8ce9-200">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8ce9-200">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f8ce9-201">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8ce9-201">MAPI-Id</span></span>                | <span data-ttu-id="f8ce9-202">0x80BD</span><span class="sxs-lookup"><span data-stu-id="f8ce9-202">0x80BD</span></span>                          |
| <span data-ttu-id="f8ce9-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8ce9-203">System-Only</span></span>            | <span data-ttu-id="f8ce9-204">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-204">True</span></span>                            |
| <span data-ttu-id="f8ce9-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8ce9-205">Is-Single-Valued</span></span>       | <span data-ttu-id="f8ce9-206">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-206">True</span></span>                            |
| <span data-ttu-id="f8ce9-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8ce9-207">Is Indexed</span></span>             | <span data-ttu-id="f8ce9-208">Falso</span><span class="sxs-lookup"><span data-stu-id="f8ce9-208">False</span></span>                           |
| <span data-ttu-id="f8ce9-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8ce9-209">In Global Catalog</span></span>      | <span data-ttu-id="f8ce9-210">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-210">True</span></span>                            |
| <span data-ttu-id="f8ce9-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8ce9-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8ce9-212">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f8ce9-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8ce9-213">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f8ce9-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8ce9-214">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f8ce9-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ce9-215">Search-Flags</span></span>           | <span data-ttu-id="f8ce9-216">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f8ce9-216">0x00000008</span></span>                      |
| <span data-ttu-id="f8ce9-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ce9-217">System-Flags</span></span>           | <span data-ttu-id="f8ce9-218">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f8ce9-218">0x00000012</span></span>                      |
| <span data-ttu-id="f8ce9-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8ce9-219">Classes used in</span></span>        | [<span data-ttu-id="f8ce9-220">**Início**</span><span class="sxs-lookup"><span data-stu-id="f8ce9-220">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f8ce9-221">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f8ce9-221">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f8ce9-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8ce9-222">Entry</span></span> | <span data-ttu-id="f8ce9-223">Valor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-223">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f8ce9-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8ce9-224">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f8ce9-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8ce9-225">MAPI-Id</span></span>                | <span data-ttu-id="f8ce9-226">0x80BD</span><span class="sxs-lookup"><span data-stu-id="f8ce9-226">0x80BD</span></span>                          |
| <span data-ttu-id="f8ce9-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8ce9-227">System-Only</span></span>            | <span data-ttu-id="f8ce9-228">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-228">True</span></span>                            |
| <span data-ttu-id="f8ce9-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8ce9-229">Is-Single-Valued</span></span>       | <span data-ttu-id="f8ce9-230">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-230">True</span></span>                            |
| <span data-ttu-id="f8ce9-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8ce9-231">Is Indexed</span></span>             | <span data-ttu-id="f8ce9-232">Falso</span><span class="sxs-lookup"><span data-stu-id="f8ce9-232">False</span></span>                           |
| <span data-ttu-id="f8ce9-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8ce9-233">In Global Catalog</span></span>      | <span data-ttu-id="f8ce9-234">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-234">True</span></span>                            |
| <span data-ttu-id="f8ce9-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8ce9-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8ce9-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f8ce9-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8ce9-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f8ce9-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8ce9-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f8ce9-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ce9-239">Search-Flags</span></span>           | <span data-ttu-id="f8ce9-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f8ce9-240">0x00000008</span></span>                      |
| <span data-ttu-id="f8ce9-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ce9-241">System-Flags</span></span>           | <span data-ttu-id="f8ce9-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f8ce9-242">0x00000012</span></span>                      |
| <span data-ttu-id="f8ce9-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8ce9-243">Classes used in</span></span>        | [<span data-ttu-id="f8ce9-244">**Início**</span><span class="sxs-lookup"><span data-stu-id="f8ce9-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f8ce9-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8ce9-245">Windows Server 2008</span></span>



| <span data-ttu-id="f8ce9-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8ce9-246">Entry</span></span> | <span data-ttu-id="f8ce9-247">Valor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f8ce9-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8ce9-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f8ce9-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8ce9-249">MAPI-Id</span></span>                | <span data-ttu-id="f8ce9-250">0x80BD</span><span class="sxs-lookup"><span data-stu-id="f8ce9-250">0x80BD</span></span>                          |
| <span data-ttu-id="f8ce9-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8ce9-251">System-Only</span></span>            | <span data-ttu-id="f8ce9-252">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-252">True</span></span>                            |
| <span data-ttu-id="f8ce9-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8ce9-253">Is-Single-Valued</span></span>       | <span data-ttu-id="f8ce9-254">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-254">True</span></span>                            |
| <span data-ttu-id="f8ce9-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8ce9-255">Is Indexed</span></span>             | <span data-ttu-id="f8ce9-256">Falso</span><span class="sxs-lookup"><span data-stu-id="f8ce9-256">False</span></span>                           |
| <span data-ttu-id="f8ce9-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8ce9-257">In Global Catalog</span></span>      | <span data-ttu-id="f8ce9-258">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-258">True</span></span>                            |
| <span data-ttu-id="f8ce9-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8ce9-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8ce9-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f8ce9-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8ce9-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f8ce9-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8ce9-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f8ce9-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ce9-263">Search-Flags</span></span>           | <span data-ttu-id="f8ce9-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f8ce9-264">0x00000008</span></span>                      |
| <span data-ttu-id="f8ce9-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ce9-265">System-Flags</span></span>           | <span data-ttu-id="f8ce9-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f8ce9-266">0x00000012</span></span>                      |
| <span data-ttu-id="f8ce9-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8ce9-267">Classes used in</span></span>        | [<span data-ttu-id="f8ce9-268">**Início**</span><span class="sxs-lookup"><span data-stu-id="f8ce9-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f8ce9-269">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f8ce9-269">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f8ce9-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8ce9-270">Entry</span></span> | <span data-ttu-id="f8ce9-271">Valor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f8ce9-272">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8ce9-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f8ce9-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8ce9-273">MAPI-Id</span></span>                | <span data-ttu-id="f8ce9-274">0x80BD</span><span class="sxs-lookup"><span data-stu-id="f8ce9-274">0x80BD</span></span>                          |
| <span data-ttu-id="f8ce9-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8ce9-275">System-Only</span></span>            | <span data-ttu-id="f8ce9-276">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-276">True</span></span>                            |
| <span data-ttu-id="f8ce9-277">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8ce9-277">Is-Single-Valued</span></span>       | <span data-ttu-id="f8ce9-278">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-278">True</span></span>                            |
| <span data-ttu-id="f8ce9-279">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8ce9-279">Is Indexed</span></span>             | <span data-ttu-id="f8ce9-280">Falso</span><span class="sxs-lookup"><span data-stu-id="f8ce9-280">False</span></span>                           |
| <span data-ttu-id="f8ce9-281">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8ce9-281">In Global Catalog</span></span>      | <span data-ttu-id="f8ce9-282">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-282">True</span></span>                            |
| <span data-ttu-id="f8ce9-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8ce9-284">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8ce9-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f8ce9-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8ce9-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f8ce9-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8ce9-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f8ce9-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ce9-287">Search-Flags</span></span>           | <span data-ttu-id="f8ce9-288">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f8ce9-288">0x00000008</span></span>                      |
| <span data-ttu-id="f8ce9-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ce9-289">System-Flags</span></span>           | <span data-ttu-id="f8ce9-290">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f8ce9-290">0x00000012</span></span>                      |
| <span data-ttu-id="f8ce9-291">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8ce9-291">Classes used in</span></span>        | [<span data-ttu-id="f8ce9-292">**Início**</span><span class="sxs-lookup"><span data-stu-id="f8ce9-292">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f8ce9-293">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f8ce9-293">Windows Server 2012</span></span>



| <span data-ttu-id="f8ce9-294">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8ce9-294">Entry</span></span> | <span data-ttu-id="f8ce9-295">Valor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-295">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f8ce9-296">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8ce9-296">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f8ce9-297">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8ce9-297">MAPI-Id</span></span>                | <span data-ttu-id="f8ce9-298">0x80BD</span><span class="sxs-lookup"><span data-stu-id="f8ce9-298">0x80BD</span></span>                          |
| <span data-ttu-id="f8ce9-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8ce9-299">System-Only</span></span>            | <span data-ttu-id="f8ce9-300">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-300">True</span></span>                            |
| <span data-ttu-id="f8ce9-301">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8ce9-301">Is-Single-Valued</span></span>       | <span data-ttu-id="f8ce9-302">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-302">True</span></span>                            |
| <span data-ttu-id="f8ce9-303">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8ce9-303">Is Indexed</span></span>             | <span data-ttu-id="f8ce9-304">Falso</span><span class="sxs-lookup"><span data-stu-id="f8ce9-304">False</span></span>                           |
| <span data-ttu-id="f8ce9-305">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8ce9-305">In Global Catalog</span></span>      | <span data-ttu-id="f8ce9-306">True</span><span class="sxs-lookup"><span data-stu-id="f8ce9-306">True</span></span>                            |
| <span data-ttu-id="f8ce9-307">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8ce9-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8ce9-308">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8ce9-308">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f8ce9-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8ce9-309">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f8ce9-310">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8ce9-310">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f8ce9-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ce9-311">Search-Flags</span></span>           | <span data-ttu-id="f8ce9-312">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f8ce9-312">0x00000008</span></span>                      |
| <span data-ttu-id="f8ce9-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8ce9-313">System-Flags</span></span>           | <span data-ttu-id="f8ce9-314">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f8ce9-314">0x00000012</span></span>                      |
| <span data-ttu-id="f8ce9-315">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8ce9-315">Classes used in</span></span>        | [<span data-ttu-id="f8ce9-316">**Início**</span><span class="sxs-lookup"><span data-stu-id="f8ce9-316">**Top**</span></span>](c-top.md)<br/> |



 

 





