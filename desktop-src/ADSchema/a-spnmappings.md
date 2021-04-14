---
title: SPN-Mappings atributo
description: Esse atributo de valores múltiplos contém uma lista de SPN (nomes de entidade de serviço) para mostrar a equivalência dos tipos SPN.
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- Esquema de SPN-Mappings do atributo AD
- Esquema de AD do atributo sPNMappings
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ccb07e068a22d0a85928832890f0b66ebda016
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104500032"
---
# <a name="spn-mappings-attribute"></a><span data-ttu-id="17d08-105">SPN-Mappings atributo</span><span class="sxs-lookup"><span data-stu-id="17d08-105">SPN-Mappings attribute</span></span>

<span data-ttu-id="17d08-106">Esse atributo de valores múltiplos contém uma lista de SPN (nomes de entidade de serviço) para mostrar a equivalência dos tipos SPN.</span><span class="sxs-lookup"><span data-stu-id="17d08-106">This multiple-valued attribute contains a list of service principal names (SPN) to show the equivalence of SPN types.</span></span> <span data-ttu-id="17d08-107">O SPN é o nome que um cliente usa para identificar exclusivamente uma instância de um serviço.</span><span class="sxs-lookup"><span data-stu-id="17d08-107">The SPN is the name a client uses to uniquely identify an instance of a service.</span></span> <span data-ttu-id="17d08-108">Se você instalar várias instâncias de um serviço em computadores em uma floresta, cada instância deverá ter seu próprio SPN.</span><span class="sxs-lookup"><span data-stu-id="17d08-108">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="17d08-109">Uma determinada instância de serviço pode ter vários SPNs se houver vários nomes que os clientes podem usar para autenticação.</span><span class="sxs-lookup"><span data-stu-id="17d08-109">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span> <span data-ttu-id="17d08-110">Por exemplo, "LDAP/..." Os SPNs podem ser mapeados para que eles sejam equivalentes a "host/..." SPNs.</span><span class="sxs-lookup"><span data-stu-id="17d08-110">For example, "ldap/..." SPNs could be mapped so that they are equivalent to "host/..." SPNs.</span></span>



| <span data-ttu-id="17d08-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="17d08-111">Entry</span></span> | <span data-ttu-id="17d08-112">Valor</span><span class="sxs-lookup"><span data-stu-id="17d08-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17d08-113">CN</span><span class="sxs-lookup"><span data-stu-id="17d08-113">CN</span></span>                | <span data-ttu-id="17d08-114">SPN-Mappings</span><span class="sxs-lookup"><span data-stu-id="17d08-114">SPN-Mappings</span></span>                                                                                                       |
| <span data-ttu-id="17d08-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="17d08-115">Ldap-Display-Name</span></span> | <span data-ttu-id="17d08-116">sPNMappings</span><span class="sxs-lookup"><span data-stu-id="17d08-116">sPNMappings</span></span>                                                                                                        |
| <span data-ttu-id="17d08-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="17d08-117">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="17d08-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="17d08-118">Update Privilege</span></span>  | <span data-ttu-id="17d08-119">Esse valor é definido durante a instalação do produto.</span><span class="sxs-lookup"><span data-stu-id="17d08-119">This value is set during the product installation.</span></span> <span data-ttu-id="17d08-120">Ele pode ser modificado pelo administrador do sistema em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="17d08-120">It can be modified by the system administrator at a later time.</span></span> |
| <span data-ttu-id="17d08-121">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="17d08-121">Update Frequency</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="17d08-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="17d08-122">Attribute-Id</span></span>      | <span data-ttu-id="17d08-123">1.2.840.113556.1.4.1347</span><span class="sxs-lookup"><span data-stu-id="17d08-123">1.2.840.113556.1.4.1347</span></span>                                                                                            |
| <span data-ttu-id="17d08-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="17d08-124">System-Id-Guid</span></span>    | <span data-ttu-id="17d08-125">2ab0e76c-7041-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="17d08-125">2ab0e76c-7041-11d2-9905-0000f87a57d4</span></span>                                                                               |
| <span data-ttu-id="17d08-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="17d08-126">Syntax</span></span>            | [<span data-ttu-id="17d08-127">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="17d08-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                        |



## <a name="implementations"></a><span data-ttu-id="17d08-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="17d08-128">Implementations</span></span>

-   [<span data-ttu-id="17d08-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="17d08-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="17d08-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="17d08-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="17d08-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="17d08-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="17d08-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="17d08-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="17d08-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="17d08-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="17d08-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="17d08-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="17d08-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="17d08-135">Windows 2000 Server</span></span>



| <span data-ttu-id="17d08-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="17d08-136">Entry</span></span> | <span data-ttu-id="17d08-137">Valor</span><span class="sxs-lookup"><span data-stu-id="17d08-137">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="17d08-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="17d08-138">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="17d08-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17d08-139">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="17d08-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="17d08-140">System-Only</span></span>            | <span data-ttu-id="17d08-141">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-141">False</span></span>                                            |
| <span data-ttu-id="17d08-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17d08-142">Is-Single-Valued</span></span>       | <span data-ttu-id="17d08-143">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-143">False</span></span>                                            |
| <span data-ttu-id="17d08-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="17d08-144">Is Indexed</span></span>             | <span data-ttu-id="17d08-145">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-145">False</span></span>                                            |
| <span data-ttu-id="17d08-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17d08-146">In Global Catalog</span></span>      | <span data-ttu-id="17d08-147">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-147">False</span></span>                                            |
| <span data-ttu-id="17d08-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17d08-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="17d08-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17d08-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="17d08-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17d08-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="17d08-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17d08-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="17d08-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17d08-152">Search-Flags</span></span>           | <span data-ttu-id="17d08-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17d08-153">0x00000000</span></span>                                       |
| <span data-ttu-id="17d08-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17d08-154">System-Flags</span></span>           | <span data-ttu-id="17d08-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17d08-155">0x00000010</span></span>                                       |
| <span data-ttu-id="17d08-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17d08-156">Classes used in</span></span>        | [<span data-ttu-id="17d08-157">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="17d08-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="17d08-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="17d08-158">Windows Server 2003</span></span>



| <span data-ttu-id="17d08-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="17d08-159">Entry</span></span> | <span data-ttu-id="17d08-160">Valor</span><span class="sxs-lookup"><span data-stu-id="17d08-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="17d08-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="17d08-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="17d08-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17d08-162">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="17d08-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="17d08-163">System-Only</span></span>            | <span data-ttu-id="17d08-164">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-164">False</span></span>                                            |
| <span data-ttu-id="17d08-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17d08-165">Is-Single-Valued</span></span>       | <span data-ttu-id="17d08-166">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-166">False</span></span>                                            |
| <span data-ttu-id="17d08-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="17d08-167">Is Indexed</span></span>             | <span data-ttu-id="17d08-168">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-168">False</span></span>                                            |
| <span data-ttu-id="17d08-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17d08-169">In Global Catalog</span></span>      | <span data-ttu-id="17d08-170">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-170">False</span></span>                                            |
| <span data-ttu-id="17d08-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17d08-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="17d08-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17d08-172">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="17d08-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17d08-173">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="17d08-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17d08-174">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="17d08-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17d08-175">Search-Flags</span></span>           | <span data-ttu-id="17d08-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17d08-176">0x00000000</span></span>                                       |
| <span data-ttu-id="17d08-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17d08-177">System-Flags</span></span>           | <span data-ttu-id="17d08-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17d08-178">0x00000010</span></span>                                       |
| <span data-ttu-id="17d08-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17d08-179">Classes used in</span></span>        | [<span data-ttu-id="17d08-180">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="17d08-180">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="17d08-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="17d08-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="17d08-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="17d08-182">Entry</span></span> | <span data-ttu-id="17d08-183">Valor</span><span class="sxs-lookup"><span data-stu-id="17d08-183">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="17d08-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="17d08-184">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="17d08-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17d08-185">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="17d08-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="17d08-186">System-Only</span></span>            | <span data-ttu-id="17d08-187">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-187">False</span></span>                                            |
| <span data-ttu-id="17d08-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17d08-188">Is-Single-Valued</span></span>       | <span data-ttu-id="17d08-189">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-189">False</span></span>                                            |
| <span data-ttu-id="17d08-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="17d08-190">Is Indexed</span></span>             | <span data-ttu-id="17d08-191">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-191">False</span></span>                                            |
| <span data-ttu-id="17d08-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17d08-192">In Global Catalog</span></span>      | <span data-ttu-id="17d08-193">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-193">False</span></span>                                            |
| <span data-ttu-id="17d08-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17d08-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="17d08-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17d08-195">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="17d08-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17d08-196">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="17d08-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17d08-197">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="17d08-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17d08-198">Search-Flags</span></span>           | <span data-ttu-id="17d08-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17d08-199">0x00000000</span></span>                                       |
| <span data-ttu-id="17d08-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17d08-200">System-Flags</span></span>           | <span data-ttu-id="17d08-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17d08-201">0x00000010</span></span>                                       |
| <span data-ttu-id="17d08-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17d08-202">Classes used in</span></span>        | [<span data-ttu-id="17d08-203">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="17d08-203">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="17d08-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17d08-204">Windows Server 2008</span></span>



| <span data-ttu-id="17d08-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="17d08-205">Entry</span></span> | <span data-ttu-id="17d08-206">Valor</span><span class="sxs-lookup"><span data-stu-id="17d08-206">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="17d08-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="17d08-207">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="17d08-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17d08-208">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="17d08-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="17d08-209">System-Only</span></span>            | <span data-ttu-id="17d08-210">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-210">False</span></span>                                            |
| <span data-ttu-id="17d08-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17d08-211">Is-Single-Valued</span></span>       | <span data-ttu-id="17d08-212">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-212">False</span></span>                                            |
| <span data-ttu-id="17d08-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="17d08-213">Is Indexed</span></span>             | <span data-ttu-id="17d08-214">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-214">False</span></span>                                            |
| <span data-ttu-id="17d08-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17d08-215">In Global Catalog</span></span>      | <span data-ttu-id="17d08-216">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-216">False</span></span>                                            |
| <span data-ttu-id="17d08-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17d08-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="17d08-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17d08-218">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="17d08-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17d08-219">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="17d08-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17d08-220">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="17d08-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17d08-221">Search-Flags</span></span>           | <span data-ttu-id="17d08-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17d08-222">0x00000000</span></span>                                       |
| <span data-ttu-id="17d08-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17d08-223">System-Flags</span></span>           | <span data-ttu-id="17d08-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17d08-224">0x00000010</span></span>                                       |
| <span data-ttu-id="17d08-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17d08-225">Classes used in</span></span>        | [<span data-ttu-id="17d08-226">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="17d08-226">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="17d08-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="17d08-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="17d08-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="17d08-228">Entry</span></span> | <span data-ttu-id="17d08-229">Valor</span><span class="sxs-lookup"><span data-stu-id="17d08-229">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="17d08-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="17d08-230">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="17d08-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17d08-231">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="17d08-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="17d08-232">System-Only</span></span>            | <span data-ttu-id="17d08-233">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-233">False</span></span>                                            |
| <span data-ttu-id="17d08-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17d08-234">Is-Single-Valued</span></span>       | <span data-ttu-id="17d08-235">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-235">False</span></span>                                            |
| <span data-ttu-id="17d08-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="17d08-236">Is Indexed</span></span>             | <span data-ttu-id="17d08-237">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-237">False</span></span>                                            |
| <span data-ttu-id="17d08-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17d08-238">In Global Catalog</span></span>      | <span data-ttu-id="17d08-239">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-239">False</span></span>                                            |
| <span data-ttu-id="17d08-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17d08-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="17d08-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17d08-241">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="17d08-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17d08-242">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="17d08-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17d08-243">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="17d08-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17d08-244">Search-Flags</span></span>           | <span data-ttu-id="17d08-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17d08-245">0x00000000</span></span>                                       |
| <span data-ttu-id="17d08-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17d08-246">System-Flags</span></span>           | <span data-ttu-id="17d08-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17d08-247">0x00000010</span></span>                                       |
| <span data-ttu-id="17d08-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17d08-248">Classes used in</span></span>        | [<span data-ttu-id="17d08-249">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="17d08-249">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="17d08-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17d08-250">Windows Server 2012</span></span>



| <span data-ttu-id="17d08-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="17d08-251">Entry</span></span> | <span data-ttu-id="17d08-252">Valor</span><span class="sxs-lookup"><span data-stu-id="17d08-252">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="17d08-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="17d08-253">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="17d08-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17d08-254">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="17d08-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="17d08-255">System-Only</span></span>            | <span data-ttu-id="17d08-256">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-256">False</span></span>                                            |
| <span data-ttu-id="17d08-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17d08-257">Is-Single-Valued</span></span>       | <span data-ttu-id="17d08-258">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-258">False</span></span>                                            |
| <span data-ttu-id="17d08-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="17d08-259">Is Indexed</span></span>             | <span data-ttu-id="17d08-260">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-260">False</span></span>                                            |
| <span data-ttu-id="17d08-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17d08-261">In Global Catalog</span></span>      | <span data-ttu-id="17d08-262">Falso</span><span class="sxs-lookup"><span data-stu-id="17d08-262">False</span></span>                                            |
| <span data-ttu-id="17d08-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17d08-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="17d08-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17d08-264">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="17d08-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17d08-265">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="17d08-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17d08-266">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="17d08-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17d08-267">Search-Flags</span></span>           | <span data-ttu-id="17d08-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17d08-268">0x00000000</span></span>                                       |
| <span data-ttu-id="17d08-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17d08-269">System-Flags</span></span>           | <span data-ttu-id="17d08-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17d08-270">0x00000010</span></span>                                       |
| <span data-ttu-id="17d08-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17d08-271">Classes used in</span></span>        | [<span data-ttu-id="17d08-272">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="17d08-272">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





