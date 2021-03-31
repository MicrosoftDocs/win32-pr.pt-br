---
title: Atributo Certificate-Revocation-List
description: Representa uma lista de certificados que foram revogados.
ms.assetid: fb7b4888-15c0-475b-a87a-7cb0656963bb
ms.tgt_platform: multiple
keywords:
- Atributo do AD de atributos de lista de certificados revogados
- Esquema de AD do atributo certificateRevocationList
topic_type:
- apiref
api_name:
- Certificate-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae77265ffeeae76ae07d608845723b1828772f0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086751"
---
# <a name="certificate-revocation-list-attribute"></a><span data-ttu-id="bcb03-105">Atributo Certificate-Revocation-List</span><span class="sxs-lookup"><span data-stu-id="bcb03-105">Certificate-Revocation-List attribute</span></span>

<span data-ttu-id="bcb03-106">Representa uma lista de certificados que foram revogados.</span><span class="sxs-lookup"><span data-stu-id="bcb03-106">Represents a list of certificates that have been revoked.</span></span>



| <span data-ttu-id="bcb03-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="bcb03-107">Entry</span></span> | <span data-ttu-id="bcb03-108">Valor</span><span class="sxs-lookup"><span data-stu-id="bcb03-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="bcb03-109">CN</span><span class="sxs-lookup"><span data-stu-id="bcb03-109">CN</span></span>                | <span data-ttu-id="bcb03-110">Certificado-lista de certificados revogados</span><span class="sxs-lookup"><span data-stu-id="bcb03-110">Certificate-Revocation-List</span></span>                           |
| <span data-ttu-id="bcb03-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bcb03-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bcb03-112">certificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="bcb03-112">certificateRevocationList</span></span>                             |
| <span data-ttu-id="bcb03-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="bcb03-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="bcb03-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="bcb03-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="bcb03-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="bcb03-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="bcb03-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bcb03-116">Attribute-Id</span></span>      | <span data-ttu-id="bcb03-117">2.5.4.39</span><span class="sxs-lookup"><span data-stu-id="bcb03-117">2.5.4.39</span></span>                                              |
| <span data-ttu-id="bcb03-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bcb03-118">System-Id-Guid</span></span>    | <span data-ttu-id="bcb03-119">1677579f-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="bcb03-119">1677579f-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="bcb03-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcb03-120">Syntax</span></span>            | [<span data-ttu-id="bcb03-121">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="bcb03-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="bcb03-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="bcb03-122">Implementations</span></span>

-   [<span data-ttu-id="bcb03-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bcb03-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bcb03-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bcb03-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bcb03-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bcb03-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bcb03-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bcb03-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bcb03-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bcb03-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bcb03-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bcb03-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bcb03-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bcb03-129">Windows 2000 Server</span></span>



| <span data-ttu-id="bcb03-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="bcb03-130">Entry</span></span> | <span data-ttu-id="bcb03-131">Valor</span><span class="sxs-lookup"><span data-stu-id="bcb03-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb03-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="bcb03-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bcb03-133">MAPI-Id</span></span>                | <span data-ttu-id="bcb03-134">0x8016</span><span class="sxs-lookup"><span data-stu-id="bcb03-134">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="bcb03-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="bcb03-135">System-Only</span></span>            | <span data-ttu-id="bcb03-136">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-136">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bcb03-137">Is-Single-Valued</span></span>       | <span data-ttu-id="bcb03-138">True</span><span class="sxs-lookup"><span data-stu-id="bcb03-138">True</span></span>                                                                                                                                       |
| <span data-ttu-id="bcb03-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="bcb03-139">Is Indexed</span></span>             | <span data-ttu-id="bcb03-140">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-140">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bcb03-141">In Global Catalog</span></span>      | <span data-ttu-id="bcb03-142">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-142">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bcb03-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="bcb03-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bcb03-144">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="bcb03-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bcb03-145">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bcb03-146">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bcb03-147">Search-Flags</span></span>           | <span data-ttu-id="bcb03-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bcb03-148">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="bcb03-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bcb03-149">System-Flags</span></span>           | <span data-ttu-id="bcb03-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bcb03-150">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="bcb03-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bcb03-151">Classes used in</span></span>        | [<span data-ttu-id="bcb03-152">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="bcb03-152">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="bcb03-153">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="bcb03-153">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bcb03-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bcb03-154">Windows Server 2003</span></span>



| <span data-ttu-id="bcb03-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="bcb03-155">Entry</span></span> | <span data-ttu-id="bcb03-156">Valor</span><span class="sxs-lookup"><span data-stu-id="bcb03-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb03-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="bcb03-157">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bcb03-158">MAPI-Id</span></span>                | <span data-ttu-id="bcb03-159">0x8016</span><span class="sxs-lookup"><span data-stu-id="bcb03-159">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="bcb03-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="bcb03-160">System-Only</span></span>            | <span data-ttu-id="bcb03-161">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bcb03-162">Is-Single-Valued</span></span>       | <span data-ttu-id="bcb03-163">True</span><span class="sxs-lookup"><span data-stu-id="bcb03-163">True</span></span>                                                                                                                                       |
| <span data-ttu-id="bcb03-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="bcb03-164">Is Indexed</span></span>             | <span data-ttu-id="bcb03-165">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bcb03-166">In Global Catalog</span></span>      | <span data-ttu-id="bcb03-167">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-167">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bcb03-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="bcb03-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bcb03-169">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="bcb03-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bcb03-170">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bcb03-171">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bcb03-172">Search-Flags</span></span>           | <span data-ttu-id="bcb03-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bcb03-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="bcb03-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bcb03-174">System-Flags</span></span>           | <span data-ttu-id="bcb03-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bcb03-175">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="bcb03-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bcb03-176">Classes used in</span></span>        | [<span data-ttu-id="bcb03-177">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="bcb03-177">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="bcb03-178">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="bcb03-178">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bcb03-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bcb03-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bcb03-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="bcb03-180">Entry</span></span> | <span data-ttu-id="bcb03-181">Valor</span><span class="sxs-lookup"><span data-stu-id="bcb03-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb03-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="bcb03-182">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bcb03-183">MAPI-Id</span></span>                | <span data-ttu-id="bcb03-184">0x8016</span><span class="sxs-lookup"><span data-stu-id="bcb03-184">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="bcb03-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="bcb03-185">System-Only</span></span>            | <span data-ttu-id="bcb03-186">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bcb03-187">Is-Single-Valued</span></span>       | <span data-ttu-id="bcb03-188">True</span><span class="sxs-lookup"><span data-stu-id="bcb03-188">True</span></span>                                                                                                                                       |
| <span data-ttu-id="bcb03-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="bcb03-189">Is Indexed</span></span>             | <span data-ttu-id="bcb03-190">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bcb03-191">In Global Catalog</span></span>      | <span data-ttu-id="bcb03-192">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-192">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bcb03-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="bcb03-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bcb03-194">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="bcb03-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bcb03-195">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bcb03-196">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bcb03-197">Search-Flags</span></span>           | <span data-ttu-id="bcb03-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bcb03-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="bcb03-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bcb03-199">System-Flags</span></span>           | <span data-ttu-id="bcb03-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bcb03-200">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="bcb03-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bcb03-201">Classes used in</span></span>        | [<span data-ttu-id="bcb03-202">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="bcb03-202">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="bcb03-203">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="bcb03-203">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bcb03-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcb03-204">Windows Server 2008</span></span>



| <span data-ttu-id="bcb03-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="bcb03-205">Entry</span></span> | <span data-ttu-id="bcb03-206">Valor</span><span class="sxs-lookup"><span data-stu-id="bcb03-206">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb03-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="bcb03-207">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bcb03-208">MAPI-Id</span></span>                | <span data-ttu-id="bcb03-209">0x8016</span><span class="sxs-lookup"><span data-stu-id="bcb03-209">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="bcb03-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="bcb03-210">System-Only</span></span>            | <span data-ttu-id="bcb03-211">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bcb03-212">Is-Single-Valued</span></span>       | <span data-ttu-id="bcb03-213">True</span><span class="sxs-lookup"><span data-stu-id="bcb03-213">True</span></span>                                                                                                                                       |
| <span data-ttu-id="bcb03-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="bcb03-214">Is Indexed</span></span>             | <span data-ttu-id="bcb03-215">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bcb03-216">In Global Catalog</span></span>      | <span data-ttu-id="bcb03-217">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-217">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bcb03-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="bcb03-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bcb03-219">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="bcb03-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bcb03-220">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bcb03-221">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bcb03-222">Search-Flags</span></span>           | <span data-ttu-id="bcb03-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bcb03-223">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="bcb03-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bcb03-224">System-Flags</span></span>           | <span data-ttu-id="bcb03-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bcb03-225">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="bcb03-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bcb03-226">Classes used in</span></span>        | [<span data-ttu-id="bcb03-227">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="bcb03-227">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="bcb03-228">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="bcb03-228">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bcb03-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bcb03-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bcb03-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="bcb03-230">Entry</span></span> | <span data-ttu-id="bcb03-231">Valor</span><span class="sxs-lookup"><span data-stu-id="bcb03-231">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb03-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="bcb03-232">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bcb03-233">MAPI-Id</span></span>                | <span data-ttu-id="bcb03-234">0x8016</span><span class="sxs-lookup"><span data-stu-id="bcb03-234">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="bcb03-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="bcb03-235">System-Only</span></span>            | <span data-ttu-id="bcb03-236">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-236">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bcb03-237">Is-Single-Valued</span></span>       | <span data-ttu-id="bcb03-238">True</span><span class="sxs-lookup"><span data-stu-id="bcb03-238">True</span></span>                                                                                                                                       |
| <span data-ttu-id="bcb03-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="bcb03-239">Is Indexed</span></span>             | <span data-ttu-id="bcb03-240">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bcb03-241">In Global Catalog</span></span>      | <span data-ttu-id="bcb03-242">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-242">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bcb03-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="bcb03-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bcb03-244">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="bcb03-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bcb03-245">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bcb03-246">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bcb03-247">Search-Flags</span></span>           | <span data-ttu-id="bcb03-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bcb03-248">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="bcb03-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bcb03-249">System-Flags</span></span>           | <span data-ttu-id="bcb03-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bcb03-250">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="bcb03-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bcb03-251">Classes used in</span></span>        | [<span data-ttu-id="bcb03-252">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="bcb03-252">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="bcb03-253">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="bcb03-253">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bcb03-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bcb03-254">Windows Server 2012</span></span>



| <span data-ttu-id="bcb03-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="bcb03-255">Entry</span></span> | <span data-ttu-id="bcb03-256">Valor</span><span class="sxs-lookup"><span data-stu-id="bcb03-256">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb03-257">ID do link</span><span class="sxs-lookup"><span data-stu-id="bcb03-257">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bcb03-258">MAPI-Id</span></span>                | <span data-ttu-id="bcb03-259">0x8016</span><span class="sxs-lookup"><span data-stu-id="bcb03-259">0x8016</span></span>                                                                                                                                     |
| <span data-ttu-id="bcb03-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="bcb03-260">System-Only</span></span>            | <span data-ttu-id="bcb03-261">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-261">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-262">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bcb03-262">Is-Single-Valued</span></span>       | <span data-ttu-id="bcb03-263">True</span><span class="sxs-lookup"><span data-stu-id="bcb03-263">True</span></span>                                                                                                                                       |
| <span data-ttu-id="bcb03-264">É indexado</span><span class="sxs-lookup"><span data-stu-id="bcb03-264">Is Indexed</span></span>             | <span data-ttu-id="bcb03-265">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-265">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-266">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bcb03-266">In Global Catalog</span></span>      | <span data-ttu-id="bcb03-267">Falso</span><span class="sxs-lookup"><span data-stu-id="bcb03-267">False</span></span>                                                                                                                                      |
| <span data-ttu-id="bcb03-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bcb03-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="bcb03-269">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bcb03-269">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="bcb03-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bcb03-270">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bcb03-271">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="bcb03-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bcb03-272">Search-Flags</span></span>           | <span data-ttu-id="bcb03-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bcb03-273">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="bcb03-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bcb03-274">System-Flags</span></span>           | <span data-ttu-id="bcb03-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bcb03-275">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="bcb03-276">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bcb03-276">Classes used in</span></span>        | [<span data-ttu-id="bcb03-277">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="bcb03-277">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="bcb03-278">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="bcb03-278">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 





