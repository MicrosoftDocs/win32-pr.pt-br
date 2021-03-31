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
# <a name="instance-type-attribute"></a><span data-ttu-id="df0e7-105">Instance-Type atributo</span><span class="sxs-lookup"><span data-stu-id="df0e7-105">Instance-Type attribute</span></span>

<span data-ttu-id="df0e7-106">Um campo de bits que determina como o objeto é instanciado em um servidor específico.</span><span class="sxs-lookup"><span data-stu-id="df0e7-106">A bitfield that dictates how the object is instantiated on a particular server.</span></span> <span data-ttu-id="df0e7-107">O valor desse atributo pode diferir em réplicas diferentes, mesmo que as réplicas estejam em sincronia.</span><span class="sxs-lookup"><span data-stu-id="df0e7-107">The value of this attribute can differ on different replicas even if the replicas are in sync.</span></span>

<span data-ttu-id="df0e7-108">Esse atributo pode ser zero ou uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="df0e7-108">This attribute can be zero or a combination of one or more of the following values.</span></span>

| <span data-ttu-id="df0e7-109">Valor</span><span class="sxs-lookup"><span data-stu-id="df0e7-109">Value</span></span>      | <span data-ttu-id="df0e7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="df0e7-110">Description</span></span>                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df0e7-111">0x00000001</span><span class="sxs-lookup"><span data-stu-id="df0e7-111">0x00000001</span></span> | <span data-ttu-id="df0e7-112">O cabeçalho do contexto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="df0e7-112">The head of naming context.</span></span>                                                                        |
| <span data-ttu-id="df0e7-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="df0e7-113">0x00000002</span></span> | <span data-ttu-id="df0e7-114">Esta réplica não está instanciada.</span><span class="sxs-lookup"><span data-stu-id="df0e7-114">This replica is not instantiated.</span></span>                                                                  |
| <span data-ttu-id="df0e7-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="df0e7-115">0x00000004</span></span> | <span data-ttu-id="df0e7-116">O objeto é gravável neste diretório.</span><span class="sxs-lookup"><span data-stu-id="df0e7-116">The object is writable on this directory.</span></span>                                                          |
| <span data-ttu-id="df0e7-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="df0e7-117">0x00000008</span></span> | <span data-ttu-id="df0e7-118">O contexto de nomenclatura acima deste diretório é mantido.</span><span class="sxs-lookup"><span data-stu-id="df0e7-118">The naming context above this one on this directory is held.</span></span>                                       |
| <span data-ttu-id="df0e7-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df0e7-119">0x00000010</span></span> | <span data-ttu-id="df0e7-120">O contexto de nomenclatura está no processo de ser construído pela primeira vez usando a replicação.</span><span class="sxs-lookup"><span data-stu-id="df0e7-120">The naming context is in the process of being constructed for the first time by using replication.</span></span> |
| <span data-ttu-id="df0e7-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="df0e7-121">0x00000020</span></span> | <span data-ttu-id="df0e7-122">O contexto de nomenclatura está no processo de ser removido do DSA local.</span><span class="sxs-lookup"><span data-stu-id="df0e7-122">The naming context is in the process of being removed from the local DSA.</span></span>                          |



 



| <span data-ttu-id="df0e7-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="df0e7-123">Entry</span></span> | <span data-ttu-id="df0e7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="df0e7-124">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="df0e7-125">CN</span><span class="sxs-lookup"><span data-stu-id="df0e7-125">CN</span></span>                | <span data-ttu-id="df0e7-126">Instance-Type</span><span class="sxs-lookup"><span data-stu-id="df0e7-126">Instance-Type</span></span>                                  |
| <span data-ttu-id="df0e7-127">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="df0e7-127">Ldap-Display-Name</span></span> | <span data-ttu-id="df0e7-128">instanceType</span><span class="sxs-lookup"><span data-stu-id="df0e7-128">instanceType</span></span>                                   |
| <span data-ttu-id="df0e7-129">Tamanho</span><span class="sxs-lookup"><span data-stu-id="df0e7-129">Size</span></span>              | <span data-ttu-id="df0e7-130">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="df0e7-130">4 bytes.</span></span>                                       |
| <span data-ttu-id="df0e7-131">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="df0e7-131">Update Privilege</span></span>  | <span data-ttu-id="df0e7-132">Esse valor é definido pelo administrador do esquema.</span><span class="sxs-lookup"><span data-stu-id="df0e7-132">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="df0e7-133">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="df0e7-133">Update Frequency</span></span>  | <span data-ttu-id="df0e7-134">Quando o objeto é criado.</span><span class="sxs-lookup"><span data-stu-id="df0e7-134">When the object is created.</span></span>                    |
| <span data-ttu-id="df0e7-135">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="df0e7-135">Attribute-Id</span></span>      | <span data-ttu-id="df0e7-136">1.2.840.113556.1.2.1</span><span class="sxs-lookup"><span data-stu-id="df0e7-136">1.2.840.113556.1.2.1</span></span>                           |
| <span data-ttu-id="df0e7-137">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="df0e7-137">System-Id-Guid</span></span>    | <span data-ttu-id="df0e7-138">bf96798c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="df0e7-138">bf96798c-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="df0e7-139">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df0e7-139">Syntax</span></span>            | [<span data-ttu-id="df0e7-140">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="df0e7-140">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="df0e7-141">Implementações</span><span class="sxs-lookup"><span data-stu-id="df0e7-141">Implementations</span></span>

-   [<span data-ttu-id="df0e7-142">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="df0e7-142">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="df0e7-143">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="df0e7-143">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="df0e7-144">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="df0e7-144">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="df0e7-145">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="df0e7-145">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="df0e7-146">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="df0e7-146">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="df0e7-147">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="df0e7-147">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="df0e7-148">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="df0e7-148">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="df0e7-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="df0e7-149">Windows 2000 Server</span></span>



| <span data-ttu-id="df0e7-150">Entrada</span><span class="sxs-lookup"><span data-stu-id="df0e7-150">Entry</span></span> | <span data-ttu-id="df0e7-151">Valor</span><span class="sxs-lookup"><span data-stu-id="df0e7-151">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df0e7-152">ID do link</span><span class="sxs-lookup"><span data-stu-id="df0e7-152">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df0e7-153">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df0e7-153">MAPI-Id</span></span>                | <span data-ttu-id="df0e7-154">0x80BD</span><span class="sxs-lookup"><span data-stu-id="df0e7-154">0x80BD</span></span>                          |
| <span data-ttu-id="df0e7-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="df0e7-155">System-Only</span></span>            | <span data-ttu-id="df0e7-156">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-156">True</span></span>                            |
| <span data-ttu-id="df0e7-157">É de valor único</span><span class="sxs-lookup"><span data-stu-id="df0e7-157">Is-Single-Valued</span></span>       | <span data-ttu-id="df0e7-158">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-158">True</span></span>                            |
| <span data-ttu-id="df0e7-159">É indexado</span><span class="sxs-lookup"><span data-stu-id="df0e7-159">Is Indexed</span></span>             | <span data-ttu-id="df0e7-160">Falso</span><span class="sxs-lookup"><span data-stu-id="df0e7-160">False</span></span>                           |
| <span data-ttu-id="df0e7-161">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="df0e7-161">In Global Catalog</span></span>      | <span data-ttu-id="df0e7-162">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-162">True</span></span>                            |
| <span data-ttu-id="df0e7-163">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df0e7-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="df0e7-164">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="df0e7-164">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df0e7-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df0e7-165">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df0e7-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df0e7-166">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df0e7-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df0e7-167">Search-Flags</span></span>           | <span data-ttu-id="df0e7-168">0x00000008</span><span class="sxs-lookup"><span data-stu-id="df0e7-168">0x00000008</span></span>                      |
| <span data-ttu-id="df0e7-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df0e7-169">System-Flags</span></span>           | <span data-ttu-id="df0e7-170">0x00000012</span><span class="sxs-lookup"><span data-stu-id="df0e7-170">0x00000012</span></span>                      |
| <span data-ttu-id="df0e7-171">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="df0e7-171">Classes used in</span></span>        | [<span data-ttu-id="df0e7-172">**Início**</span><span class="sxs-lookup"><span data-stu-id="df0e7-172">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="df0e7-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="df0e7-173">Windows Server 2003</span></span>



| <span data-ttu-id="df0e7-174">Entrada</span><span class="sxs-lookup"><span data-stu-id="df0e7-174">Entry</span></span> | <span data-ttu-id="df0e7-175">Valor</span><span class="sxs-lookup"><span data-stu-id="df0e7-175">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df0e7-176">ID do link</span><span class="sxs-lookup"><span data-stu-id="df0e7-176">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df0e7-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df0e7-177">MAPI-Id</span></span>                | <span data-ttu-id="df0e7-178">0x80BD</span><span class="sxs-lookup"><span data-stu-id="df0e7-178">0x80BD</span></span>                          |
| <span data-ttu-id="df0e7-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="df0e7-179">System-Only</span></span>            | <span data-ttu-id="df0e7-180">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-180">True</span></span>                            |
| <span data-ttu-id="df0e7-181">É de valor único</span><span class="sxs-lookup"><span data-stu-id="df0e7-181">Is-Single-Valued</span></span>       | <span data-ttu-id="df0e7-182">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-182">True</span></span>                            |
| <span data-ttu-id="df0e7-183">É indexado</span><span class="sxs-lookup"><span data-stu-id="df0e7-183">Is Indexed</span></span>             | <span data-ttu-id="df0e7-184">Falso</span><span class="sxs-lookup"><span data-stu-id="df0e7-184">False</span></span>                           |
| <span data-ttu-id="df0e7-185">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="df0e7-185">In Global Catalog</span></span>      | <span data-ttu-id="df0e7-186">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-186">True</span></span>                            |
| <span data-ttu-id="df0e7-187">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df0e7-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="df0e7-188">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="df0e7-188">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df0e7-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df0e7-189">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df0e7-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df0e7-190">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df0e7-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df0e7-191">Search-Flags</span></span>           | <span data-ttu-id="df0e7-192">0x00000008</span><span class="sxs-lookup"><span data-stu-id="df0e7-192">0x00000008</span></span>                      |
| <span data-ttu-id="df0e7-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df0e7-193">System-Flags</span></span>           | <span data-ttu-id="df0e7-194">0x00000012</span><span class="sxs-lookup"><span data-stu-id="df0e7-194">0x00000012</span></span>                      |
| <span data-ttu-id="df0e7-195">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="df0e7-195">Classes used in</span></span>        | [<span data-ttu-id="df0e7-196">**Início**</span><span class="sxs-lookup"><span data-stu-id="df0e7-196">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="df0e7-197">ADAM</span><span class="sxs-lookup"><span data-stu-id="df0e7-197">ADAM</span></span>



| <span data-ttu-id="df0e7-198">Entrada</span><span class="sxs-lookup"><span data-stu-id="df0e7-198">Entry</span></span> | <span data-ttu-id="df0e7-199">Valor</span><span class="sxs-lookup"><span data-stu-id="df0e7-199">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df0e7-200">ID do link</span><span class="sxs-lookup"><span data-stu-id="df0e7-200">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df0e7-201">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df0e7-201">MAPI-Id</span></span>                | <span data-ttu-id="df0e7-202">0x80BD</span><span class="sxs-lookup"><span data-stu-id="df0e7-202">0x80BD</span></span>                          |
| <span data-ttu-id="df0e7-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="df0e7-203">System-Only</span></span>            | <span data-ttu-id="df0e7-204">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-204">True</span></span>                            |
| <span data-ttu-id="df0e7-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="df0e7-205">Is-Single-Valued</span></span>       | <span data-ttu-id="df0e7-206">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-206">True</span></span>                            |
| <span data-ttu-id="df0e7-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="df0e7-207">Is Indexed</span></span>             | <span data-ttu-id="df0e7-208">Falso</span><span class="sxs-lookup"><span data-stu-id="df0e7-208">False</span></span>                           |
| <span data-ttu-id="df0e7-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="df0e7-209">In Global Catalog</span></span>      | <span data-ttu-id="df0e7-210">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-210">True</span></span>                            |
| <span data-ttu-id="df0e7-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df0e7-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="df0e7-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="df0e7-212">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df0e7-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df0e7-213">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df0e7-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df0e7-214">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df0e7-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df0e7-215">Search-Flags</span></span>           | <span data-ttu-id="df0e7-216">0x00000008</span><span class="sxs-lookup"><span data-stu-id="df0e7-216">0x00000008</span></span>                      |
| <span data-ttu-id="df0e7-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df0e7-217">System-Flags</span></span>           | <span data-ttu-id="df0e7-218">0x00000012</span><span class="sxs-lookup"><span data-stu-id="df0e7-218">0x00000012</span></span>                      |
| <span data-ttu-id="df0e7-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="df0e7-219">Classes used in</span></span>        | [<span data-ttu-id="df0e7-220">**Início**</span><span class="sxs-lookup"><span data-stu-id="df0e7-220">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="df0e7-221">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="df0e7-221">Windows Server 2003 R2</span></span>



| <span data-ttu-id="df0e7-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="df0e7-222">Entry</span></span> | <span data-ttu-id="df0e7-223">Valor</span><span class="sxs-lookup"><span data-stu-id="df0e7-223">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df0e7-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="df0e7-224">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df0e7-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df0e7-225">MAPI-Id</span></span>                | <span data-ttu-id="df0e7-226">0x80BD</span><span class="sxs-lookup"><span data-stu-id="df0e7-226">0x80BD</span></span>                          |
| <span data-ttu-id="df0e7-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="df0e7-227">System-Only</span></span>            | <span data-ttu-id="df0e7-228">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-228">True</span></span>                            |
| <span data-ttu-id="df0e7-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="df0e7-229">Is-Single-Valued</span></span>       | <span data-ttu-id="df0e7-230">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-230">True</span></span>                            |
| <span data-ttu-id="df0e7-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="df0e7-231">Is Indexed</span></span>             | <span data-ttu-id="df0e7-232">Falso</span><span class="sxs-lookup"><span data-stu-id="df0e7-232">False</span></span>                           |
| <span data-ttu-id="df0e7-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="df0e7-233">In Global Catalog</span></span>      | <span data-ttu-id="df0e7-234">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-234">True</span></span>                            |
| <span data-ttu-id="df0e7-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df0e7-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="df0e7-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="df0e7-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df0e7-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df0e7-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df0e7-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df0e7-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df0e7-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df0e7-239">Search-Flags</span></span>           | <span data-ttu-id="df0e7-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="df0e7-240">0x00000008</span></span>                      |
| <span data-ttu-id="df0e7-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df0e7-241">System-Flags</span></span>           | <span data-ttu-id="df0e7-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="df0e7-242">0x00000012</span></span>                      |
| <span data-ttu-id="df0e7-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="df0e7-243">Classes used in</span></span>        | [<span data-ttu-id="df0e7-244">**Início**</span><span class="sxs-lookup"><span data-stu-id="df0e7-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="df0e7-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df0e7-245">Windows Server 2008</span></span>



| <span data-ttu-id="df0e7-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="df0e7-246">Entry</span></span> | <span data-ttu-id="df0e7-247">Valor</span><span class="sxs-lookup"><span data-stu-id="df0e7-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df0e7-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="df0e7-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df0e7-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df0e7-249">MAPI-Id</span></span>                | <span data-ttu-id="df0e7-250">0x80BD</span><span class="sxs-lookup"><span data-stu-id="df0e7-250">0x80BD</span></span>                          |
| <span data-ttu-id="df0e7-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="df0e7-251">System-Only</span></span>            | <span data-ttu-id="df0e7-252">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-252">True</span></span>                            |
| <span data-ttu-id="df0e7-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="df0e7-253">Is-Single-Valued</span></span>       | <span data-ttu-id="df0e7-254">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-254">True</span></span>                            |
| <span data-ttu-id="df0e7-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="df0e7-255">Is Indexed</span></span>             | <span data-ttu-id="df0e7-256">Falso</span><span class="sxs-lookup"><span data-stu-id="df0e7-256">False</span></span>                           |
| <span data-ttu-id="df0e7-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="df0e7-257">In Global Catalog</span></span>      | <span data-ttu-id="df0e7-258">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-258">True</span></span>                            |
| <span data-ttu-id="df0e7-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df0e7-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="df0e7-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="df0e7-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df0e7-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df0e7-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df0e7-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df0e7-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df0e7-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df0e7-263">Search-Flags</span></span>           | <span data-ttu-id="df0e7-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="df0e7-264">0x00000008</span></span>                      |
| <span data-ttu-id="df0e7-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df0e7-265">System-Flags</span></span>           | <span data-ttu-id="df0e7-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="df0e7-266">0x00000012</span></span>                      |
| <span data-ttu-id="df0e7-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="df0e7-267">Classes used in</span></span>        | [<span data-ttu-id="df0e7-268">**Início**</span><span class="sxs-lookup"><span data-stu-id="df0e7-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="df0e7-269">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="df0e7-269">Windows Server 2008 R2</span></span>



| <span data-ttu-id="df0e7-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="df0e7-270">Entry</span></span> | <span data-ttu-id="df0e7-271">Valor</span><span class="sxs-lookup"><span data-stu-id="df0e7-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df0e7-272">ID do link</span><span class="sxs-lookup"><span data-stu-id="df0e7-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df0e7-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df0e7-273">MAPI-Id</span></span>                | <span data-ttu-id="df0e7-274">0x80BD</span><span class="sxs-lookup"><span data-stu-id="df0e7-274">0x80BD</span></span>                          |
| <span data-ttu-id="df0e7-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="df0e7-275">System-Only</span></span>            | <span data-ttu-id="df0e7-276">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-276">True</span></span>                            |
| <span data-ttu-id="df0e7-277">É de valor único</span><span class="sxs-lookup"><span data-stu-id="df0e7-277">Is-Single-Valued</span></span>       | <span data-ttu-id="df0e7-278">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-278">True</span></span>                            |
| <span data-ttu-id="df0e7-279">É indexado</span><span class="sxs-lookup"><span data-stu-id="df0e7-279">Is Indexed</span></span>             | <span data-ttu-id="df0e7-280">Falso</span><span class="sxs-lookup"><span data-stu-id="df0e7-280">False</span></span>                           |
| <span data-ttu-id="df0e7-281">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="df0e7-281">In Global Catalog</span></span>      | <span data-ttu-id="df0e7-282">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-282">True</span></span>                            |
| <span data-ttu-id="df0e7-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df0e7-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="df0e7-284">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="df0e7-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df0e7-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df0e7-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df0e7-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df0e7-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df0e7-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df0e7-287">Search-Flags</span></span>           | <span data-ttu-id="df0e7-288">0x00000008</span><span class="sxs-lookup"><span data-stu-id="df0e7-288">0x00000008</span></span>                      |
| <span data-ttu-id="df0e7-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df0e7-289">System-Flags</span></span>           | <span data-ttu-id="df0e7-290">0x00000012</span><span class="sxs-lookup"><span data-stu-id="df0e7-290">0x00000012</span></span>                      |
| <span data-ttu-id="df0e7-291">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="df0e7-291">Classes used in</span></span>        | [<span data-ttu-id="df0e7-292">**Início**</span><span class="sxs-lookup"><span data-stu-id="df0e7-292">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="df0e7-293">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df0e7-293">Windows Server 2012</span></span>



| <span data-ttu-id="df0e7-294">Entrada</span><span class="sxs-lookup"><span data-stu-id="df0e7-294">Entry</span></span> | <span data-ttu-id="df0e7-295">Valor</span><span class="sxs-lookup"><span data-stu-id="df0e7-295">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df0e7-296">ID do link</span><span class="sxs-lookup"><span data-stu-id="df0e7-296">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df0e7-297">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df0e7-297">MAPI-Id</span></span>                | <span data-ttu-id="df0e7-298">0x80BD</span><span class="sxs-lookup"><span data-stu-id="df0e7-298">0x80BD</span></span>                          |
| <span data-ttu-id="df0e7-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="df0e7-299">System-Only</span></span>            | <span data-ttu-id="df0e7-300">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-300">True</span></span>                            |
| <span data-ttu-id="df0e7-301">É de valor único</span><span class="sxs-lookup"><span data-stu-id="df0e7-301">Is-Single-Valued</span></span>       | <span data-ttu-id="df0e7-302">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-302">True</span></span>                            |
| <span data-ttu-id="df0e7-303">É indexado</span><span class="sxs-lookup"><span data-stu-id="df0e7-303">Is Indexed</span></span>             | <span data-ttu-id="df0e7-304">Falso</span><span class="sxs-lookup"><span data-stu-id="df0e7-304">False</span></span>                           |
| <span data-ttu-id="df0e7-305">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="df0e7-305">In Global Catalog</span></span>      | <span data-ttu-id="df0e7-306">True</span><span class="sxs-lookup"><span data-stu-id="df0e7-306">True</span></span>                            |
| <span data-ttu-id="df0e7-307">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df0e7-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="df0e7-308">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="df0e7-308">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df0e7-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df0e7-309">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df0e7-310">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df0e7-310">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df0e7-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df0e7-311">Search-Flags</span></span>           | <span data-ttu-id="df0e7-312">0x00000008</span><span class="sxs-lookup"><span data-stu-id="df0e7-312">0x00000008</span></span>                      |
| <span data-ttu-id="df0e7-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df0e7-313">System-Flags</span></span>           | <span data-ttu-id="df0e7-314">0x00000012</span><span class="sxs-lookup"><span data-stu-id="df0e7-314">0x00000012</span></span>                      |
| <span data-ttu-id="df0e7-315">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="df0e7-315">Classes used in</span></span>        | [<span data-ttu-id="df0e7-316">**Início**</span><span class="sxs-lookup"><span data-stu-id="df0e7-316">**Top**</span></span>](c-top.md)<br/> |



 

 





