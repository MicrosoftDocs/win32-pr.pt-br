---
title: Atributo User-principal-Name
description: Esse atributo contém o UPN que é um nome de logon no estilo da Internet para um usuário baseado na RFC 822 padrão da Internet.
ms.assetid: 588e76fa-45b6-4853-821a-9e5730255b9f
ms.tgt_platform: multiple
keywords:
- Atributo User-principal-Name do AD Schema
- Esquema de atributo userPrincipalName do AD
topic_type:
- apiref
api_name:
- User-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffdb5bde76325409e0911615d1d21b1b4f593c06
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919413"
---
# <a name="user-principal-name-attribute"></a><span data-ttu-id="72e2d-105">Atributo User-principal-Name</span><span class="sxs-lookup"><span data-stu-id="72e2d-105">User-Principal-Name attribute</span></span>

<span data-ttu-id="72e2d-106">Esse atributo contém o UPN que é um nome de logon no estilo da Internet para um usuário baseado na [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)padrão da Internet.</span><span class="sxs-lookup"><span data-stu-id="72e2d-106">This attribute contains the UPN that is an Internet-style login name for a user based on the Internet standard [RFC 822](https://www.ietf.org/rfc/rfc0822.txt).</span></span> <span data-ttu-id="72e2d-107">O UPN é menor do que o nome distinto e mais fácil de lembrar.</span><span class="sxs-lookup"><span data-stu-id="72e2d-107">The UPN is shorter than the distinguished name and easier to remember.</span></span> <span data-ttu-id="72e2d-108">Por convenção, isso deve ser mapeado para o nome de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="72e2d-108">By convention, this should map to the user email name.</span></span> <span data-ttu-id="72e2d-109">O valor definido para esse atributo é igual ao comprimento da ID do usuário e do nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="72e2d-109">The value set for this attribute is equal to the length of the user's ID and the domain name.</span></span> <span data-ttu-id="72e2d-110">Para obter mais informações sobre esse atributo, consulte [atributos de nomenclatura de usuário](/windows/desktop/AD/naming-properties).</span><span class="sxs-lookup"><span data-stu-id="72e2d-110">For more information about this attribute, see [User Naming Attributes](/windows/desktop/AD/naming-properties).</span></span>



| <span data-ttu-id="72e2d-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="72e2d-111">Entry</span></span> | <span data-ttu-id="72e2d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="72e2d-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="72e2d-113">CN</span><span class="sxs-lookup"><span data-stu-id="72e2d-113">CN</span></span>                | <span data-ttu-id="72e2d-114">User-Principal-Name</span><span class="sxs-lookup"><span data-stu-id="72e2d-114">User-Principal-Name</span></span>                         |
| <span data-ttu-id="72e2d-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="72e2d-115">Ldap-Display-Name</span></span> | <span data-ttu-id="72e2d-116">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="72e2d-116">userPrincipalName</span></span>                           |
| <span data-ttu-id="72e2d-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="72e2d-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="72e2d-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="72e2d-118">Update Privilege</span></span>  | <span data-ttu-id="72e2d-119">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="72e2d-119">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="72e2d-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="72e2d-120">Update Frequency</span></span>  | <span data-ttu-id="72e2d-121">Em teoria, isso nunca deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="72e2d-121">In theory this should never change.</span></span>         |
| <span data-ttu-id="72e2d-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="72e2d-122">Attribute-Id</span></span>      | <span data-ttu-id="72e2d-123">1.2.840.113556.1.4.656</span><span class="sxs-lookup"><span data-stu-id="72e2d-123">1.2.840.113556.1.4.656</span></span>                      |
| <span data-ttu-id="72e2d-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="72e2d-124">System-Id-Guid</span></span>    | <span data-ttu-id="72e2d-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="72e2d-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="72e2d-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="72e2d-126">Syntax</span></span>            | [<span data-ttu-id="72e2d-127">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="72e2d-127">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="72e2d-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="72e2d-128">Implementations</span></span>

-   [<span data-ttu-id="72e2d-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="72e2d-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="72e2d-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="72e2d-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="72e2d-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="72e2d-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="72e2d-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="72e2d-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="72e2d-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="72e2d-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="72e2d-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="72e2d-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="72e2d-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="72e2d-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="72e2d-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="72e2d-136">Windows 2000 Server</span></span>



| <span data-ttu-id="72e2d-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="72e2d-137">Entry</span></span> | <span data-ttu-id="72e2d-138">Valor</span><span class="sxs-lookup"><span data-stu-id="72e2d-138">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72e2d-139">ID do link</span><span class="sxs-lookup"><span data-stu-id="72e2d-139">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72e2d-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e2d-140">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72e2d-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e2d-141">System-Only</span></span>            | <span data-ttu-id="72e2d-142">Falso</span><span class="sxs-lookup"><span data-stu-id="72e2d-142">False</span></span>                             |
| <span data-ttu-id="72e2d-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72e2d-143">Is-Single-Valued</span></span>       | <span data-ttu-id="72e2d-144">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-144">True</span></span>                              |
| <span data-ttu-id="72e2d-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="72e2d-145">Is Indexed</span></span>             | <span data-ttu-id="72e2d-146">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-146">True</span></span>                              |
| <span data-ttu-id="72e2d-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72e2d-147">In Global Catalog</span></span>      | <span data-ttu-id="72e2d-148">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-148">True</span></span>                              |
| <span data-ttu-id="72e2d-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72e2d-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e2d-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72e2d-150">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72e2d-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e2d-151">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72e2d-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e2d-152">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72e2d-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e2d-153">Search-Flags</span></span>           | <span data-ttu-id="72e2d-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72e2d-154">0x00000001</span></span>                        |
| <span data-ttu-id="72e2d-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e2d-155">System-Flags</span></span>           | <span data-ttu-id="72e2d-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72e2d-156">0x00000012</span></span>                        |
| <span data-ttu-id="72e2d-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72e2d-157">Classes used in</span></span>        | [<span data-ttu-id="72e2d-158">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="72e2d-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="72e2d-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72e2d-159">Windows Server 2003</span></span>



| <span data-ttu-id="72e2d-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="72e2d-160">Entry</span></span> | <span data-ttu-id="72e2d-161">Valor</span><span class="sxs-lookup"><span data-stu-id="72e2d-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72e2d-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="72e2d-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72e2d-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e2d-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72e2d-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e2d-164">System-Only</span></span>            | <span data-ttu-id="72e2d-165">Falso</span><span class="sxs-lookup"><span data-stu-id="72e2d-165">False</span></span>                             |
| <span data-ttu-id="72e2d-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72e2d-166">Is-Single-Valued</span></span>       | <span data-ttu-id="72e2d-167">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-167">True</span></span>                              |
| <span data-ttu-id="72e2d-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="72e2d-168">Is Indexed</span></span>             | <span data-ttu-id="72e2d-169">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-169">True</span></span>                              |
| <span data-ttu-id="72e2d-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72e2d-170">In Global Catalog</span></span>      | <span data-ttu-id="72e2d-171">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-171">True</span></span>                              |
| <span data-ttu-id="72e2d-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72e2d-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e2d-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72e2d-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72e2d-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e2d-174">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72e2d-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e2d-175">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72e2d-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e2d-176">Search-Flags</span></span>           | <span data-ttu-id="72e2d-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72e2d-177">0x00000001</span></span>                        |
| <span data-ttu-id="72e2d-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e2d-178">System-Flags</span></span>           | <span data-ttu-id="72e2d-179">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72e2d-179">0x00000012</span></span>                        |
| <span data-ttu-id="72e2d-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72e2d-180">Classes used in</span></span>        | [<span data-ttu-id="72e2d-181">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="72e2d-181">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="72e2d-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="72e2d-182">ADAM</span></span>



| <span data-ttu-id="72e2d-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="72e2d-183">Entry</span></span> | <span data-ttu-id="72e2d-184">Valor</span><span class="sxs-lookup"><span data-stu-id="72e2d-184">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="72e2d-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="72e2d-185">Link-Id</span></span>                | \-           |
| <span data-ttu-id="72e2d-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e2d-186">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="72e2d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e2d-187">System-Only</span></span>            | <span data-ttu-id="72e2d-188">Falso</span><span class="sxs-lookup"><span data-stu-id="72e2d-188">False</span></span>        |
| <span data-ttu-id="72e2d-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72e2d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="72e2d-190">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-190">True</span></span>         |
| <span data-ttu-id="72e2d-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="72e2d-191">Is Indexed</span></span>             | <span data-ttu-id="72e2d-192">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-192">True</span></span>         |
| <span data-ttu-id="72e2d-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72e2d-193">In Global Catalog</span></span>      | <span data-ttu-id="72e2d-194">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-194">True</span></span>         |
| <span data-ttu-id="72e2d-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72e2d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e2d-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72e2d-196">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="72e2d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e2d-197">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="72e2d-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e2d-198">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="72e2d-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e2d-199">Search-Flags</span></span>           | <span data-ttu-id="72e2d-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72e2d-200">0x00000001</span></span>   |
| <span data-ttu-id="72e2d-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e2d-201">System-Flags</span></span>           | <span data-ttu-id="72e2d-202">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72e2d-202">0x00000012</span></span>   |
| <span data-ttu-id="72e2d-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72e2d-203">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="72e2d-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="72e2d-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="72e2d-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="72e2d-205">Entry</span></span> | <span data-ttu-id="72e2d-206">Valor</span><span class="sxs-lookup"><span data-stu-id="72e2d-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72e2d-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="72e2d-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72e2d-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e2d-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72e2d-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e2d-209">System-Only</span></span>            | <span data-ttu-id="72e2d-210">Falso</span><span class="sxs-lookup"><span data-stu-id="72e2d-210">False</span></span>                             |
| <span data-ttu-id="72e2d-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72e2d-211">Is-Single-Valued</span></span>       | <span data-ttu-id="72e2d-212">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-212">True</span></span>                              |
| <span data-ttu-id="72e2d-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="72e2d-213">Is Indexed</span></span>             | <span data-ttu-id="72e2d-214">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-214">True</span></span>                              |
| <span data-ttu-id="72e2d-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72e2d-215">In Global Catalog</span></span>      | <span data-ttu-id="72e2d-216">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-216">True</span></span>                              |
| <span data-ttu-id="72e2d-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72e2d-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e2d-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72e2d-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72e2d-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e2d-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72e2d-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e2d-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72e2d-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e2d-221">Search-Flags</span></span>           | <span data-ttu-id="72e2d-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72e2d-222">0x00000001</span></span>                        |
| <span data-ttu-id="72e2d-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e2d-223">System-Flags</span></span>           | <span data-ttu-id="72e2d-224">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72e2d-224">0x00000012</span></span>                        |
| <span data-ttu-id="72e2d-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72e2d-225">Classes used in</span></span>        | [<span data-ttu-id="72e2d-226">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="72e2d-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="72e2d-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72e2d-227">Windows Server 2008</span></span>



| <span data-ttu-id="72e2d-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="72e2d-228">Entry</span></span> | <span data-ttu-id="72e2d-229">Valor</span><span class="sxs-lookup"><span data-stu-id="72e2d-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72e2d-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="72e2d-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72e2d-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e2d-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72e2d-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e2d-232">System-Only</span></span>            | <span data-ttu-id="72e2d-233">Falso</span><span class="sxs-lookup"><span data-stu-id="72e2d-233">False</span></span>                             |
| <span data-ttu-id="72e2d-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72e2d-234">Is-Single-Valued</span></span>       | <span data-ttu-id="72e2d-235">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-235">True</span></span>                              |
| <span data-ttu-id="72e2d-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="72e2d-236">Is Indexed</span></span>             | <span data-ttu-id="72e2d-237">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-237">True</span></span>                              |
| <span data-ttu-id="72e2d-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72e2d-238">In Global Catalog</span></span>      | <span data-ttu-id="72e2d-239">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-239">True</span></span>                              |
| <span data-ttu-id="72e2d-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72e2d-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e2d-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72e2d-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72e2d-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e2d-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72e2d-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e2d-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72e2d-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e2d-244">Search-Flags</span></span>           | <span data-ttu-id="72e2d-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72e2d-245">0x00000001</span></span>                        |
| <span data-ttu-id="72e2d-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e2d-246">System-Flags</span></span>           | <span data-ttu-id="72e2d-247">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72e2d-247">0x00000012</span></span>                        |
| <span data-ttu-id="72e2d-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72e2d-248">Classes used in</span></span>        | [<span data-ttu-id="72e2d-249">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="72e2d-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="72e2d-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72e2d-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="72e2d-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="72e2d-251">Entry</span></span> | <span data-ttu-id="72e2d-252">Valor</span><span class="sxs-lookup"><span data-stu-id="72e2d-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72e2d-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="72e2d-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72e2d-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e2d-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72e2d-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e2d-255">System-Only</span></span>            | <span data-ttu-id="72e2d-256">Falso</span><span class="sxs-lookup"><span data-stu-id="72e2d-256">False</span></span>                             |
| <span data-ttu-id="72e2d-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72e2d-257">Is-Single-Valued</span></span>       | <span data-ttu-id="72e2d-258">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-258">True</span></span>                              |
| <span data-ttu-id="72e2d-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="72e2d-259">Is Indexed</span></span>             | <span data-ttu-id="72e2d-260">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-260">True</span></span>                              |
| <span data-ttu-id="72e2d-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72e2d-261">In Global Catalog</span></span>      | <span data-ttu-id="72e2d-262">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-262">True</span></span>                              |
| <span data-ttu-id="72e2d-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72e2d-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e2d-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72e2d-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72e2d-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e2d-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72e2d-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e2d-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72e2d-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e2d-267">Search-Flags</span></span>           | <span data-ttu-id="72e2d-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72e2d-268">0x00000001</span></span>                        |
| <span data-ttu-id="72e2d-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e2d-269">System-Flags</span></span>           | <span data-ttu-id="72e2d-270">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72e2d-270">0x00000012</span></span>                        |
| <span data-ttu-id="72e2d-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72e2d-271">Classes used in</span></span>        | [<span data-ttu-id="72e2d-272">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="72e2d-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="72e2d-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72e2d-273">Windows Server 2012</span></span>



| <span data-ttu-id="72e2d-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="72e2d-274">Entry</span></span> | <span data-ttu-id="72e2d-275">Valor</span><span class="sxs-lookup"><span data-stu-id="72e2d-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72e2d-276">ID do link</span><span class="sxs-lookup"><span data-stu-id="72e2d-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72e2d-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e2d-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72e2d-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e2d-278">System-Only</span></span>            | <span data-ttu-id="72e2d-279">Falso</span><span class="sxs-lookup"><span data-stu-id="72e2d-279">False</span></span>                             |
| <span data-ttu-id="72e2d-280">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72e2d-280">Is-Single-Valued</span></span>       | <span data-ttu-id="72e2d-281">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-281">True</span></span>                              |
| <span data-ttu-id="72e2d-282">É indexado</span><span class="sxs-lookup"><span data-stu-id="72e2d-282">Is Indexed</span></span>             | <span data-ttu-id="72e2d-283">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-283">True</span></span>                              |
| <span data-ttu-id="72e2d-284">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72e2d-284">In Global Catalog</span></span>      | <span data-ttu-id="72e2d-285">True</span><span class="sxs-lookup"><span data-stu-id="72e2d-285">True</span></span>                              |
| <span data-ttu-id="72e2d-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72e2d-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e2d-287">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72e2d-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72e2d-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e2d-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72e2d-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e2d-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72e2d-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e2d-290">Search-Flags</span></span>           | <span data-ttu-id="72e2d-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72e2d-291">0x00000001</span></span>                        |
| <span data-ttu-id="72e2d-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e2d-292">System-Flags</span></span>           | <span data-ttu-id="72e2d-293">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72e2d-293">0x00000012</span></span>                        |
| <span data-ttu-id="72e2d-294">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72e2d-294">Classes used in</span></span>        | [<span data-ttu-id="72e2d-295">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="72e2d-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="72e2d-296">Comentários</span><span class="sxs-lookup"><span data-stu-id="72e2d-296">Remarks</span></span>

<span data-ttu-id="72e2d-297">No ADAM, esse atributo não precisa estar no formato padrão RFC 822 da Internet; pode ser um nome simples.</span><span class="sxs-lookup"><span data-stu-id="72e2d-297">In ADAM, this attribute is not required to be in the Internet standard RFC 822 format; it can be a simple name.</span></span>

 

