---
title: Lockout-Duration atributo
description: A quantidade de tempo em que uma conta é bloqueada devido à Lockout-Threshold sendo excedida.
ms.assetid: 6a26ef80-86ed-433f-9032-cdd1aaf00388
ms.tgt_platform: multiple
keywords:
- Esquema de Lockout-Duration do atributo AD
- Esquema de AD do atributo lockoutDuration
topic_type:
- apiref
api_name:
- Lockout-Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526fedef47bea20148a591259dbc7ec1702b5a15
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105753825"
---
# <a name="lockout-duration-attribute"></a><span data-ttu-id="0d24b-105">Lockout-Duration atributo</span><span class="sxs-lookup"><span data-stu-id="0d24b-105">Lockout-Duration attribute</span></span>

<span data-ttu-id="0d24b-106">A quantidade de tempo que uma conta está bloqueada devido ao [**limite de bloqueio**](a-lockoutthreshold.md) ser excedido.</span><span class="sxs-lookup"><span data-stu-id="0d24b-106">The amount of time that an account is locked due to the [**Lockout-Threshold**](a-lockoutthreshold.md) being exceeded.</span></span> <span data-ttu-id="0d24b-107">Esse valor é armazenado como um inteiro grande que representa o negativo do número de intervalos de 100 a nanossegundos a partir do momento em que o [**limite de bloqueio**](a-lockoutthreshold.md) é excedido e deve decorrer antes que a conta seja desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="0d24b-107">This value is stored as a large integer that represents the negative of the number of 100-nanosecond intervals from the time the [**Lockout-Threshold**](a-lockoutthreshold.md) is exceeded that must elapse before the account is unlocked.</span></span>



| <span data-ttu-id="0d24b-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d24b-108">Entry</span></span> | <span data-ttu-id="0d24b-109">Valor</span><span class="sxs-lookup"><span data-stu-id="0d24b-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0d24b-110">CN</span><span class="sxs-lookup"><span data-stu-id="0d24b-110">CN</span></span>                | <span data-ttu-id="0d24b-111">Lockout-Duration</span><span class="sxs-lookup"><span data-stu-id="0d24b-111">Lockout-Duration</span></span>                     |
| <span data-ttu-id="0d24b-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0d24b-112">Ldap-Display-Name</span></span> | <span data-ttu-id="0d24b-113">lockoutDuration</span><span class="sxs-lookup"><span data-stu-id="0d24b-113">lockoutDuration</span></span>                      |
| <span data-ttu-id="0d24b-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0d24b-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="0d24b-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="0d24b-115">Update Privilege</span></span>  | <span data-ttu-id="0d24b-116">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="0d24b-116">Domain administrator</span></span>                 |
| <span data-ttu-id="0d24b-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="0d24b-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="0d24b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0d24b-118">Attribute-Id</span></span>      | <span data-ttu-id="0d24b-119">1.2.840.113556.1.4.60</span><span class="sxs-lookup"><span data-stu-id="0d24b-119">1.2.840.113556.1.4.60</span></span>                |
| <span data-ttu-id="0d24b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0d24b-120">System-Id-Guid</span></span>    | <span data-ttu-id="0d24b-121">bf9679a5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0d24b-121">bf9679a5-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="0d24b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d24b-122">Syntax</span></span>            | [<span data-ttu-id="0d24b-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="0d24b-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="0d24b-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="0d24b-124">Implementations</span></span>

-   [<span data-ttu-id="0d24b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0d24b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0d24b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0d24b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0d24b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0d24b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0d24b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0d24b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0d24b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0d24b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0d24b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0d24b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0d24b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0d24b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0d24b-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d24b-132">Entry</span></span> | <span data-ttu-id="0d24b-133">Valor</span><span class="sxs-lookup"><span data-stu-id="0d24b-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d24b-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="0d24b-134">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d24b-135">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d24b-136">System-Only</span></span>            | <span data-ttu-id="0d24b-137">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-137">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0d24b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0d24b-139">True</span><span class="sxs-lookup"><span data-stu-id="0d24b-139">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="0d24b-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="0d24b-140">Is Indexed</span></span>             | <span data-ttu-id="0d24b-141">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-141">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0d24b-142">In Global Catalog</span></span>      | <span data-ttu-id="0d24b-143">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-143">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0d24b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d24b-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0d24b-145">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="0d24b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d24b-146">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d24b-147">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d24b-148">Search-Flags</span></span>           | <span data-ttu-id="0d24b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d24b-149">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="0d24b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d24b-150">System-Flags</span></span>           | <span data-ttu-id="0d24b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d24b-151">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="0d24b-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0d24b-152">Classes used in</span></span>        | [<span data-ttu-id="0d24b-153">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="0d24b-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="0d24b-154">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="0d24b-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="0d24b-155">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="0d24b-155">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0d24b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0d24b-156">Windows Server 2003</span></span>



| <span data-ttu-id="0d24b-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d24b-157">Entry</span></span> | <span data-ttu-id="0d24b-158">Valor</span><span class="sxs-lookup"><span data-stu-id="0d24b-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d24b-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="0d24b-159">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d24b-160">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d24b-161">System-Only</span></span>            | <span data-ttu-id="0d24b-162">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-162">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0d24b-163">Is-Single-Valued</span></span>       | <span data-ttu-id="0d24b-164">True</span><span class="sxs-lookup"><span data-stu-id="0d24b-164">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="0d24b-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="0d24b-165">Is Indexed</span></span>             | <span data-ttu-id="0d24b-166">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-166">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0d24b-167">In Global Catalog</span></span>      | <span data-ttu-id="0d24b-168">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-168">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0d24b-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d24b-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0d24b-170">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="0d24b-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d24b-171">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d24b-172">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d24b-173">Search-Flags</span></span>           | <span data-ttu-id="0d24b-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d24b-174">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="0d24b-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d24b-175">System-Flags</span></span>           | <span data-ttu-id="0d24b-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d24b-176">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="0d24b-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0d24b-177">Classes used in</span></span>        | [<span data-ttu-id="0d24b-178">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="0d24b-178">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="0d24b-179">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="0d24b-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="0d24b-180">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="0d24b-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0d24b-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0d24b-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0d24b-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d24b-182">Entry</span></span> | <span data-ttu-id="0d24b-183">Valor</span><span class="sxs-lookup"><span data-stu-id="0d24b-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d24b-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="0d24b-184">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d24b-185">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d24b-186">System-Only</span></span>            | <span data-ttu-id="0d24b-187">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-187">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0d24b-188">Is-Single-Valued</span></span>       | <span data-ttu-id="0d24b-189">True</span><span class="sxs-lookup"><span data-stu-id="0d24b-189">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="0d24b-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="0d24b-190">Is Indexed</span></span>             | <span data-ttu-id="0d24b-191">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-191">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0d24b-192">In Global Catalog</span></span>      | <span data-ttu-id="0d24b-193">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-193">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0d24b-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d24b-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0d24b-195">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="0d24b-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d24b-196">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d24b-197">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d24b-198">Search-Flags</span></span>           | <span data-ttu-id="0d24b-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d24b-199">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="0d24b-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d24b-200">System-Flags</span></span>           | <span data-ttu-id="0d24b-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d24b-201">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="0d24b-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0d24b-202">Classes used in</span></span>        | [<span data-ttu-id="0d24b-203">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="0d24b-203">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="0d24b-204">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="0d24b-204">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="0d24b-205">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="0d24b-205">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0d24b-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d24b-206">Windows Server 2008</span></span>



| <span data-ttu-id="0d24b-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d24b-207">Entry</span></span> | <span data-ttu-id="0d24b-208">Valor</span><span class="sxs-lookup"><span data-stu-id="0d24b-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d24b-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="0d24b-209">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d24b-210">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d24b-211">System-Only</span></span>            | <span data-ttu-id="0d24b-212">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-212">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0d24b-213">Is-Single-Valued</span></span>       | <span data-ttu-id="0d24b-214">True</span><span class="sxs-lookup"><span data-stu-id="0d24b-214">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="0d24b-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="0d24b-215">Is Indexed</span></span>             | <span data-ttu-id="0d24b-216">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-216">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0d24b-217">In Global Catalog</span></span>      | <span data-ttu-id="0d24b-218">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-218">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0d24b-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d24b-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0d24b-220">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="0d24b-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d24b-221">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d24b-222">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d24b-223">Search-Flags</span></span>           | <span data-ttu-id="0d24b-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d24b-224">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="0d24b-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d24b-225">System-Flags</span></span>           | <span data-ttu-id="0d24b-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d24b-226">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="0d24b-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0d24b-227">Classes used in</span></span>        | [<span data-ttu-id="0d24b-228">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="0d24b-228">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="0d24b-229">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="0d24b-229">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="0d24b-230">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="0d24b-230">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0d24b-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0d24b-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0d24b-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d24b-232">Entry</span></span> | <span data-ttu-id="0d24b-233">Valor</span><span class="sxs-lookup"><span data-stu-id="0d24b-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d24b-234">ID do link</span><span class="sxs-lookup"><span data-stu-id="0d24b-234">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d24b-235">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d24b-236">System-Only</span></span>            | <span data-ttu-id="0d24b-237">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-237">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-238">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0d24b-238">Is-Single-Valued</span></span>       | <span data-ttu-id="0d24b-239">True</span><span class="sxs-lookup"><span data-stu-id="0d24b-239">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="0d24b-240">É indexado</span><span class="sxs-lookup"><span data-stu-id="0d24b-240">Is Indexed</span></span>             | <span data-ttu-id="0d24b-241">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-241">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-242">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0d24b-242">In Global Catalog</span></span>      | <span data-ttu-id="0d24b-243">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-243">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0d24b-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d24b-245">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0d24b-245">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="0d24b-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d24b-246">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d24b-247">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d24b-248">Search-Flags</span></span>           | <span data-ttu-id="0d24b-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d24b-249">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="0d24b-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d24b-250">System-Flags</span></span>           | <span data-ttu-id="0d24b-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d24b-251">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="0d24b-252">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0d24b-252">Classes used in</span></span>        | [<span data-ttu-id="0d24b-253">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="0d24b-253">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="0d24b-254">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="0d24b-254">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="0d24b-255">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="0d24b-255">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0d24b-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0d24b-256">Windows Server 2012</span></span>



| <span data-ttu-id="0d24b-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d24b-257">Entry</span></span> | <span data-ttu-id="0d24b-258">Valor</span><span class="sxs-lookup"><span data-stu-id="0d24b-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d24b-259">ID do link</span><span class="sxs-lookup"><span data-stu-id="0d24b-259">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d24b-260">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d24b-261">System-Only</span></span>            | <span data-ttu-id="0d24b-262">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-262">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-263">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0d24b-263">Is-Single-Valued</span></span>       | <span data-ttu-id="0d24b-264">True</span><span class="sxs-lookup"><span data-stu-id="0d24b-264">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="0d24b-265">É indexado</span><span class="sxs-lookup"><span data-stu-id="0d24b-265">Is Indexed</span></span>             | <span data-ttu-id="0d24b-266">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-266">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-267">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0d24b-267">In Global Catalog</span></span>      | <span data-ttu-id="0d24b-268">Falso</span><span class="sxs-lookup"><span data-stu-id="0d24b-268">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0d24b-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0d24b-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d24b-270">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0d24b-270">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="0d24b-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d24b-271">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d24b-272">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0d24b-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d24b-273">Search-Flags</span></span>           | <span data-ttu-id="0d24b-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d24b-274">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="0d24b-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d24b-275">System-Flags</span></span>           | <span data-ttu-id="0d24b-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d24b-276">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="0d24b-277">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0d24b-277">Classes used in</span></span>        | [<span data-ttu-id="0d24b-278">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="0d24b-278">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="0d24b-279">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="0d24b-279">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="0d24b-280">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="0d24b-280">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="0d24b-281">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d24b-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d24b-282">**Limite de bloqueio**</span><span class="sxs-lookup"><span data-stu-id="0d24b-282">**Lockout-Threshold**</span></span>](a-lockoutthreshold.md)
</dt> </dl>

 

 





