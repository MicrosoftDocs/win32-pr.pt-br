---
title: atributo ms-FRS-Topology-pref
description: O atributo ms-FRS-Topology-pref é usado para registrar as configurações de topologia de NTFRS preferenciais.
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-FRS-Topology-pref
- Esquema de AD de atributos msFRS-Topology-pref
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de417b03385e51d6a97fd68097f81bcc0cb6b9db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645441"
---
# <a name="ms-frs-topology-pref-attribute"></a><span data-ttu-id="37536-105">atributo ms-FRS-Topology-pref</span><span class="sxs-lookup"><span data-stu-id="37536-105">ms-FRS-Topology-Pref attribute</span></span>

<span data-ttu-id="37536-106">O atributo **MS-FRS-Topology-pref** é usado para registrar as configurações de topologia de NTFRS preferenciais.</span><span class="sxs-lookup"><span data-stu-id="37536-106">The **ms-FRS-Topology-Pref** attribute is used to record the preferred NTFRS topology settings.</span></span> <span data-ttu-id="37536-107">Quando um membro do FRS é adicionado ou excluído ao conjunto de réplicas, esses atributos são referenciados e os ajustes feitos nas conexões entre o restante dos membros do FRS no conjunto de réplicas.</span><span class="sxs-lookup"><span data-stu-id="37536-107">When an FRS member gets added or deleted to the replica set, these attributes are referred, and adjustments made to the connections between the rest of the FRS members in the replica set.</span></span>

<span data-ttu-id="37536-108">Os valores válidos para esse atributo são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="37536-108">Valid values for this attribute are as follows.</span></span>

| <span data-ttu-id="37536-109">Valor</span><span class="sxs-lookup"><span data-stu-id="37536-109">Value</span></span> | <span data-ttu-id="37536-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="37536-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="37536-111">1</span><span class="sxs-lookup"><span data-stu-id="37536-111">1</span></span>     | <span data-ttu-id="37536-112">\_anel RSTOPOLOGYPREF do FRS \_</span><span class="sxs-lookup"><span data-stu-id="37536-112">FRS\_RSTOPOLOGYPREF\_RING</span></span><br/>     |
| <span data-ttu-id="37536-113">2</span><span class="sxs-lookup"><span data-stu-id="37536-113">2</span></span>     | <span data-ttu-id="37536-114">\_HUBSPOKE RSTOPOLOGYPREF do FRS \_</span><span class="sxs-lookup"><span data-stu-id="37536-114">FRS\_RSTOPOLOGYPREF\_HUBSPOKE</span></span><br/> |
| <span data-ttu-id="37536-115">3</span><span class="sxs-lookup"><span data-stu-id="37536-115">3</span></span>     | <span data-ttu-id="37536-116">\_FULLMESH RSTOPOLOGYPREF do FRS \_</span><span class="sxs-lookup"><span data-stu-id="37536-116">FRS\_RSTOPOLOGYPREF\_FULLMESH</span></span><br/> |
| <span data-ttu-id="37536-117">4</span><span class="sxs-lookup"><span data-stu-id="37536-117">4</span></span>     | <span data-ttu-id="37536-118">RSTOPOLOGYPREF de FRS \_ \_ personalizado</span><span class="sxs-lookup"><span data-stu-id="37536-118">FRS\_RSTOPOLOGYPREF\_CUSTOM</span></span><br/>   |



 



| <span data-ttu-id="37536-119">Entrada</span><span class="sxs-lookup"><span data-stu-id="37536-119">Entry</span></span> | <span data-ttu-id="37536-120">Valor</span><span class="sxs-lookup"><span data-stu-id="37536-120">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="37536-121">CN</span><span class="sxs-lookup"><span data-stu-id="37536-121">CN</span></span>                | <span data-ttu-id="37536-122">MS-FRS-Topology-pref</span><span class="sxs-lookup"><span data-stu-id="37536-122">ms-FRS-Topology-Pref</span></span>                                               |
| <span data-ttu-id="37536-123">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="37536-123">Ldap-Display-Name</span></span> | <span data-ttu-id="37536-124">msFRS-Topology-pref</span><span class="sxs-lookup"><span data-stu-id="37536-124">msFRS-Topology-Pref</span></span>                                                |
| <span data-ttu-id="37536-125">Tamanho</span><span class="sxs-lookup"><span data-stu-id="37536-125">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="37536-126">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="37536-126">Update Privilege</span></span>  | <span data-ttu-id="37536-127">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="37536-127">Domain administrator</span></span>                                               |
| <span data-ttu-id="37536-128">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="37536-128">Update Frequency</span></span>  | <span data-ttu-id="37536-129">Quando o conjunto de réplicas é criado ou a topologia preferida é alterada.</span><span class="sxs-lookup"><span data-stu-id="37536-129">When the replica set is created or the preferred topology changes.</span></span> |
| <span data-ttu-id="37536-130">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="37536-130">Attribute-Id</span></span>      | <span data-ttu-id="37536-131">1.2.840.113556.1.4.1692</span><span class="sxs-lookup"><span data-stu-id="37536-131">1.2.840.113556.1.4.1692</span></span>                                            |
| <span data-ttu-id="37536-132">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="37536-132">System-Id-Guid</span></span>    | <span data-ttu-id="37536-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span><span class="sxs-lookup"><span data-stu-id="37536-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span></span>                               |
| <span data-ttu-id="37536-134">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37536-134">Syntax</span></span>            | [<span data-ttu-id="37536-135">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="37536-135">**String(Unicode)**</span></span>](s-string-unicode.md)                        |



## <a name="implementations"></a><span data-ttu-id="37536-136">Implementações</span><span class="sxs-lookup"><span data-stu-id="37536-136">Implementations</span></span>

-   [<span data-ttu-id="37536-137">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="37536-137">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="37536-138">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="37536-138">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="37536-139">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="37536-139">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="37536-140">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="37536-140">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="37536-141">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="37536-141">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="37536-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37536-142">Windows Server 2003</span></span>



| <span data-ttu-id="37536-143">Entrada</span><span class="sxs-lookup"><span data-stu-id="37536-143">Entry</span></span> | <span data-ttu-id="37536-144">Valor</span><span class="sxs-lookup"><span data-stu-id="37536-144">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="37536-145">ID do link</span><span class="sxs-lookup"><span data-stu-id="37536-145">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="37536-146">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37536-146">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="37536-147">System-Only</span><span class="sxs-lookup"><span data-stu-id="37536-147">System-Only</span></span>            | <span data-ttu-id="37536-148">Falso</span><span class="sxs-lookup"><span data-stu-id="37536-148">False</span></span>                                                     |
| <span data-ttu-id="37536-149">É de valor único</span><span class="sxs-lookup"><span data-stu-id="37536-149">Is-Single-Valued</span></span>       | <span data-ttu-id="37536-150">True</span><span class="sxs-lookup"><span data-stu-id="37536-150">True</span></span>                                                      |
| <span data-ttu-id="37536-151">É indexado</span><span class="sxs-lookup"><span data-stu-id="37536-151">Is Indexed</span></span>             | <span data-ttu-id="37536-152">Falso</span><span class="sxs-lookup"><span data-stu-id="37536-152">False</span></span>                                                     |
| <span data-ttu-id="37536-153">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="37536-153">In Global Catalog</span></span>      | <span data-ttu-id="37536-154">Falso</span><span class="sxs-lookup"><span data-stu-id="37536-154">False</span></span>                                                     |
| <span data-ttu-id="37536-155">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="37536-155">NT-Security-Descriptor</span></span> | <span data-ttu-id="37536-156">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="37536-156">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="37536-157">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37536-157">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="37536-158">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37536-158">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="37536-159">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37536-159">Search-Flags</span></span>           | <span data-ttu-id="37536-160">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37536-160">0x00000000</span></span>                                                |
| <span data-ttu-id="37536-161">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37536-161">System-Flags</span></span>           | <span data-ttu-id="37536-162">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37536-162">0x00000000</span></span>                                                |
| <span data-ttu-id="37536-163">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="37536-163">Classes used in</span></span>        | [<span data-ttu-id="37536-164">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="37536-164">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="37536-165">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="37536-165">Windows Server 2003 R2</span></span>



| <span data-ttu-id="37536-166">Entrada</span><span class="sxs-lookup"><span data-stu-id="37536-166">Entry</span></span> | <span data-ttu-id="37536-167">Valor</span><span class="sxs-lookup"><span data-stu-id="37536-167">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="37536-168">ID do link</span><span class="sxs-lookup"><span data-stu-id="37536-168">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="37536-169">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37536-169">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="37536-170">System-Only</span><span class="sxs-lookup"><span data-stu-id="37536-170">System-Only</span></span>            | <span data-ttu-id="37536-171">Falso</span><span class="sxs-lookup"><span data-stu-id="37536-171">False</span></span>                                                     |
| <span data-ttu-id="37536-172">É de valor único</span><span class="sxs-lookup"><span data-stu-id="37536-172">Is-Single-Valued</span></span>       | <span data-ttu-id="37536-173">True</span><span class="sxs-lookup"><span data-stu-id="37536-173">True</span></span>                                                      |
| <span data-ttu-id="37536-174">É indexado</span><span class="sxs-lookup"><span data-stu-id="37536-174">Is Indexed</span></span>             | <span data-ttu-id="37536-175">Falso</span><span class="sxs-lookup"><span data-stu-id="37536-175">False</span></span>                                                     |
| <span data-ttu-id="37536-176">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="37536-176">In Global Catalog</span></span>      | <span data-ttu-id="37536-177">Falso</span><span class="sxs-lookup"><span data-stu-id="37536-177">False</span></span>                                                     |
| <span data-ttu-id="37536-178">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="37536-178">NT-Security-Descriptor</span></span> | <span data-ttu-id="37536-179">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="37536-179">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="37536-180">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37536-180">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="37536-181">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37536-181">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="37536-182">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37536-182">Search-Flags</span></span>           | <span data-ttu-id="37536-183">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37536-183">0x00000000</span></span>                                                |
| <span data-ttu-id="37536-184">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37536-184">System-Flags</span></span>           | <span data-ttu-id="37536-185">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37536-185">0x00000000</span></span>                                                |
| <span data-ttu-id="37536-186">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="37536-186">Classes used in</span></span>        | [<span data-ttu-id="37536-187">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="37536-187">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="37536-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37536-188">Windows Server 2008</span></span>



| <span data-ttu-id="37536-189">Entrada</span><span class="sxs-lookup"><span data-stu-id="37536-189">Entry</span></span> | <span data-ttu-id="37536-190">Valor</span><span class="sxs-lookup"><span data-stu-id="37536-190">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="37536-191">ID do link</span><span class="sxs-lookup"><span data-stu-id="37536-191">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="37536-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37536-192">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="37536-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="37536-193">System-Only</span></span>            | <span data-ttu-id="37536-194">Falso</span><span class="sxs-lookup"><span data-stu-id="37536-194">False</span></span>                                                     |
| <span data-ttu-id="37536-195">É de valor único</span><span class="sxs-lookup"><span data-stu-id="37536-195">Is-Single-Valued</span></span>       | <span data-ttu-id="37536-196">True</span><span class="sxs-lookup"><span data-stu-id="37536-196">True</span></span>                                                      |
| <span data-ttu-id="37536-197">É indexado</span><span class="sxs-lookup"><span data-stu-id="37536-197">Is Indexed</span></span>             | <span data-ttu-id="37536-198">Falso</span><span class="sxs-lookup"><span data-stu-id="37536-198">False</span></span>                                                     |
| <span data-ttu-id="37536-199">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="37536-199">In Global Catalog</span></span>      | <span data-ttu-id="37536-200">Falso</span><span class="sxs-lookup"><span data-stu-id="37536-200">False</span></span>                                                     |
| <span data-ttu-id="37536-201">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="37536-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="37536-202">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="37536-202">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="37536-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37536-203">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="37536-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37536-204">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="37536-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37536-205">Search-Flags</span></span>           | <span data-ttu-id="37536-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37536-206">0x00000000</span></span>                                                |
| <span data-ttu-id="37536-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37536-207">System-Flags</span></span>           | <span data-ttu-id="37536-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37536-208">0x00000000</span></span>                                                |
| <span data-ttu-id="37536-209">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="37536-209">Classes used in</span></span>        | [<span data-ttu-id="37536-210">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="37536-210">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="37536-211">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="37536-211">Windows Server 2008 R2</span></span>



| <span data-ttu-id="37536-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="37536-212">Entry</span></span> | <span data-ttu-id="37536-213">Valor</span><span class="sxs-lookup"><span data-stu-id="37536-213">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="37536-214">ID do link</span><span class="sxs-lookup"><span data-stu-id="37536-214">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="37536-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37536-215">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="37536-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="37536-216">System-Only</span></span>            | <span data-ttu-id="37536-217">Falso</span><span class="sxs-lookup"><span data-stu-id="37536-217">False</span></span>                                                     |
| <span data-ttu-id="37536-218">É de valor único</span><span class="sxs-lookup"><span data-stu-id="37536-218">Is-Single-Valued</span></span>       | <span data-ttu-id="37536-219">True</span><span class="sxs-lookup"><span data-stu-id="37536-219">True</span></span>                                                      |
| <span data-ttu-id="37536-220">É indexado</span><span class="sxs-lookup"><span data-stu-id="37536-220">Is Indexed</span></span>             | <span data-ttu-id="37536-221">Falso</span><span class="sxs-lookup"><span data-stu-id="37536-221">False</span></span>                                                     |
| <span data-ttu-id="37536-222">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="37536-222">In Global Catalog</span></span>      | <span data-ttu-id="37536-223">Falso</span><span class="sxs-lookup"><span data-stu-id="37536-223">False</span></span>                                                     |
| <span data-ttu-id="37536-224">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="37536-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="37536-225">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="37536-225">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="37536-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37536-226">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="37536-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37536-227">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="37536-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37536-228">Search-Flags</span></span>           | <span data-ttu-id="37536-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37536-229">0x00000000</span></span>                                                |
| <span data-ttu-id="37536-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37536-230">System-Flags</span></span>           | <span data-ttu-id="37536-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37536-231">0x00000000</span></span>                                                |
| <span data-ttu-id="37536-232">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="37536-232">Classes used in</span></span>        | [<span data-ttu-id="37536-233">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="37536-233">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="37536-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37536-234">Windows Server 2012</span></span>



| <span data-ttu-id="37536-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="37536-235">Entry</span></span> | <span data-ttu-id="37536-236">Valor</span><span class="sxs-lookup"><span data-stu-id="37536-236">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="37536-237">ID do link</span><span class="sxs-lookup"><span data-stu-id="37536-237">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="37536-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37536-238">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="37536-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="37536-239">System-Only</span></span>            | <span data-ttu-id="37536-240">Falso</span><span class="sxs-lookup"><span data-stu-id="37536-240">False</span></span>                                                     |
| <span data-ttu-id="37536-241">É de valor único</span><span class="sxs-lookup"><span data-stu-id="37536-241">Is-Single-Valued</span></span>       | <span data-ttu-id="37536-242">True</span><span class="sxs-lookup"><span data-stu-id="37536-242">True</span></span>                                                      |
| <span data-ttu-id="37536-243">É indexado</span><span class="sxs-lookup"><span data-stu-id="37536-243">Is Indexed</span></span>             | <span data-ttu-id="37536-244">Falso</span><span class="sxs-lookup"><span data-stu-id="37536-244">False</span></span>                                                     |
| <span data-ttu-id="37536-245">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="37536-245">In Global Catalog</span></span>      | <span data-ttu-id="37536-246">Falso</span><span class="sxs-lookup"><span data-stu-id="37536-246">False</span></span>                                                     |
| <span data-ttu-id="37536-247">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="37536-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="37536-248">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="37536-248">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="37536-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37536-249">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="37536-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37536-250">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="37536-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37536-251">Search-Flags</span></span>           | <span data-ttu-id="37536-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37536-252">0x00000000</span></span>                                                |
| <span data-ttu-id="37536-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37536-253">System-Flags</span></span>           | <span data-ttu-id="37536-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37536-254">0x00000000</span></span>                                                |
| <span data-ttu-id="37536-255">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="37536-255">Classes used in</span></span>        | [<span data-ttu-id="37536-256">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="37536-256">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





