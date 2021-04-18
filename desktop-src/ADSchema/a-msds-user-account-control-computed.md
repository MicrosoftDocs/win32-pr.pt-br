---
title: atributo de controle de conta de usuário ms-DS-User-Control-computado
description: msDS-User-Account-Control-computado é muito parecido com userAccountControl, mas o valor do atributo pode conter bits adicionais que não são persistentes.
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo do MS-DS-User-Account-Control-computado
- msDS-conta de usuário-controle de atributo calculado do esquema do AD
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b5e9b047dd44d637b56cae8ded9e0991c46025
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105756306"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a><span data-ttu-id="f7aef-105">atributo de controle de conta de usuário ms-DS-User-Control-computado</span><span class="sxs-lookup"><span data-stu-id="f7aef-105">ms-DS-User-Account-Control-Computed attribute</span></span>

<span data-ttu-id="f7aef-106">**msDS-User-Account-Control-computado** é muito parecido com [**userAccountControl**](a-useraccountcontrol.md), mas o valor do atributo pode conter bits adicionais que não são persistentes.</span><span class="sxs-lookup"><span data-stu-id="f7aef-106">**msDS-User-Account-Control-Computed** is much like [**userAccountControl**](a-useraccountcontrol.md), but the attribute's value can contain additional bits that are not persisted.</span></span> <span data-ttu-id="f7aef-107">Os bits computados incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="f7aef-107">The computed bits include the following.</span></span>



| <span data-ttu-id="f7aef-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f7aef-108">Value</span></span>                | <span data-ttu-id="f7aef-109">Nome (definido em IADs. h)</span><span class="sxs-lookup"><span data-stu-id="f7aef-109">Name (defined in Iads.h)</span></span>                     |
|----------------------|----------------------------------------------|
| <span data-ttu-id="f7aef-110">0x0010</span><span class="sxs-lookup"><span data-stu-id="f7aef-110">0x0010</span></span><br/>    | <span data-ttu-id="f7aef-111">**bloqueio da UF \_**</span><span class="sxs-lookup"><span data-stu-id="f7aef-111">**UF\_LOCKOUT**</span></span><br/>                   |
| <span data-ttu-id="f7aef-112">0x800000</span><span class="sxs-lookup"><span data-stu-id="f7aef-112">0x800000</span></span><br/>  | <span data-ttu-id="f7aef-113">**UF de \_ senha \_ expirada**</span><span class="sxs-lookup"><span data-stu-id="f7aef-113">**UF\_PASSWORD\_EXPIRED**</span></span><br/>         |
| <span data-ttu-id="f7aef-114">0x4000000</span><span class="sxs-lookup"><span data-stu-id="f7aef-114">0x4000000</span></span><br/> | <span data-ttu-id="f7aef-115">**\_conta de \_ segredos parciais da UF \_**</span><span class="sxs-lookup"><span data-stu-id="f7aef-115">**UF\_PARTIAL\_SECRETS\_ACCOUNT**</span></span><br/> |
| <span data-ttu-id="f7aef-116">0x8000000</span><span class="sxs-lookup"><span data-stu-id="f7aef-116">0x8000000</span></span><br/> | <span data-ttu-id="f7aef-117">**UF de \_ uso de \_ \_ chaves AES**</span><span class="sxs-lookup"><span data-stu-id="f7aef-117">**UF\_USE\_AES\_KEYS**</span></span><br/>            |



 

<span data-ttu-id="f7aef-118">A lista completa de bits que o [**controle de conta de usuário**](a-useraccountcontrol.md) e, portanto, o **msDS-User-Account-Control-computated** também pode ser encontrada na página de referência de controle de conta de **usuário** (mapeada por meio do sinalizador [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) ) ou nas páginas de referência de gerenciamento de rede da estrutura [**informações do usuário \_ \_ 1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) .</span><span class="sxs-lookup"><span data-stu-id="f7aef-118">The full list of bits that [**User-Account-Control**](a-useraccountcontrol.md) and therefore **msDS-User-Account-Control-Computed** can also contain can be found in the **User-Account-Control** reference page (mapped through the [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) flagset) or on the network management reference pages for the [**user\_info\_1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) structure.</span></span>



| <span data-ttu-id="f7aef-119">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7aef-119">Entry</span></span> | <span data-ttu-id="f7aef-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f7aef-120">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f7aef-121">CN</span><span class="sxs-lookup"><span data-stu-id="f7aef-121">CN</span></span>                | <span data-ttu-id="f7aef-122">ms-DS-usuário-conta-controle-calculado</span><span class="sxs-lookup"><span data-stu-id="f7aef-122">ms-DS-User-Account-Control-Computed</span></span>  |
| <span data-ttu-id="f7aef-123">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f7aef-123">Ldap-Display-Name</span></span> | <span data-ttu-id="f7aef-124">msDS-conta de usuário-controle-computado</span><span class="sxs-lookup"><span data-stu-id="f7aef-124">msDS-User-Account-Control-Computed</span></span>   |
| <span data-ttu-id="f7aef-125">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f7aef-125">Size</span></span>              | \-                                   |
| <span data-ttu-id="f7aef-126">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f7aef-126">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f7aef-127">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f7aef-127">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f7aef-128">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f7aef-128">Attribute-Id</span></span>      | <span data-ttu-id="f7aef-129">1.2.840.113556.1.4.1460</span><span class="sxs-lookup"><span data-stu-id="f7aef-129">1.2.840.113556.1.4.1460</span></span>              |
| <span data-ttu-id="f7aef-130">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f7aef-130">System-Id-Guid</span></span>    | <span data-ttu-id="f7aef-131">2cc4b836-b63f-4940-8d23-ea7acf06af56</span><span class="sxs-lookup"><span data-stu-id="f7aef-131">2cc4b836-b63f-4940-8d23-ea7acf06af56</span></span> |
| <span data-ttu-id="f7aef-132">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7aef-132">Syntax</span></span>            | [<span data-ttu-id="f7aef-133">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="f7aef-133">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="f7aef-134">Implementações</span><span class="sxs-lookup"><span data-stu-id="f7aef-134">Implementations</span></span>

-   [<span data-ttu-id="f7aef-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f7aef-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f7aef-136">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f7aef-136">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f7aef-137">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f7aef-137">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f7aef-138">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f7aef-138">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f7aef-139">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f7aef-139">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f7aef-140">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f7aef-140">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f7aef-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f7aef-141">Windows Server 2003</span></span>



| <span data-ttu-id="f7aef-142">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7aef-142">Entry</span></span> | <span data-ttu-id="f7aef-143">Valor</span><span class="sxs-lookup"><span data-stu-id="f7aef-143">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7aef-144">ID do link</span><span class="sxs-lookup"><span data-stu-id="f7aef-144">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7aef-145">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7aef-145">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7aef-146">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7aef-146">System-Only</span></span>            | <span data-ttu-id="f7aef-147">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-147">False</span></span>                             |
| <span data-ttu-id="f7aef-148">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f7aef-148">Is-Single-Valued</span></span>       | <span data-ttu-id="f7aef-149">True</span><span class="sxs-lookup"><span data-stu-id="f7aef-149">True</span></span>                              |
| <span data-ttu-id="f7aef-150">É indexado</span><span class="sxs-lookup"><span data-stu-id="f7aef-150">Is Indexed</span></span>             | <span data-ttu-id="f7aef-151">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-151">False</span></span>                             |
| <span data-ttu-id="f7aef-152">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7aef-152">In Global Catalog</span></span>      | <span data-ttu-id="f7aef-153">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-153">False</span></span>                             |
| <span data-ttu-id="f7aef-154">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7aef-154">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7aef-155">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f7aef-155">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7aef-156">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7aef-156">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7aef-157">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7aef-157">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7aef-158">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7aef-158">Search-Flags</span></span>           | <span data-ttu-id="f7aef-159">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7aef-159">0x00000000</span></span>                        |
| <span data-ttu-id="f7aef-160">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7aef-160">System-Flags</span></span>           | <span data-ttu-id="f7aef-161">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f7aef-161">0x00000014</span></span>                        |
| <span data-ttu-id="f7aef-162">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f7aef-162">Classes used in</span></span>        | [<span data-ttu-id="f7aef-163">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f7aef-163">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f7aef-164">ADAM</span><span class="sxs-lookup"><span data-stu-id="f7aef-164">ADAM</span></span>



| <span data-ttu-id="f7aef-165">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7aef-165">Entry</span></span> | <span data-ttu-id="f7aef-166">Valor</span><span class="sxs-lookup"><span data-stu-id="f7aef-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f7aef-167">ID do link</span><span class="sxs-lookup"><span data-stu-id="f7aef-167">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f7aef-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7aef-168">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f7aef-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7aef-169">System-Only</span></span>            | <span data-ttu-id="f7aef-170">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-170">False</span></span>                                                             |
| <span data-ttu-id="f7aef-171">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f7aef-171">Is-Single-Valued</span></span>       | <span data-ttu-id="f7aef-172">True</span><span class="sxs-lookup"><span data-stu-id="f7aef-172">True</span></span>                                                              |
| <span data-ttu-id="f7aef-173">É indexado</span><span class="sxs-lookup"><span data-stu-id="f7aef-173">Is Indexed</span></span>             | <span data-ttu-id="f7aef-174">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-174">False</span></span>                                                             |
| <span data-ttu-id="f7aef-175">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7aef-175">In Global Catalog</span></span>      | <span data-ttu-id="f7aef-176">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-176">False</span></span>                                                             |
| <span data-ttu-id="f7aef-177">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7aef-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7aef-178">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f7aef-178">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f7aef-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7aef-179">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f7aef-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7aef-180">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f7aef-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7aef-181">Search-Flags</span></span>           | <span data-ttu-id="f7aef-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7aef-182">0x00000000</span></span>                                                        |
| <span data-ttu-id="f7aef-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7aef-183">System-Flags</span></span>           | <span data-ttu-id="f7aef-184">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f7aef-184">0x00000014</span></span>                                                        |
| <span data-ttu-id="f7aef-185">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f7aef-185">Classes used in</span></span>        | [<span data-ttu-id="f7aef-186">**ms-DS-Vinculed-Object**</span><span class="sxs-lookup"><span data-stu-id="f7aef-186">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f7aef-187">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f7aef-187">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f7aef-188">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7aef-188">Entry</span></span> | <span data-ttu-id="f7aef-189">Valor</span><span class="sxs-lookup"><span data-stu-id="f7aef-189">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7aef-190">ID do link</span><span class="sxs-lookup"><span data-stu-id="f7aef-190">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7aef-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7aef-191">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7aef-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7aef-192">System-Only</span></span>            | <span data-ttu-id="f7aef-193">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-193">False</span></span>                             |
| <span data-ttu-id="f7aef-194">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f7aef-194">Is-Single-Valued</span></span>       | <span data-ttu-id="f7aef-195">True</span><span class="sxs-lookup"><span data-stu-id="f7aef-195">True</span></span>                              |
| <span data-ttu-id="f7aef-196">É indexado</span><span class="sxs-lookup"><span data-stu-id="f7aef-196">Is Indexed</span></span>             | <span data-ttu-id="f7aef-197">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-197">False</span></span>                             |
| <span data-ttu-id="f7aef-198">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7aef-198">In Global Catalog</span></span>      | <span data-ttu-id="f7aef-199">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-199">False</span></span>                             |
| <span data-ttu-id="f7aef-200">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7aef-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7aef-201">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f7aef-201">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7aef-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7aef-202">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7aef-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7aef-203">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7aef-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7aef-204">Search-Flags</span></span>           | <span data-ttu-id="f7aef-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7aef-205">0x00000000</span></span>                        |
| <span data-ttu-id="f7aef-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7aef-206">System-Flags</span></span>           | <span data-ttu-id="f7aef-207">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f7aef-207">0x00000014</span></span>                        |
| <span data-ttu-id="f7aef-208">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f7aef-208">Classes used in</span></span>        | [<span data-ttu-id="f7aef-209">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f7aef-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f7aef-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7aef-210">Windows Server 2008</span></span>



| <span data-ttu-id="f7aef-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7aef-211">Entry</span></span> | <span data-ttu-id="f7aef-212">Valor</span><span class="sxs-lookup"><span data-stu-id="f7aef-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7aef-213">ID do link</span><span class="sxs-lookup"><span data-stu-id="f7aef-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7aef-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7aef-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7aef-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7aef-215">System-Only</span></span>            | <span data-ttu-id="f7aef-216">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-216">False</span></span>                             |
| <span data-ttu-id="f7aef-217">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f7aef-217">Is-Single-Valued</span></span>       | <span data-ttu-id="f7aef-218">True</span><span class="sxs-lookup"><span data-stu-id="f7aef-218">True</span></span>                              |
| <span data-ttu-id="f7aef-219">É indexado</span><span class="sxs-lookup"><span data-stu-id="f7aef-219">Is Indexed</span></span>             | <span data-ttu-id="f7aef-220">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-220">False</span></span>                             |
| <span data-ttu-id="f7aef-221">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7aef-221">In Global Catalog</span></span>      | <span data-ttu-id="f7aef-222">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-222">False</span></span>                             |
| <span data-ttu-id="f7aef-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7aef-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7aef-224">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f7aef-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7aef-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7aef-225">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7aef-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7aef-226">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7aef-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7aef-227">Search-Flags</span></span>           | <span data-ttu-id="f7aef-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7aef-228">0x00000000</span></span>                        |
| <span data-ttu-id="f7aef-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7aef-229">System-Flags</span></span>           | <span data-ttu-id="f7aef-230">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f7aef-230">0x00000014</span></span>                        |
| <span data-ttu-id="f7aef-231">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f7aef-231">Classes used in</span></span>        | [<span data-ttu-id="f7aef-232">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f7aef-232">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f7aef-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7aef-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f7aef-234">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7aef-234">Entry</span></span> | <span data-ttu-id="f7aef-235">Valor</span><span class="sxs-lookup"><span data-stu-id="f7aef-235">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7aef-236">ID do link</span><span class="sxs-lookup"><span data-stu-id="f7aef-236">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7aef-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7aef-237">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7aef-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7aef-238">System-Only</span></span>            | <span data-ttu-id="f7aef-239">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-239">False</span></span>                             |
| <span data-ttu-id="f7aef-240">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f7aef-240">Is-Single-Valued</span></span>       | <span data-ttu-id="f7aef-241">True</span><span class="sxs-lookup"><span data-stu-id="f7aef-241">True</span></span>                              |
| <span data-ttu-id="f7aef-242">É indexado</span><span class="sxs-lookup"><span data-stu-id="f7aef-242">Is Indexed</span></span>             | <span data-ttu-id="f7aef-243">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-243">False</span></span>                             |
| <span data-ttu-id="f7aef-244">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7aef-244">In Global Catalog</span></span>      | <span data-ttu-id="f7aef-245">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-245">False</span></span>                             |
| <span data-ttu-id="f7aef-246">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7aef-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7aef-247">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f7aef-247">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7aef-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7aef-248">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7aef-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7aef-249">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7aef-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7aef-250">Search-Flags</span></span>           | <span data-ttu-id="f7aef-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7aef-251">0x00000000</span></span>                        |
| <span data-ttu-id="f7aef-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7aef-252">System-Flags</span></span>           | <span data-ttu-id="f7aef-253">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f7aef-253">0x00000014</span></span>                        |
| <span data-ttu-id="f7aef-254">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f7aef-254">Classes used in</span></span>        | [<span data-ttu-id="f7aef-255">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f7aef-255">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f7aef-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7aef-256">Windows Server 2012</span></span>



| <span data-ttu-id="f7aef-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7aef-257">Entry</span></span> | <span data-ttu-id="f7aef-258">Valor</span><span class="sxs-lookup"><span data-stu-id="f7aef-258">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7aef-259">ID do link</span><span class="sxs-lookup"><span data-stu-id="f7aef-259">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7aef-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7aef-260">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7aef-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7aef-261">System-Only</span></span>            | <span data-ttu-id="f7aef-262">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-262">False</span></span>                             |
| <span data-ttu-id="f7aef-263">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f7aef-263">Is-Single-Valued</span></span>       | <span data-ttu-id="f7aef-264">True</span><span class="sxs-lookup"><span data-stu-id="f7aef-264">True</span></span>                              |
| <span data-ttu-id="f7aef-265">É indexado</span><span class="sxs-lookup"><span data-stu-id="f7aef-265">Is Indexed</span></span>             | <span data-ttu-id="f7aef-266">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-266">False</span></span>                             |
| <span data-ttu-id="f7aef-267">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7aef-267">In Global Catalog</span></span>      | <span data-ttu-id="f7aef-268">Falso</span><span class="sxs-lookup"><span data-stu-id="f7aef-268">False</span></span>                             |
| <span data-ttu-id="f7aef-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7aef-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7aef-270">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f7aef-270">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7aef-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7aef-271">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7aef-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7aef-272">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7aef-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7aef-273">Search-Flags</span></span>           | <span data-ttu-id="f7aef-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7aef-274">0x00000000</span></span>                        |
| <span data-ttu-id="f7aef-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7aef-275">System-Flags</span></span>           | <span data-ttu-id="f7aef-276">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f7aef-276">0x00000014</span></span>                        |
| <span data-ttu-id="f7aef-277">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f7aef-277">Classes used in</span></span>        | [<span data-ttu-id="f7aef-278">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f7aef-278">**User**</span></span>](c-user.md)<br/> |



 

