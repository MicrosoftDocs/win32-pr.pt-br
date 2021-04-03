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
# <a name="ms-frs-topology-pref-attribute"></a><span data-ttu-id="52a6a-105">atributo ms-FRS-Topology-pref</span><span class="sxs-lookup"><span data-stu-id="52a6a-105">ms-FRS-Topology-Pref attribute</span></span>

<span data-ttu-id="52a6a-106">O atributo **MS-FRS-Topology-pref** é usado para registrar as configurações de topologia de NTFRS preferenciais.</span><span class="sxs-lookup"><span data-stu-id="52a6a-106">The **ms-FRS-Topology-Pref** attribute is used to record the preferred NTFRS topology settings.</span></span> <span data-ttu-id="52a6a-107">Quando um membro do FRS é adicionado ou excluído ao conjunto de réplicas, esses atributos são referenciados e os ajustes feitos nas conexões entre o restante dos membros do FRS no conjunto de réplicas.</span><span class="sxs-lookup"><span data-stu-id="52a6a-107">When an FRS member gets added or deleted to the replica set, these attributes are referred, and adjustments made to the connections between the rest of the FRS members in the replica set.</span></span>

<span data-ttu-id="52a6a-108">Os valores válidos para esse atributo são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="52a6a-108">Valid values for this attribute are as follows.</span></span>

| <span data-ttu-id="52a6a-109">Valor</span><span class="sxs-lookup"><span data-stu-id="52a6a-109">Value</span></span> | <span data-ttu-id="52a6a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="52a6a-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="52a6a-111">1</span><span class="sxs-lookup"><span data-stu-id="52a6a-111">1</span></span>     | <span data-ttu-id="52a6a-112">\_anel RSTOPOLOGYPREF do FRS \_</span><span class="sxs-lookup"><span data-stu-id="52a6a-112">FRS\_RSTOPOLOGYPREF\_RING</span></span><br/>     |
| <span data-ttu-id="52a6a-113">2</span><span class="sxs-lookup"><span data-stu-id="52a6a-113">2</span></span>     | <span data-ttu-id="52a6a-114">\_HUBSPOKE RSTOPOLOGYPREF do FRS \_</span><span class="sxs-lookup"><span data-stu-id="52a6a-114">FRS\_RSTOPOLOGYPREF\_HUBSPOKE</span></span><br/> |
| <span data-ttu-id="52a6a-115">3</span><span class="sxs-lookup"><span data-stu-id="52a6a-115">3</span></span>     | <span data-ttu-id="52a6a-116">\_FULLMESH RSTOPOLOGYPREF do FRS \_</span><span class="sxs-lookup"><span data-stu-id="52a6a-116">FRS\_RSTOPOLOGYPREF\_FULLMESH</span></span><br/> |
| <span data-ttu-id="52a6a-117">4</span><span class="sxs-lookup"><span data-stu-id="52a6a-117">4</span></span>     | <span data-ttu-id="52a6a-118">RSTOPOLOGYPREF de FRS \_ \_ personalizado</span><span class="sxs-lookup"><span data-stu-id="52a6a-118">FRS\_RSTOPOLOGYPREF\_CUSTOM</span></span><br/>   |



 



| <span data-ttu-id="52a6a-119">Entrada</span><span class="sxs-lookup"><span data-stu-id="52a6a-119">Entry</span></span> | <span data-ttu-id="52a6a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="52a6a-120">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="52a6a-121">CN</span><span class="sxs-lookup"><span data-stu-id="52a6a-121">CN</span></span>                | <span data-ttu-id="52a6a-122">MS-FRS-Topology-pref</span><span class="sxs-lookup"><span data-stu-id="52a6a-122">ms-FRS-Topology-Pref</span></span>                                               |
| <span data-ttu-id="52a6a-123">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="52a6a-123">Ldap-Display-Name</span></span> | <span data-ttu-id="52a6a-124">msFRS-Topology-pref</span><span class="sxs-lookup"><span data-stu-id="52a6a-124">msFRS-Topology-Pref</span></span>                                                |
| <span data-ttu-id="52a6a-125">Tamanho</span><span class="sxs-lookup"><span data-stu-id="52a6a-125">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="52a6a-126">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="52a6a-126">Update Privilege</span></span>  | <span data-ttu-id="52a6a-127">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="52a6a-127">Domain administrator</span></span>                                               |
| <span data-ttu-id="52a6a-128">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="52a6a-128">Update Frequency</span></span>  | <span data-ttu-id="52a6a-129">Quando o conjunto de réplicas é criado ou a topologia preferida é alterada.</span><span class="sxs-lookup"><span data-stu-id="52a6a-129">When the replica set is created or the preferred topology changes.</span></span> |
| <span data-ttu-id="52a6a-130">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="52a6a-130">Attribute-Id</span></span>      | <span data-ttu-id="52a6a-131">1.2.840.113556.1.4.1692</span><span class="sxs-lookup"><span data-stu-id="52a6a-131">1.2.840.113556.1.4.1692</span></span>                                            |
| <span data-ttu-id="52a6a-132">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="52a6a-132">System-Id-Guid</span></span>    | <span data-ttu-id="52a6a-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span><span class="sxs-lookup"><span data-stu-id="52a6a-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span></span>                               |
| <span data-ttu-id="52a6a-134">Syntax</span><span class="sxs-lookup"><span data-stu-id="52a6a-134">Syntax</span></span>            | [<span data-ttu-id="52a6a-135">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="52a6a-135">**String(Unicode)**</span></span>](s-string-unicode.md)                        |



## <a name="implementations"></a><span data-ttu-id="52a6a-136">Implementações</span><span class="sxs-lookup"><span data-stu-id="52a6a-136">Implementations</span></span>

-   [<span data-ttu-id="52a6a-137">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="52a6a-137">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="52a6a-138">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="52a6a-138">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="52a6a-139">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="52a6a-139">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="52a6a-140">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="52a6a-140">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="52a6a-141">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="52a6a-141">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="52a6a-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="52a6a-142">Windows Server 2003</span></span>



| <span data-ttu-id="52a6a-143">Entrada</span><span class="sxs-lookup"><span data-stu-id="52a6a-143">Entry</span></span> | <span data-ttu-id="52a6a-144">Valor</span><span class="sxs-lookup"><span data-stu-id="52a6a-144">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="52a6a-145">ID do link</span><span class="sxs-lookup"><span data-stu-id="52a6a-145">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="52a6a-146">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52a6a-146">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="52a6a-147">System-Only</span><span class="sxs-lookup"><span data-stu-id="52a6a-147">System-Only</span></span>            | <span data-ttu-id="52a6a-148">Falso</span><span class="sxs-lookup"><span data-stu-id="52a6a-148">False</span></span>                                                     |
| <span data-ttu-id="52a6a-149">É de valor único</span><span class="sxs-lookup"><span data-stu-id="52a6a-149">Is-Single-Valued</span></span>       | <span data-ttu-id="52a6a-150">True</span><span class="sxs-lookup"><span data-stu-id="52a6a-150">True</span></span>                                                      |
| <span data-ttu-id="52a6a-151">É indexado</span><span class="sxs-lookup"><span data-stu-id="52a6a-151">Is Indexed</span></span>             | <span data-ttu-id="52a6a-152">Falso</span><span class="sxs-lookup"><span data-stu-id="52a6a-152">False</span></span>                                                     |
| <span data-ttu-id="52a6a-153">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="52a6a-153">In Global Catalog</span></span>      | <span data-ttu-id="52a6a-154">Falso</span><span class="sxs-lookup"><span data-stu-id="52a6a-154">False</span></span>                                                     |
| <span data-ttu-id="52a6a-155">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="52a6a-155">NT-Security-Descriptor</span></span> | <span data-ttu-id="52a6a-156">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="52a6a-156">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="52a6a-157">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52a6a-157">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="52a6a-158">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52a6a-158">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="52a6a-159">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52a6a-159">Search-Flags</span></span>           | <span data-ttu-id="52a6a-160">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52a6a-160">0x00000000</span></span>                                                |
| <span data-ttu-id="52a6a-161">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52a6a-161">System-Flags</span></span>           | <span data-ttu-id="52a6a-162">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52a6a-162">0x00000000</span></span>                                                |
| <span data-ttu-id="52a6a-163">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="52a6a-163">Classes used in</span></span>        | [<span data-ttu-id="52a6a-164">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="52a6a-164">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="52a6a-165">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="52a6a-165">Windows Server 2003 R2</span></span>



| <span data-ttu-id="52a6a-166">Entrada</span><span class="sxs-lookup"><span data-stu-id="52a6a-166">Entry</span></span> | <span data-ttu-id="52a6a-167">Valor</span><span class="sxs-lookup"><span data-stu-id="52a6a-167">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="52a6a-168">ID do link</span><span class="sxs-lookup"><span data-stu-id="52a6a-168">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="52a6a-169">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52a6a-169">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="52a6a-170">System-Only</span><span class="sxs-lookup"><span data-stu-id="52a6a-170">System-Only</span></span>            | <span data-ttu-id="52a6a-171">Falso</span><span class="sxs-lookup"><span data-stu-id="52a6a-171">False</span></span>                                                     |
| <span data-ttu-id="52a6a-172">É de valor único</span><span class="sxs-lookup"><span data-stu-id="52a6a-172">Is-Single-Valued</span></span>       | <span data-ttu-id="52a6a-173">True</span><span class="sxs-lookup"><span data-stu-id="52a6a-173">True</span></span>                                                      |
| <span data-ttu-id="52a6a-174">É indexado</span><span class="sxs-lookup"><span data-stu-id="52a6a-174">Is Indexed</span></span>             | <span data-ttu-id="52a6a-175">Falso</span><span class="sxs-lookup"><span data-stu-id="52a6a-175">False</span></span>                                                     |
| <span data-ttu-id="52a6a-176">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="52a6a-176">In Global Catalog</span></span>      | <span data-ttu-id="52a6a-177">Falso</span><span class="sxs-lookup"><span data-stu-id="52a6a-177">False</span></span>                                                     |
| <span data-ttu-id="52a6a-178">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="52a6a-178">NT-Security-Descriptor</span></span> | <span data-ttu-id="52a6a-179">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="52a6a-179">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="52a6a-180">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52a6a-180">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="52a6a-181">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52a6a-181">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="52a6a-182">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52a6a-182">Search-Flags</span></span>           | <span data-ttu-id="52a6a-183">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52a6a-183">0x00000000</span></span>                                                |
| <span data-ttu-id="52a6a-184">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52a6a-184">System-Flags</span></span>           | <span data-ttu-id="52a6a-185">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52a6a-185">0x00000000</span></span>                                                |
| <span data-ttu-id="52a6a-186">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="52a6a-186">Classes used in</span></span>        | [<span data-ttu-id="52a6a-187">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="52a6a-187">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="52a6a-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52a6a-188">Windows Server 2008</span></span>



| <span data-ttu-id="52a6a-189">Entrada</span><span class="sxs-lookup"><span data-stu-id="52a6a-189">Entry</span></span> | <span data-ttu-id="52a6a-190">Valor</span><span class="sxs-lookup"><span data-stu-id="52a6a-190">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="52a6a-191">ID do link</span><span class="sxs-lookup"><span data-stu-id="52a6a-191">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="52a6a-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52a6a-192">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="52a6a-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="52a6a-193">System-Only</span></span>            | <span data-ttu-id="52a6a-194">Falso</span><span class="sxs-lookup"><span data-stu-id="52a6a-194">False</span></span>                                                     |
| <span data-ttu-id="52a6a-195">É de valor único</span><span class="sxs-lookup"><span data-stu-id="52a6a-195">Is-Single-Valued</span></span>       | <span data-ttu-id="52a6a-196">True</span><span class="sxs-lookup"><span data-stu-id="52a6a-196">True</span></span>                                                      |
| <span data-ttu-id="52a6a-197">É indexado</span><span class="sxs-lookup"><span data-stu-id="52a6a-197">Is Indexed</span></span>             | <span data-ttu-id="52a6a-198">Falso</span><span class="sxs-lookup"><span data-stu-id="52a6a-198">False</span></span>                                                     |
| <span data-ttu-id="52a6a-199">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="52a6a-199">In Global Catalog</span></span>      | <span data-ttu-id="52a6a-200">Falso</span><span class="sxs-lookup"><span data-stu-id="52a6a-200">False</span></span>                                                     |
| <span data-ttu-id="52a6a-201">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="52a6a-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="52a6a-202">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="52a6a-202">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="52a6a-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52a6a-203">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="52a6a-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52a6a-204">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="52a6a-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52a6a-205">Search-Flags</span></span>           | <span data-ttu-id="52a6a-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52a6a-206">0x00000000</span></span>                                                |
| <span data-ttu-id="52a6a-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52a6a-207">System-Flags</span></span>           | <span data-ttu-id="52a6a-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52a6a-208">0x00000000</span></span>                                                |
| <span data-ttu-id="52a6a-209">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="52a6a-209">Classes used in</span></span>        | [<span data-ttu-id="52a6a-210">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="52a6a-210">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="52a6a-211">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="52a6a-211">Windows Server 2008 R2</span></span>



| <span data-ttu-id="52a6a-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="52a6a-212">Entry</span></span> | <span data-ttu-id="52a6a-213">Valor</span><span class="sxs-lookup"><span data-stu-id="52a6a-213">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="52a6a-214">ID do link</span><span class="sxs-lookup"><span data-stu-id="52a6a-214">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="52a6a-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52a6a-215">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="52a6a-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="52a6a-216">System-Only</span></span>            | <span data-ttu-id="52a6a-217">Falso</span><span class="sxs-lookup"><span data-stu-id="52a6a-217">False</span></span>                                                     |
| <span data-ttu-id="52a6a-218">É de valor único</span><span class="sxs-lookup"><span data-stu-id="52a6a-218">Is-Single-Valued</span></span>       | <span data-ttu-id="52a6a-219">True</span><span class="sxs-lookup"><span data-stu-id="52a6a-219">True</span></span>                                                      |
| <span data-ttu-id="52a6a-220">É indexado</span><span class="sxs-lookup"><span data-stu-id="52a6a-220">Is Indexed</span></span>             | <span data-ttu-id="52a6a-221">Falso</span><span class="sxs-lookup"><span data-stu-id="52a6a-221">False</span></span>                                                     |
| <span data-ttu-id="52a6a-222">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="52a6a-222">In Global Catalog</span></span>      | <span data-ttu-id="52a6a-223">Falso</span><span class="sxs-lookup"><span data-stu-id="52a6a-223">False</span></span>                                                     |
| <span data-ttu-id="52a6a-224">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="52a6a-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="52a6a-225">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="52a6a-225">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="52a6a-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52a6a-226">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="52a6a-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52a6a-227">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="52a6a-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52a6a-228">Search-Flags</span></span>           | <span data-ttu-id="52a6a-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52a6a-229">0x00000000</span></span>                                                |
| <span data-ttu-id="52a6a-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52a6a-230">System-Flags</span></span>           | <span data-ttu-id="52a6a-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52a6a-231">0x00000000</span></span>                                                |
| <span data-ttu-id="52a6a-232">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="52a6a-232">Classes used in</span></span>        | [<span data-ttu-id="52a6a-233">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="52a6a-233">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="52a6a-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="52a6a-234">Windows Server 2012</span></span>



| <span data-ttu-id="52a6a-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="52a6a-235">Entry</span></span> | <span data-ttu-id="52a6a-236">Valor</span><span class="sxs-lookup"><span data-stu-id="52a6a-236">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="52a6a-237">ID do link</span><span class="sxs-lookup"><span data-stu-id="52a6a-237">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="52a6a-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52a6a-238">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="52a6a-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="52a6a-239">System-Only</span></span>            | <span data-ttu-id="52a6a-240">Falso</span><span class="sxs-lookup"><span data-stu-id="52a6a-240">False</span></span>                                                     |
| <span data-ttu-id="52a6a-241">É de valor único</span><span class="sxs-lookup"><span data-stu-id="52a6a-241">Is-Single-Valued</span></span>       | <span data-ttu-id="52a6a-242">True</span><span class="sxs-lookup"><span data-stu-id="52a6a-242">True</span></span>                                                      |
| <span data-ttu-id="52a6a-243">É indexado</span><span class="sxs-lookup"><span data-stu-id="52a6a-243">Is Indexed</span></span>             | <span data-ttu-id="52a6a-244">Falso</span><span class="sxs-lookup"><span data-stu-id="52a6a-244">False</span></span>                                                     |
| <span data-ttu-id="52a6a-245">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="52a6a-245">In Global Catalog</span></span>      | <span data-ttu-id="52a6a-246">Falso</span><span class="sxs-lookup"><span data-stu-id="52a6a-246">False</span></span>                                                     |
| <span data-ttu-id="52a6a-247">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="52a6a-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="52a6a-248">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="52a6a-248">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="52a6a-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52a6a-249">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="52a6a-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52a6a-250">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="52a6a-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52a6a-251">Search-Flags</span></span>           | <span data-ttu-id="52a6a-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52a6a-252">0x00000000</span></span>                                                |
| <span data-ttu-id="52a6a-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52a6a-253">System-Flags</span></span>           | <span data-ttu-id="52a6a-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52a6a-254">0x00000000</span></span>                                                |
| <span data-ttu-id="52a6a-255">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="52a6a-255">Classes used in</span></span>        | [<span data-ttu-id="52a6a-256">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="52a6a-256">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





