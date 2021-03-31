---
title: Atributo min-pwd-age
description: A quantidade mínima de tempo, em intervalos de 100 a nanossegundos, que uma senha é válida.
ms.assetid: c1ddd8a3-8481-4b6e-95ac-1cdc81a4cf78
ms.tgt_platform: multiple
keywords:
- Esquema de anúncio de atributo min-pwd-age
- Esquema de AD do atributo minPwdAge
topic_type:
- apiref
api_name:
- Min-Pwd-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c733f1a6f6803b10f04d6b0f9e367a9933cd9330
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086731"
---
# <a name="min-pwd-age-attribute"></a><span data-ttu-id="ecfb6-105">Atributo min-pwd-age</span><span class="sxs-lookup"><span data-stu-id="ecfb6-105">Min-Pwd-Age attribute</span></span>

<span data-ttu-id="ecfb6-106">A quantidade mínima de tempo, em intervalos de 100 a nanossegundos, que uma senha é válida.</span><span class="sxs-lookup"><span data-stu-id="ecfb6-106">The minimum amount of time, in 100-nanosecond intervals, that a password is valid.</span></span>



| <span data-ttu-id="ecfb6-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ecfb6-107">Entry</span></span> | <span data-ttu-id="ecfb6-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ecfb6-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ecfb6-109">CN</span><span class="sxs-lookup"><span data-stu-id="ecfb6-109">CN</span></span>                | <span data-ttu-id="ecfb6-110">Mín-pwd-idade</span><span class="sxs-lookup"><span data-stu-id="ecfb6-110">Min-Pwd-Age</span></span>                          |
| <span data-ttu-id="ecfb6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ecfb6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ecfb6-112">minPwdAge</span><span class="sxs-lookup"><span data-stu-id="ecfb6-112">minPwdAge</span></span>                            |
| <span data-ttu-id="ecfb6-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ecfb6-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="ecfb6-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="ecfb6-114">Update Privilege</span></span>  | <span data-ttu-id="ecfb6-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="ecfb6-115">Domain administrator</span></span>                 |
| <span data-ttu-id="ecfb6-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="ecfb6-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ecfb6-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ecfb6-117">Attribute-Id</span></span>      | <span data-ttu-id="ecfb6-118">1.2.840.113556.1.4.78</span><span class="sxs-lookup"><span data-stu-id="ecfb6-118">1.2.840.113556.1.4.78</span></span>                |
| <span data-ttu-id="ecfb6-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ecfb6-119">System-Id-Guid</span></span>    | <span data-ttu-id="ecfb6-120">bf9679c2-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ecfb6-120">bf9679c2-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ecfb6-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecfb6-121">Syntax</span></span>            | [<span data-ttu-id="ecfb6-122">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="ecfb6-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="ecfb6-123">Implementations</span></span>

-   [<span data-ttu-id="ecfb6-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ecfb6-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ecfb6-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ecfb6-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ecfb6-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ecfb6-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ecfb6-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ecfb6-130">Windows 2000 Server</span></span>



| <span data-ttu-id="ecfb6-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="ecfb6-131">Entry</span></span> | <span data-ttu-id="ecfb6-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ecfb6-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecfb6-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="ecfb6-133">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecfb6-134">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecfb6-135">System-Only</span></span>            | <span data-ttu-id="ecfb6-136">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-136">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ecfb6-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ecfb6-138">True</span><span class="sxs-lookup"><span data-stu-id="ecfb6-138">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ecfb6-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="ecfb6-139">Is Indexed</span></span>             | <span data-ttu-id="ecfb6-140">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-140">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ecfb6-141">In Global Catalog</span></span>      | <span data-ttu-id="ecfb6-142">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-142">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ecfb6-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecfb6-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ecfb6-144">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ecfb6-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecfb6-145">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecfb6-146">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecfb6-147">Search-Flags</span></span>           | <span data-ttu-id="ecfb6-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecfb6-148">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ecfb6-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecfb6-149">System-Flags</span></span>           | <span data-ttu-id="ecfb6-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecfb6-150">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ecfb6-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ecfb6-151">Classes used in</span></span>        | [<span data-ttu-id="ecfb6-152">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-152">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ecfb6-153">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ecfb6-154">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ecfb6-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ecfb6-155">Windows Server 2003</span></span>



| <span data-ttu-id="ecfb6-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="ecfb6-156">Entry</span></span> | <span data-ttu-id="ecfb6-157">Valor</span><span class="sxs-lookup"><span data-stu-id="ecfb6-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecfb6-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="ecfb6-158">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecfb6-159">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecfb6-160">System-Only</span></span>            | <span data-ttu-id="ecfb6-161">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-161">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ecfb6-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ecfb6-163">True</span><span class="sxs-lookup"><span data-stu-id="ecfb6-163">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ecfb6-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="ecfb6-164">Is Indexed</span></span>             | <span data-ttu-id="ecfb6-165">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-165">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ecfb6-166">In Global Catalog</span></span>      | <span data-ttu-id="ecfb6-167">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-167">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ecfb6-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecfb6-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ecfb6-169">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ecfb6-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecfb6-170">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecfb6-171">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecfb6-172">Search-Flags</span></span>           | <span data-ttu-id="ecfb6-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecfb6-173">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ecfb6-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecfb6-174">System-Flags</span></span>           | <span data-ttu-id="ecfb6-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecfb6-175">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ecfb6-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ecfb6-176">Classes used in</span></span>        | [<span data-ttu-id="ecfb6-177">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ecfb6-178">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-178">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ecfb6-179">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ecfb6-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ecfb6-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ecfb6-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="ecfb6-181">Entry</span></span> | <span data-ttu-id="ecfb6-182">Valor</span><span class="sxs-lookup"><span data-stu-id="ecfb6-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecfb6-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="ecfb6-183">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecfb6-184">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecfb6-185">System-Only</span></span>            | <span data-ttu-id="ecfb6-186">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-186">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ecfb6-187">Is-Single-Valued</span></span>       | <span data-ttu-id="ecfb6-188">True</span><span class="sxs-lookup"><span data-stu-id="ecfb6-188">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ecfb6-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="ecfb6-189">Is Indexed</span></span>             | <span data-ttu-id="ecfb6-190">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-190">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ecfb6-191">In Global Catalog</span></span>      | <span data-ttu-id="ecfb6-192">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-192">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ecfb6-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecfb6-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ecfb6-194">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ecfb6-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecfb6-195">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecfb6-196">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecfb6-197">Search-Flags</span></span>           | <span data-ttu-id="ecfb6-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecfb6-198">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ecfb6-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecfb6-199">System-Flags</span></span>           | <span data-ttu-id="ecfb6-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecfb6-200">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ecfb6-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ecfb6-201">Classes used in</span></span>        | [<span data-ttu-id="ecfb6-202">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-202">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ecfb6-203">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ecfb6-204">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-204">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ecfb6-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecfb6-205">Windows Server 2008</span></span>



| <span data-ttu-id="ecfb6-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="ecfb6-206">Entry</span></span> | <span data-ttu-id="ecfb6-207">Valor</span><span class="sxs-lookup"><span data-stu-id="ecfb6-207">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecfb6-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="ecfb6-208">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecfb6-209">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecfb6-210">System-Only</span></span>            | <span data-ttu-id="ecfb6-211">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-211">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ecfb6-212">Is-Single-Valued</span></span>       | <span data-ttu-id="ecfb6-213">True</span><span class="sxs-lookup"><span data-stu-id="ecfb6-213">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ecfb6-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="ecfb6-214">Is Indexed</span></span>             | <span data-ttu-id="ecfb6-215">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-215">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ecfb6-216">In Global Catalog</span></span>      | <span data-ttu-id="ecfb6-217">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-217">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ecfb6-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecfb6-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ecfb6-219">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ecfb6-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecfb6-220">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecfb6-221">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecfb6-222">Search-Flags</span></span>           | <span data-ttu-id="ecfb6-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecfb6-223">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ecfb6-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecfb6-224">System-Flags</span></span>           | <span data-ttu-id="ecfb6-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecfb6-225">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ecfb6-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ecfb6-226">Classes used in</span></span>        | [<span data-ttu-id="ecfb6-227">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-227">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ecfb6-228">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-228">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ecfb6-229">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-229">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ecfb6-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ecfb6-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ecfb6-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="ecfb6-231">Entry</span></span> | <span data-ttu-id="ecfb6-232">Valor</span><span class="sxs-lookup"><span data-stu-id="ecfb6-232">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecfb6-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="ecfb6-233">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecfb6-234">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecfb6-235">System-Only</span></span>            | <span data-ttu-id="ecfb6-236">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-236">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ecfb6-237">Is-Single-Valued</span></span>       | <span data-ttu-id="ecfb6-238">True</span><span class="sxs-lookup"><span data-stu-id="ecfb6-238">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ecfb6-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="ecfb6-239">Is Indexed</span></span>             | <span data-ttu-id="ecfb6-240">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-240">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ecfb6-241">In Global Catalog</span></span>      | <span data-ttu-id="ecfb6-242">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-242">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ecfb6-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecfb6-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ecfb6-244">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ecfb6-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecfb6-245">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecfb6-246">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecfb6-247">Search-Flags</span></span>           | <span data-ttu-id="ecfb6-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecfb6-248">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ecfb6-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecfb6-249">System-Flags</span></span>           | <span data-ttu-id="ecfb6-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecfb6-250">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ecfb6-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ecfb6-251">Classes used in</span></span>        | [<span data-ttu-id="ecfb6-252">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-252">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ecfb6-253">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-253">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ecfb6-254">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-254">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ecfb6-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ecfb6-255">Windows Server 2012</span></span>



| <span data-ttu-id="ecfb6-256">Entrada</span><span class="sxs-lookup"><span data-stu-id="ecfb6-256">Entry</span></span> | <span data-ttu-id="ecfb6-257">Valor</span><span class="sxs-lookup"><span data-stu-id="ecfb6-257">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecfb6-258">ID do link</span><span class="sxs-lookup"><span data-stu-id="ecfb6-258">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ecfb6-259">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="ecfb6-260">System-Only</span></span>            | <span data-ttu-id="ecfb6-261">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-261">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-262">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ecfb6-262">Is-Single-Valued</span></span>       | <span data-ttu-id="ecfb6-263">True</span><span class="sxs-lookup"><span data-stu-id="ecfb6-263">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ecfb6-264">É indexado</span><span class="sxs-lookup"><span data-stu-id="ecfb6-264">Is Indexed</span></span>             | <span data-ttu-id="ecfb6-265">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-265">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-266">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ecfb6-266">In Global Catalog</span></span>      | <span data-ttu-id="ecfb6-267">Falso</span><span class="sxs-lookup"><span data-stu-id="ecfb6-267">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ecfb6-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ecfb6-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="ecfb6-269">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ecfb6-269">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ecfb6-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ecfb6-270">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ecfb6-271">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ecfb6-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ecfb6-272">Search-Flags</span></span>           | <span data-ttu-id="ecfb6-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ecfb6-273">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ecfb6-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ecfb6-274">System-Flags</span></span>           | <span data-ttu-id="ecfb6-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecfb6-275">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ecfb6-276">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ecfb6-276">Classes used in</span></span>        | [<span data-ttu-id="ecfb6-277">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-277">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ecfb6-278">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-278">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ecfb6-279">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="ecfb6-279">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





