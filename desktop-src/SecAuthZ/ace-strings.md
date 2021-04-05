---
description: Explica as cadeias de caracteres usadas em uma entrada de controle de acesso.
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: Cadeias de caracteres ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a35bde18a1ca3ac416faa42e3b693e26305beb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662053"
---
# <a name="ace-strings"></a><span data-ttu-id="14683-103">Cadeias de caracteres ACE</span><span class="sxs-lookup"><span data-stu-id="14683-103">ACE Strings</span></span>

<span data-ttu-id="14683-104">A [linguagem de definição do descritor de segurança](security-descriptor-definition-language.md) (SDDL) usa cadeias de caracteres Ace nos componentes DACL e SACL de uma cadeia de caracteres de [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) .</span><span class="sxs-lookup"><span data-stu-id="14683-104">The [security descriptor definition language](security-descriptor-definition-language.md) (SDDL) uses ACE strings in the DACL and SACL components of a [*security descriptor*](/windows/desktop/SecGloss/s-gly) string.</span></span>

<span data-ttu-id="14683-105">Conforme mostrado nos exemplos de [formato de cadeia de caracteres do descritor de segurança](security-descriptor-string-format.md) , cada ACE em uma cadeia de caracteres de descritor de segurança é colocado entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="14683-105">As shown in the [Security Descriptor String Format](security-descriptor-string-format.md) examples, each ACE in a security descriptor string is enclosed in parentheses.</span></span> <span data-ttu-id="14683-106">Os campos da ACE estão na seguinte ordem e são separados por ponto e vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="14683-106">The fields of the ACE are in the following order and are separated by semicolons (;).</span></span>

> [!Note]  
> <span data-ttu-id="14683-107">Há um formato diferente para as ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) condicionais que outros tipos de Ace.</span><span class="sxs-lookup"><span data-stu-id="14683-107">There is a different format for conditional [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) than other ACE types.</span></span> <span data-ttu-id="14683-108">Para ACEs condicionais, consulte [linguagem de definição do descritor de segurança para aces condicionais](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="14683-108">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a><span data-ttu-id="14683-109">Campos</span><span class="sxs-lookup"><span data-stu-id="14683-109">Fields</span></span>

<dl> <dt>

<span data-ttu-id="14683-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**tipo de Ace \_**</span><span class="sxs-lookup"><span data-stu-id="14683-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**ace\_type**</span></span>
</dt> <dd>

<span data-ttu-id="14683-111">Uma cadeia de caracteres que indica o valor do membro **AceType** da estrutura de [**\_ cabeçalho Ace**](/windows/desktop/api/Winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="14683-111">A string that indicates the value of the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="14683-112">A cadeia do tipo ACE pode ser uma das seguintes cadeias de caracteres definidas em SDDL. h.</span><span class="sxs-lookup"><span data-stu-id="14683-112">The ACE type string can be one of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="14683-113">ACE tipo String</span><span class="sxs-lookup"><span data-stu-id="14683-113">ACE type string</span></span> | <span data-ttu-id="14683-114">Constante em SDDL. h</span><span class="sxs-lookup"><span data-stu-id="14683-114">Constant in Sddl.h</span></span>                      | <span data-ttu-id="14683-115">Valor de AceType</span><span class="sxs-lookup"><span data-stu-id="14683-115">AceType value</span></span>                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14683-116">"A"</span><span class="sxs-lookup"><span data-stu-id="14683-116">"A"</span></span>             | <span data-ttu-id="14683-117">acesso de SDDL \_ \_ permitido</span><span class="sxs-lookup"><span data-stu-id="14683-117">SDDL\_ACCESS\_ALLOWED</span></span>                   | <span data-ttu-id="14683-118">\_tipo de \_ Ace \_ permitido de acesso</span><span class="sxs-lookup"><span data-stu-id="14683-118">ACCESS\_ALLOWED\_ACE\_TYPE</span></span>                                                                                                                                         |
| <span data-ttu-id="14683-119">"D"</span><span class="sxs-lookup"><span data-stu-id="14683-119">"D"</span></span>             | <span data-ttu-id="14683-120">acesso de SDDL \_ \_ negado</span><span class="sxs-lookup"><span data-stu-id="14683-120">SDDL\_ACCESS\_DENIED</span></span>                    | <span data-ttu-id="14683-121">tipo de ACE de acesso \_ negado \_ \_</span><span class="sxs-lookup"><span data-stu-id="14683-121">ACCESS\_DENIED\_ACE\_TYPE</span></span>                                                                                                                                          |
| <span data-ttu-id="14683-122">OA</span><span class="sxs-lookup"><span data-stu-id="14683-122">"OA"</span></span>            | <span data-ttu-id="14683-123">\_acesso de objeto SDDL \_ \_ permitido</span><span class="sxs-lookup"><span data-stu-id="14683-123">SDDL\_OBJECT\_ACCESS\_ALLOWED</span></span>           | <span data-ttu-id="14683-124">\_tipo de \_ ACE de objeto permitido \_ de acesso \_</span><span class="sxs-lookup"><span data-stu-id="14683-124">ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                 |
| <span data-ttu-id="14683-125">OD</span><span class="sxs-lookup"><span data-stu-id="14683-125">"OD"</span></span>            | <span data-ttu-id="14683-126">\_ \_ acesso \_ negado ao objeto SDDL</span><span class="sxs-lookup"><span data-stu-id="14683-126">SDDL\_OBJECT\_ACCESS\_DENIED</span></span>            | <span data-ttu-id="14683-127">tipo de ACE de objeto de acesso \_ negado \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="14683-127">ACCESS\_DENIED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                  |
| <span data-ttu-id="14683-128">AU</span><span class="sxs-lookup"><span data-stu-id="14683-128">"AU"</span></span>            | <span data-ttu-id="14683-129">auditoria de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-129">SDDL\_AUDIT</span></span>                             | <span data-ttu-id="14683-130">\_tipo de \_ ACE de auditoria do sistema \_</span><span class="sxs-lookup"><span data-stu-id="14683-130">SYSTEM\_AUDIT\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="14683-131">"AL"</span><span class="sxs-lookup"><span data-stu-id="14683-131">"AL"</span></span>            | <span data-ttu-id="14683-132">\_alarme SDDL</span><span class="sxs-lookup"><span data-stu-id="14683-132">SDDL\_ALARM</span></span>                             | <span data-ttu-id="14683-133">\_tipo de \_ Ace do alarme do sistema \_</span><span class="sxs-lookup"><span data-stu-id="14683-133">SYSTEM\_ALARM\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="14683-134">CN</span><span class="sxs-lookup"><span data-stu-id="14683-134">"OU"</span></span>            | <span data-ttu-id="14683-135">\_auditoria de objeto SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-135">SDDL\_OBJECT\_AUDIT</span></span>                     | <span data-ttu-id="14683-136">\_ \_ tipo ACE do objeto Audit \_ do \_ sistema</span><span class="sxs-lookup"><span data-stu-id="14683-136">SYSTEM\_AUDIT\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="14683-137">OL</span><span class="sxs-lookup"><span data-stu-id="14683-137">"OL"</span></span>            | <span data-ttu-id="14683-138">\_alarme do objeto SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-138">SDDL\_OBJECT\_ALARM</span></span>                     | <span data-ttu-id="14683-139">\_ \_ tipo ACE do objeto Alarm \_ do \_ sistema</span><span class="sxs-lookup"><span data-stu-id="14683-139">SYSTEM\_ALARM\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="14683-140">ML</span><span class="sxs-lookup"><span data-stu-id="14683-140">"ML"</span></span>            | <span data-ttu-id="14683-141">\_rótulo obrigatório de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-141">SDDL\_MANDATORY\_LABEL</span></span>                  | <span data-ttu-id="14683-142">\_tipo de \_ ACE de rótulo obrigatório \_ do sistema \_</span><span class="sxs-lookup"><span data-stu-id="14683-142">SYSTEM\_MANDATORY\_LABEL\_ACE\_TYPE</span></span>                                                                                                                                |
| <span data-ttu-id="14683-143">XA</span><span class="sxs-lookup"><span data-stu-id="14683-143">"XA"</span></span>            | <span data-ttu-id="14683-144">\_acesso de retorno de chamada SDDL \_ \_ permitido</span><span class="sxs-lookup"><span data-stu-id="14683-144">SDDL\_CALLBACK\_ACCESS\_ALLOWED</span></span>         | <span data-ttu-id="14683-145">ACESSO \_ permitido \_ retorno \_ de chamada Ace \_ tipo **windows vista e Windows Server 2003:** não disponível.</span><span class="sxs-lookup"><span data-stu-id="14683-145">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Vista and Windows Server 2003:** Not available.</span></span><br/>                                                           |
| <span data-ttu-id="14683-146">XD</span><span class="sxs-lookup"><span data-stu-id="14683-146">"XD"</span></span>            | <span data-ttu-id="14683-147">\_acesso de retorno de chamada SDDL \_ \_ negado</span><span class="sxs-lookup"><span data-stu-id="14683-147">SDDL\_CALLBACK\_ACCESS\_DENIED</span></span>          | <span data-ttu-id="14683-148">ACESSO \_ negado ao \_ retorno \_ de chamada Ace \_ tipo **windows vista e Windows Server 2003:** não disponível.</span><span class="sxs-lookup"><span data-stu-id="14683-148">ACCESS\_DENIED\_CALLBACK\_ACE\_TYPE **Windows Vista and Windows Server 2003:** Not available.</span></span><br/>                                                            |
| <span data-ttu-id="14683-149">ARQUITETURA</span><span class="sxs-lookup"><span data-stu-id="14683-149">"RA"</span></span>            | <span data-ttu-id="14683-150">\_atributo de recurso SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-150">SDDL\_RESOURCE\_ATTRIBUTE</span></span>               | <span data-ttu-id="14683-151">\_Tipo de Ace do atributo de recurso do sistema \_ \_ \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows vista e Windows Server 2003:** não disponível.</span><span class="sxs-lookup"><span data-stu-id="14683-151">SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/> |
| <span data-ttu-id="14683-152">SP3</span><span class="sxs-lookup"><span data-stu-id="14683-152">"SP"</span></span>            | <span data-ttu-id="14683-153">ID da política com \_ escopo SDDL \_ \_</span><span class="sxs-lookup"><span data-stu-id="14683-153">SDDL\_SCOPED\_POLICY\_ID</span></span>                | <span data-ttu-id="14683-154">ID da política com escopo do sistema \_ \_ \_ \_ ACE \_ tipo **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista e Windows Server 2003:** não disponível.</span><span class="sxs-lookup"><span data-stu-id="14683-154">SYSTEM\_SCOPED\_POLICY\_ID\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>  |
| <span data-ttu-id="14683-155">"XU"</span><span class="sxs-lookup"><span data-stu-id="14683-155">"XU"</span></span>            | <span data-ttu-id="14683-156">\_auditoria de retorno de chamada SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-156">SDDL\_CALLBACK\_AUDIT</span></span>                   | <span data-ttu-id="14683-157">\_Tipo de \_ retorno de chamada \_ de auditoria do sistema \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows vista e Windows Server 2003:** não disponível.</span><span class="sxs-lookup"><span data-stu-id="14683-157">SYSTEM\_AUDIT\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>     |
| <span data-ttu-id="14683-158">ZA</span><span class="sxs-lookup"><span data-stu-id="14683-158">"ZA"</span></span>            | <span data-ttu-id="14683-159">\_acesso de objeto de retorno de chamada SDDL \_ \_ \_ permitido</span><span class="sxs-lookup"><span data-stu-id="14683-159">SDDL\_CALLBACK\_OBJECT\_ACCESS\_ALLOWED</span></span> | <span data-ttu-id="14683-160">ACESSO \_ permitido \_ retorno de chamada \_ Ace \_ tipo **Windows Server 2008 R2, windows 7, Windows Server 2008, windows vista e Windows Server 2003:** não disponível.</span><span class="sxs-lookup"><span data-stu-id="14683-160">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>   |



 

> [!Note]  
> <span data-ttu-id="14683-161">Se **o \_ tipo ACE** for \_ \_ \_ o tipo de ACE de objeto permitido \_ de acesso e nenhum GUID de **objeto \_** nem **herdar o \_ \_ GUID de objeto** tiver um [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) especificado, [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) converterá o **\_ tipo ACE** para acessar o \_ \_ tipo de Ace permitido \_ .</span><span class="sxs-lookup"><span data-stu-id="14683-161">If **ace\_type** is ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE and neither **object\_guid** nor **inherit\_object\_guid** has a [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) specified, then [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) converts **ace\_type** to ACCESS\_ALLOWED\_ACE\_TYPE.</span></span>

 

</dd> <dt>

<span data-ttu-id="14683-162"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**sinalizadores de Ace \_**</span><span class="sxs-lookup"><span data-stu-id="14683-162"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**ace\_flags**</span></span>
</dt> <dd>

<span data-ttu-id="14683-163">Uma cadeia de caracteres que indica o valor do membro **AceFlags** da estrutura de [**\_ cabeçalho Ace**](/windows/desktop/api/Winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="14683-163">A string that indicates the value of the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="14683-164">A cadeia de caracteres de sinalizadores de ACE pode ser uma concatenação das seguintes seqüências definidas em SDDL. h.</span><span class="sxs-lookup"><span data-stu-id="14683-164">The ACE flags string can be a concatenation of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="14683-165">Cadeia de caracteres de sinalizadores ACE</span><span class="sxs-lookup"><span data-stu-id="14683-165">ACE flags string</span></span> | <span data-ttu-id="14683-166">Constante em SDDL. h</span><span class="sxs-lookup"><span data-stu-id="14683-166">Constant in Sddl.h</span></span>       | <span data-ttu-id="14683-167">Valor de AceFlag</span><span class="sxs-lookup"><span data-stu-id="14683-167">AceFlag value</span></span>                 |
|------------------|--------------------------|-------------------------------|
| <span data-ttu-id="14683-168">CIS</span><span class="sxs-lookup"><span data-stu-id="14683-168">"CI"</span></span>             | <span data-ttu-id="14683-169">\_herança de contêiner SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-169">SDDL\_CONTAINER\_INHERIT</span></span> | <span data-ttu-id="14683-170">\_Ace herdar contêiner \_</span><span class="sxs-lookup"><span data-stu-id="14683-170">CONTAINER\_INHERIT\_ACE</span></span>       |
| <span data-ttu-id="14683-171">Oi</span><span class="sxs-lookup"><span data-stu-id="14683-171">"OI"</span></span>             | <span data-ttu-id="14683-172">\_herança de objeto SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-172">SDDL\_OBJECT\_INHERIT</span></span>    | <span data-ttu-id="14683-173">\_ACE de herança de objeto \_</span><span class="sxs-lookup"><span data-stu-id="14683-173">OBJECT\_INHERIT\_ACE</span></span>          |
| <span data-ttu-id="14683-174">NP</span><span class="sxs-lookup"><span data-stu-id="14683-174">"NP"</span></span>             | <span data-ttu-id="14683-175">SDDL \_ sem \_ propagação</span><span class="sxs-lookup"><span data-stu-id="14683-175">SDDL\_NO\_PROPAGATE</span></span>      | <span data-ttu-id="14683-176">NENHUMA \_ ACE de \_ herança de propagação \_</span><span class="sxs-lookup"><span data-stu-id="14683-176">NO\_PROPAGATE\_INHERIT\_ACE</span></span>   |
| <span data-ttu-id="14683-177">I</span><span class="sxs-lookup"><span data-stu-id="14683-177">"IO"</span></span>             | <span data-ttu-id="14683-178">herança de SDDL \_ \_ somente</span><span class="sxs-lookup"><span data-stu-id="14683-178">SDDL\_INHERIT\_ONLY</span></span>      | <span data-ttu-id="14683-179">HERDAr \_ somente \_ Ace</span><span class="sxs-lookup"><span data-stu-id="14683-179">INHERIT\_ONLY\_ACE</span></span>            |
| <span data-ttu-id="14683-180">“ID”</span><span class="sxs-lookup"><span data-stu-id="14683-180">"ID"</span></span>             | <span data-ttu-id="14683-181">SDDL \_ herdada</span><span class="sxs-lookup"><span data-stu-id="14683-181">SDDL\_INHERITED</span></span>          | <span data-ttu-id="14683-182">Ace HERDAdo \_</span><span class="sxs-lookup"><span data-stu-id="14683-182">INHERITED\_ACE</span></span>                |
| <span data-ttu-id="14683-183">ADMINISTRADOR</span><span class="sxs-lookup"><span data-stu-id="14683-183">"SA"</span></span>             | <span data-ttu-id="14683-184">\_êxito na auditoria de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-184">SDDL\_AUDIT\_SUCCESS</span></span>     | <span data-ttu-id="14683-185">\_sinalizador de \_ ACE de acesso bem-sucedido \_</span><span class="sxs-lookup"><span data-stu-id="14683-185">SUCCESSFUL\_ACCESS\_ACE\_FLAG</span></span> |
| <span data-ttu-id="14683-186">ATIVO</span><span class="sxs-lookup"><span data-stu-id="14683-186">"FA"</span></span>             | <span data-ttu-id="14683-187">\_falha de auditoria de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-187">SDDL\_AUDIT\_FAILURE</span></span>     | <span data-ttu-id="14683-188">\_sinalizador de \_ ACE de acesso com falha \_</span><span class="sxs-lookup"><span data-stu-id="14683-188">FAILED\_ACCESS\_ACE\_FLAG</span></span>     |



 

</dd> <dt>

<span data-ttu-id="14683-189"><span id="rights"></span><span id="RIGHTS"></span>**privilégios**</span><span class="sxs-lookup"><span data-stu-id="14683-189"><span id="rights"></span><span id="RIGHTS"></span>**rights**</span></span>
</dt> <dd>

<span data-ttu-id="14683-190">Uma cadeia de caracteres que indica os [direitos de acesso](access-rights-and-access-masks.md) controlados pela Ace.</span><span class="sxs-lookup"><span data-stu-id="14683-190">A string that indicates the [access rights](access-rights-and-access-masks.md) controlled by the ACE.</span></span> <span data-ttu-id="14683-191">Essa cadeia de caracteres pode ser uma representação de cadeia de caracteres hexadecimal dos direitos de acesso, como "0x7800003F", ou pode ser uma concatenação das cadeias de caracteres a seguir.</span><span class="sxs-lookup"><span data-stu-id="14683-191">This string can be a hexadecimal string representation of the access rights, such as "0x7800003F", or it can be a concatenation of the following strings.</span></span>



### <a name="generic-access-rights"></a><span data-ttu-id="14683-192">Direitos de acesso genéricos</span><span class="sxs-lookup"><span data-stu-id="14683-192">Generic access rights</span></span>

| <span data-ttu-id="14683-193">Cadeia de direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="14683-193">Access rights string</span></span> | <span data-ttu-id="14683-194">Constante em SDDL. h</span><span class="sxs-lookup"><span data-stu-id="14683-194">Constant in Sddl.h</span></span> | <span data-ttu-id="14683-195">Valor direito de acesso</span><span class="sxs-lookup"><span data-stu-id="14683-195">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="14683-196">3º</span><span class="sxs-lookup"><span data-stu-id="14683-196">"GA"</span></span>                 | <span data-ttu-id="14683-197">\_ \_ todos os genéricos SDDL</span><span class="sxs-lookup"><span data-stu-id="14683-197">SDDL\_GENERIC\_ALL</span></span> | <span data-ttu-id="14683-198">\_tudo genérico</span><span class="sxs-lookup"><span data-stu-id="14683-198">GENERIC\_ALL</span></span>       |
| <span data-ttu-id="14683-199">GR</span><span class="sxs-lookup"><span data-stu-id="14683-199">"GR"</span></span>                 | <span data-ttu-id="14683-200">\_leitura genérica de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-200">SDDL\_GENERIC\_READ</span></span> | <span data-ttu-id="14683-201">\_leitura genérica</span><span class="sxs-lookup"><span data-stu-id="14683-201">GENERIC\_READ</span></span>     |
| <span data-ttu-id="14683-202">GW</span><span class="sxs-lookup"><span data-stu-id="14683-202">"GW"</span></span>                 | <span data-ttu-id="14683-203">\_gravação genérica \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="14683-203">SDDL\_GENERIC\_WRITE</span></span> | <span data-ttu-id="14683-204">\_gravação genérica</span><span class="sxs-lookup"><span data-stu-id="14683-204">GENERIC\_WRITE</span></span> |
| <span data-ttu-id="14683-205">GX</span><span class="sxs-lookup"><span data-stu-id="14683-205">"GX"</span></span>                 | <span data-ttu-id="14683-206">\_execução genérica de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-206">SDDL\_GENERIC\_EXECUTE</span></span> | <span data-ttu-id="14683-207">\_execução genérica</span><span class="sxs-lookup"><span data-stu-id="14683-207">GENERIC\_EXECUTE</span></span> |


### <a name="standard-access-rights"></a><span data-ttu-id="14683-208">Direitos de acesso padrão</span><span class="sxs-lookup"><span data-stu-id="14683-208">Standard access rights</span></span>

| <span data-ttu-id="14683-209">Cadeia de direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="14683-209">Access rights string</span></span> | <span data-ttu-id="14683-210">Constante em SDDL. h</span><span class="sxs-lookup"><span data-stu-id="14683-210">Constant in Sddl.h</span></span> | <span data-ttu-id="14683-211">Valor direito de acesso</span><span class="sxs-lookup"><span data-stu-id="14683-211">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="14683-212">RC</span><span class="sxs-lookup"><span data-stu-id="14683-212">"RC"</span></span>                 | <span data-ttu-id="14683-213">\_controle de leitura de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-213">SDDL\_READ\_CONTROL</span></span> | <span data-ttu-id="14683-214">controle de leitura \_</span><span class="sxs-lookup"><span data-stu-id="14683-214">READ\_CONTROL</span></span>      |
| <span data-ttu-id="14683-215">SD</span><span class="sxs-lookup"><span data-stu-id="14683-215">"SD"</span></span>                 | <span data-ttu-id="14683-216">\_exclusão padrão de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-216">SDDL\_STANDARD\_DELETE</span></span> | <span data-ttu-id="14683-217">Delete (excluir)</span><span class="sxs-lookup"><span data-stu-id="14683-217">DELETE</span></span>          |
| <span data-ttu-id="14683-218">WD</span><span class="sxs-lookup"><span data-stu-id="14683-218">"WD"</span></span>                 | <span data-ttu-id="14683-219">\_DAC de gravação de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-219">SDDL\_WRITE\_DAC</span></span> | <span data-ttu-id="14683-220">GRAVAR \_ DAC</span><span class="sxs-lookup"><span data-stu-id="14683-220">WRITE\_DAC</span></span>            |
| <span data-ttu-id="14683-221">OIS</span><span class="sxs-lookup"><span data-stu-id="14683-221">"WO"</span></span>                 | <span data-ttu-id="14683-222">\_proprietário da gravação SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-222">SDDL\_WRITE\_OWNER</span></span> | <span data-ttu-id="14683-223">proprietário da gravação \_</span><span class="sxs-lookup"><span data-stu-id="14683-223">WRITE\_OWNER</span></span>        |

### <a name="directory-service-object-access-rights"></a><span data-ttu-id="14683-224">Direitos de acesso a objeto de serviço de diretório</span><span class="sxs-lookup"><span data-stu-id="14683-224">Directory service object access rights</span></span>

| <span data-ttu-id="14683-225">Cadeia de direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="14683-225">Access rights string</span></span> | <span data-ttu-id="14683-226">Constante em SDDL. h</span><span class="sxs-lookup"><span data-stu-id="14683-226">Constant in Sddl.h</span></span> | <span data-ttu-id="14683-227">Valor direito de acesso</span><span class="sxs-lookup"><span data-stu-id="14683-227">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="14683-228">RP</span><span class="sxs-lookup"><span data-stu-id="14683-228">"RP"</span></span>                 | <span data-ttu-id="14683-229">\_propriedade de leitura de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-229">SDDL\_READ\_PROPERTY</span></span> | <span data-ttu-id="14683-230">ADS \_ direito \_ de \_ leitura de DS \_ de AD</span><span class="sxs-lookup"><span data-stu-id="14683-230">ADS\_RIGHT\_DS\_READ\_PROP</span></span> |
| <span data-ttu-id="14683-231">PROCESSADOR</span><span class="sxs-lookup"><span data-stu-id="14683-231">"WP"</span></span>                 | <span data-ttu-id="14683-232">\_propriedade de gravação SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-232">SDDL\_WRITE\_PROPERTY</span></span> | <span data-ttu-id="14683-233">publicidade \_ de \_ gravação DS do \_ ad \_</span><span class="sxs-lookup"><span data-stu-id="14683-233">ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="14683-234">CC</span><span class="sxs-lookup"><span data-stu-id="14683-234">"CC"</span></span>                 | <span data-ttu-id="14683-235">\_criar \_ filho de SDDL</span><span class="sxs-lookup"><span data-stu-id="14683-235">SDDL\_CREATE\_CHILD</span></span> | <span data-ttu-id="14683-236">\_direito de \_ criação de DS do AD do ADS \_ \_</span><span class="sxs-lookup"><span data-stu-id="14683-236">ADS\_RIGHT\_DS\_CREATE\_CHILD</span></span> |
| <span data-ttu-id="14683-237">ORIGEM</span><span class="sxs-lookup"><span data-stu-id="14683-237">"DC"</span></span>                 | <span data-ttu-id="14683-238">\_excluir \_ filho de SDDL</span><span class="sxs-lookup"><span data-stu-id="14683-238">SDDL\_DELETE\_CHILD</span></span> | <span data-ttu-id="14683-239">\_direito de \_ exclusão de DS do AD do ADS \_ \_</span><span class="sxs-lookup"><span data-stu-id="14683-239">ADS\_RIGHT\_DS\_DELETE\_CHILD</span></span> |
| <span data-ttu-id="14683-240">LCs</span><span class="sxs-lookup"><span data-stu-id="14683-240">"LC"</span></span>                 | <span data-ttu-id="14683-241">\_lista de \_ filhos de SDDL</span><span class="sxs-lookup"><span data-stu-id="14683-241">SDDL\_LIST\_CHILDREN</span></span> | <span data-ttu-id="14683-242">lista de anúncios \_ à direita \_ ACTRL \_ DS \_</span><span class="sxs-lookup"><span data-stu-id="14683-242">ADS\_RIGHT\_ACTRL\_DS\_LIST</span></span> |
| <span data-ttu-id="14683-243">CM</span><span class="sxs-lookup"><span data-stu-id="14683-243">"SW"</span></span>                 | <span data-ttu-id="14683-244">\_auto- \_ gravação de SDDL</span><span class="sxs-lookup"><span data-stu-id="14683-244">SDDL\_SELF\_WRITE</span></span>    | <span data-ttu-id="14683-245">ANÚNCIOS \_ do lado direito do \_ ad \_</span><span class="sxs-lookup"><span data-stu-id="14683-245">ADS\_RIGHT\_DS\_SELF</span></span> |
| <span data-ttu-id="14683-246">LO</span><span class="sxs-lookup"><span data-stu-id="14683-246">"LO"</span></span>                  | <span data-ttu-id="14683-247">\_objeto da lista SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-247">SDDL\_LIST\_OBJECT</span></span> | <span data-ttu-id="14683-248">\_objeto de \_ lista de DS direito do ADS \_ \_</span><span class="sxs-lookup"><span data-stu-id="14683-248">ADS\_RIGHT\_DS\_LIST\_OBJECT</span></span> |
| <span data-ttu-id="14683-249">DT</span><span class="sxs-lookup"><span data-stu-id="14683-249">"DT"</span></span>                 | <span data-ttu-id="14683-250">\_árvore de exclusão de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-250">SDDL\_DELETE\_TREE</span></span> | <span data-ttu-id="14683-251">\_árvore de \_ exclusão de DS do lado do ADS \_ \_</span><span class="sxs-lookup"><span data-stu-id="14683-251">ADS\_RIGHT\_DS\_DELETE\_TREE</span></span> |
| <span data-ttu-id="14683-252">CD</span><span class="sxs-lookup"><span data-stu-id="14683-252">"CR"</span></span>                  | <span data-ttu-id="14683-253">\_acesso de controle SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-253">SDDL\_CONTROL\_ACCESS</span></span> | <span data-ttu-id="14683-254">\_acesso ao \_ controle de DS direito do ADS \_ \_</span><span class="sxs-lookup"><span data-stu-id="14683-254">ADS\_RIGHT\_DS\_CONTROL\_ACCESS</span></span> |

### <a name="file-access-rights"></a><span data-ttu-id="14683-255">Direitos de acesso a arquivos</span><span class="sxs-lookup"><span data-stu-id="14683-255">File access rights</span></span>

| <span data-ttu-id="14683-256">Cadeia de direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="14683-256">Access rights string</span></span> | <span data-ttu-id="14683-257">Constante em SDDL. h</span><span class="sxs-lookup"><span data-stu-id="14683-257">Constant in Sddl.h</span></span> | <span data-ttu-id="14683-258">Valor direito de acesso</span><span class="sxs-lookup"><span data-stu-id="14683-258">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="14683-259">ATIVO</span><span class="sxs-lookup"><span data-stu-id="14683-259">"FA"</span></span>                 | <span data-ttu-id="14683-260">\_arquivo SDDL \_ All</span><span class="sxs-lookup"><span data-stu-id="14683-260">SDDL\_FILE\_ALL</span></span>    | <span data-ttu-id="14683-261">ARQUIVAr \_ todo o \_ acesso</span><span class="sxs-lookup"><span data-stu-id="14683-261">FILE\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="14683-262">FR</span><span class="sxs-lookup"><span data-stu-id="14683-262">"FR"</span></span>                 | <span data-ttu-id="14683-263">\_leitura de arquivo SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-263">SDDL\_FILE\_READ</span></span>   | <span data-ttu-id="14683-264">\_leitura genérica do arquivo \_</span><span class="sxs-lookup"><span data-stu-id="14683-264">FILE\_GENERIC\_READ</span></span> |
| <span data-ttu-id="14683-265">FW</span><span class="sxs-lookup"><span data-stu-id="14683-265">"FW"</span></span>                 | <span data-ttu-id="14683-266">\_gravação de arquivo SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-266">SDDL\_FILE\_WRITE</span></span>  | <span data-ttu-id="14683-267">\_gravação genérica de arquivo \_</span><span class="sxs-lookup"><span data-stu-id="14683-267">FILE\_GENERIC\_WRITE</span></span> |
| <span data-ttu-id="14683-268">EFEITO</span><span class="sxs-lookup"><span data-stu-id="14683-268">"FX"</span></span>                 | <span data-ttu-id="14683-269">\_execução de arquivo SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-269">SDDL\_FILE\_EXECUTE</span></span> | <span data-ttu-id="14683-270">\_execução genérica do arquivo \_</span><span class="sxs-lookup"><span data-stu-id="14683-270">FILE\_GENERIC\_EXECUTE</span></span> |


### <a name="registry-key-access-rights"></a><span data-ttu-id="14683-271">Direitos de acesso à chave do registro</span><span class="sxs-lookup"><span data-stu-id="14683-271">Registry key access rights</span></span>

| <span data-ttu-id="14683-272">Cadeia de direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="14683-272">Access rights string</span></span> | <span data-ttu-id="14683-273">Constante em SDDL. h</span><span class="sxs-lookup"><span data-stu-id="14683-273">Constant in Sddl.h</span></span> | <span data-ttu-id="14683-274">Valor direito de acesso</span><span class="sxs-lookup"><span data-stu-id="14683-274">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="14683-275">Ka</span><span class="sxs-lookup"><span data-stu-id="14683-275">"KA"</span></span>                 | <span data-ttu-id="14683-276">\_chave SDDL \_ All</span><span class="sxs-lookup"><span data-stu-id="14683-276">SDDL\_KEY\_ALL</span></span>     | <span data-ttu-id="14683-277">CHAVE de \_ todo o \_ acesso</span><span class="sxs-lookup"><span data-stu-id="14683-277">KEY\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="14683-278">Coreia</span><span class="sxs-lookup"><span data-stu-id="14683-278">"KR"</span></span>                 | <span data-ttu-id="14683-279">\_leitura de chave SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-279">SDDL\_KEY\_READ</span></span>    | <span data-ttu-id="14683-280">leitura de chave \_</span><span class="sxs-lookup"><span data-stu-id="14683-280">KEY\_READ</span></span>          |
| <span data-ttu-id="14683-281">KW</span><span class="sxs-lookup"><span data-stu-id="14683-281">"KW"</span></span>                 | <span data-ttu-id="14683-282">\_gravação de chave SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-282">SDDL\_KEY\_WRITE</span></span>   | <span data-ttu-id="14683-283">gravação de chave \_</span><span class="sxs-lookup"><span data-stu-id="14683-283">KEY\_WRITE</span></span>         |
| <span data-ttu-id="14683-284">"KX"</span><span class="sxs-lookup"><span data-stu-id="14683-284">"KX"</span></span>                 | <span data-ttu-id="14683-285">\_execução da chave SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-285">SDDL\_KEY\_EXECUTE</span></span> | <span data-ttu-id="14683-286">\_executar chave</span><span class="sxs-lookup"><span data-stu-id="14683-286">KEY\_EXECUTE</span></span>       |

### <a name="mandatory-label-rights"></a><span data-ttu-id="14683-287">Direitos de rótulo obrigatórios</span><span class="sxs-lookup"><span data-stu-id="14683-287">Mandatory label rights</span></span>

| <span data-ttu-id="14683-288">Cadeia de direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="14683-288">Access rights string</span></span> | <span data-ttu-id="14683-289">Constante em SDDL. h</span><span class="sxs-lookup"><span data-stu-id="14683-289">Constant in Sddl.h</span></span> | <span data-ttu-id="14683-290">Valor direito de acesso</span><span class="sxs-lookup"><span data-stu-id="14683-290">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="14683-291">NR</span><span class="sxs-lookup"><span data-stu-id="14683-291">"NR"</span></span>                 | <span data-ttu-id="14683-292">SDDL \_ não \_ lido \_</span><span class="sxs-lookup"><span data-stu-id="14683-292">SDDL\_NO\_READ\_UP</span></span> | <span data-ttu-id="14683-293">\_rótulo obrigatório do sistema \_ \_ sem \_ leitura \_</span><span class="sxs-lookup"><span data-stu-id="14683-293">SYSTEM\_MANDATORY\_LABEL\_NO\_READ\_UP</span></span> |
| <span data-ttu-id="14683-294">NW</span><span class="sxs-lookup"><span data-stu-id="14683-294">"NW"</span></span>                 | <span data-ttu-id="14683-295">SDDL \_ sem \_ gravação \_</span><span class="sxs-lookup"><span data-stu-id="14683-295">SDDL\_NO\_WRITE\_UP</span></span> | <span data-ttu-id="14683-296">\_rótulo obrigatório do sistema \_ \_ sem \_ gravação \_</span><span class="sxs-lookup"><span data-stu-id="14683-296">SYSTEM\_MANDATORY\_LABEL\_NO\_WRITE\_UP</span></span> |
| <span data-ttu-id="14683-297">NX</span><span class="sxs-lookup"><span data-stu-id="14683-297">"NX"</span></span>                 | <span data-ttu-id="14683-298">SDDL \_ não \_ executar \_</span><span class="sxs-lookup"><span data-stu-id="14683-298">SDDL\_NO\_EXECUTE\_UP</span></span> | <span data-ttu-id="14683-299">\_rótulo obrigatório do sistema \_ \_ não \_ executar \_</span><span class="sxs-lookup"><span data-stu-id="14683-299">SYSTEM\_MANDATORY\_LABEL\_NO\_EXECUTE\_UP</span></span> |
</dd> <dt>

<span data-ttu-id="14683-300"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**GUID do objeto \_**</span><span class="sxs-lookup"><span data-stu-id="14683-300"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="14683-301">Uma representação de cadeia de caracteres de um GUID que indica o valor do membro **objecttype** de uma estrutura ACE específica de objeto, [**como \_ \_ \_ ACE de objeto permitido de acesso**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace).</span><span class="sxs-lookup"><span data-stu-id="14683-301">A string representation of a GUID that indicates the value of the **ObjectType** member of an object-specific ACE structure, such as [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace).</span></span> <span data-ttu-id="14683-302">A cadeia de caracteres GUID usa o formato retornado pela função [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .</span><span class="sxs-lookup"><span data-stu-id="14683-302">The GUID string uses the format returned by the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) function.</span></span>

<span data-ttu-id="14683-303">A tabela a seguir lista alguns GUIDs de objeto usados com frequência.</span><span class="sxs-lookup"><span data-stu-id="14683-303">The following table lists some commonly used object GUIDs.</span></span>



| <span data-ttu-id="14683-304">Direitos e GUID</span><span class="sxs-lookup"><span data-stu-id="14683-304">Rights and GUID</span></span>                         | <span data-ttu-id="14683-305">Permissão</span><span class="sxs-lookup"><span data-stu-id="14683-305">Permission</span></span>      |
|-----------------------------------------|-----------------|
| <span data-ttu-id="14683-306">CR; ab721a53-1e2f-11D0-9819-00aa0040529b</span><span class="sxs-lookup"><span data-stu-id="14683-306">CR;ab721a53-1e2f-11d0-9819-00aa0040529b</span></span> | <span data-ttu-id="14683-307">Alterar senha</span><span class="sxs-lookup"><span data-stu-id="14683-307">Change password</span></span> |
| <span data-ttu-id="14683-308">CR; 00299570-246d-11D0-A768-00aa006e0529</span><span class="sxs-lookup"><span data-stu-id="14683-308">CR;00299570-246d-11d0-a768-00aa006e0529</span></span> | <span data-ttu-id="14683-309">Redefinir senha</span><span class="sxs-lookup"><span data-stu-id="14683-309">Reset password</span></span>  |



 

</dd> <dt>

<span data-ttu-id="14683-310"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**herdar \_ GUID do objeto \_**</span><span class="sxs-lookup"><span data-stu-id="14683-310"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**inherit\_object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="14683-311">Uma representação de cadeia de caracteres de um GUID que indica o valor do membro **InheritedObjectType** de uma estrutura ACE específica de objeto.</span><span class="sxs-lookup"><span data-stu-id="14683-311">A string representation of a GUID that indicates the value of the **InheritedObjectType** member of an object-specific ACE structure.</span></span> <span data-ttu-id="14683-312">A cadeia de caracteres GUID usa o formato [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .</span><span class="sxs-lookup"><span data-stu-id="14683-312">The GUID string uses the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) format.</span></span>

</dd> <dt>

<span data-ttu-id="14683-313"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**Sid da conta \_**</span><span class="sxs-lookup"><span data-stu-id="14683-313"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**account\_sid**</span></span>
</dt> <dd>

<span data-ttu-id="14683-314">[Cadeia de caracteres de Sid](sid-strings.md) que identifica o [confiável](trustees.md) da Ace.</span><span class="sxs-lookup"><span data-stu-id="14683-314">[SID string](sid-strings.md) that identifies the [trustee](trustees.md) of the ACE.</span></span>

</dd> <dt>

<span data-ttu-id="14683-315"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**atributo de recurso \_**</span><span class="sxs-lookup"><span data-stu-id="14683-315"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**resource\_attribute**</span></span>
</dt> <dd>

<span data-ttu-id="14683-316">\[OPCIONAL \] o atributo de recurso \_ é apenas para ACEs de recurso e é opcional.</span><span class="sxs-lookup"><span data-stu-id="14683-316">\[OPTIONAL\] The resource\_attribute is only for resource ACEs and is optional.</span></span> <span data-ttu-id="14683-317">Uma cadeia de caracteres que indica o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="14683-317">A string that indicates the data type.</span></span> <span data-ttu-id="14683-318">O tipo de dados Ace do atributo de recurso pode ser um dos seguintes tipos de dados definidos em SDDL. h.</span><span class="sxs-lookup"><span data-stu-id="14683-318">The resource attribute ace data type can be one of the following data types defined in Sddl.h.</span></span>

<span data-ttu-id="14683-319">O \# sinal "" é sinônimo de "0" em atributos de recurso.</span><span class="sxs-lookup"><span data-stu-id="14683-319">The "\#" sign is synonymous with "0" in resource attributes.</span></span> <span data-ttu-id="14683-320">Por exemplo, D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) é equivalente a e interpretado como D:ai (XA; OICI; FA;;; WD; (OctetStringType = = \# 01020300)).</span><span class="sxs-lookup"><span data-stu-id="14683-320">For example, D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#1\#2\#3\#\#)) is equivalent to and interpreted as D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#01020300)).</span></span>

<span data-ttu-id="14683-321">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista e Windows Server 2003:** Os atributos de recurso não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="14683-321">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Resource attributes are not available.</span></span>



| <span data-ttu-id="14683-322">Cadeia de caracteres de tipo de dados ACE de atributo de recurso</span><span class="sxs-lookup"><span data-stu-id="14683-322">Resource attribute ace data type string</span></span> | <span data-ttu-id="14683-323">Constante em SDDL. h</span><span class="sxs-lookup"><span data-stu-id="14683-323">Constant in Sddl.h</span></span> | <span data-ttu-id="14683-324">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="14683-324">Data type</span></span>        |
|-----------------------------------------|--------------------|------------------|
| <span data-ttu-id="14683-325">It</span><span class="sxs-lookup"><span data-stu-id="14683-325">"TI"</span></span>                                    | <span data-ttu-id="14683-326">SDDL \_ int</span><span class="sxs-lookup"><span data-stu-id="14683-326">SDDL\_INT</span></span>          | <span data-ttu-id="14683-327">Inteiro assinado</span><span class="sxs-lookup"><span data-stu-id="14683-327">Signed integer</span></span>   |
| <span data-ttu-id="14683-328">Tu</span><span class="sxs-lookup"><span data-stu-id="14683-328">"TU"</span></span>                                    | <span data-ttu-id="14683-329">SDDL \_ uint</span><span class="sxs-lookup"><span data-stu-id="14683-329">SDDL\_UINT</span></span>         | <span data-ttu-id="14683-330">Inteiro não assinado</span><span class="sxs-lookup"><span data-stu-id="14683-330">Unsigned integer</span></span> |
| <span data-ttu-id="14683-331">CALs</span><span class="sxs-lookup"><span data-stu-id="14683-331">"TS"</span></span>                                    | <span data-ttu-id="14683-332">\_WSTRING SDDL</span><span class="sxs-lookup"><span data-stu-id="14683-332">SDDL\_WSTRING</span></span>      | <span data-ttu-id="14683-333">Cadeia de caracteres larga</span><span class="sxs-lookup"><span data-stu-id="14683-333">Wide string</span></span>      |
| <span data-ttu-id="14683-334">TD</span><span class="sxs-lookup"><span data-stu-id="14683-334">"TD"</span></span>                                    | <span data-ttu-id="14683-335">\_SID SDDL</span><span class="sxs-lookup"><span data-stu-id="14683-335">SDDL\_SID</span></span>          | <span data-ttu-id="14683-336">SID</span><span class="sxs-lookup"><span data-stu-id="14683-336">SID</span></span>              |
| <span data-ttu-id="14683-337">TX</span><span class="sxs-lookup"><span data-stu-id="14683-337">"TX"</span></span>                                    | <span data-ttu-id="14683-338">BLOB de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="14683-338">SDDL\_BLOB</span></span>         | <span data-ttu-id="14683-339">Cadeia de caracteres de octeto</span><span class="sxs-lookup"><span data-stu-id="14683-339">Octet string</span></span>     |
| <span data-ttu-id="14683-340">TB</span><span class="sxs-lookup"><span data-stu-id="14683-340">"TB"</span></span>                                    | <span data-ttu-id="14683-341">\_booliano SDDL</span><span class="sxs-lookup"><span data-stu-id="14683-341">SDDL\_BOOLEAN</span></span>      | <span data-ttu-id="14683-342">Boolean</span><span class="sxs-lookup"><span data-stu-id="14683-342">Boolean</span></span>          |



 

</dd> </dl>

<span data-ttu-id="14683-343">O exemplo a seguir mostra uma cadeia de caracteres ACE para uma ACE permitida pelo Access.</span><span class="sxs-lookup"><span data-stu-id="14683-343">The following example shows an ACE string for an access-allowed ACE.</span></span> <span data-ttu-id="14683-344">Ele não é uma ACE específica do objeto, portanto, não tem informações nos campos **\_ GUID do objeto** e **herdar \_ \_ GUID do objeto** .</span><span class="sxs-lookup"><span data-stu-id="14683-344">It is not an object-specific ACE, so it has no information in the **object\_guid** and **inherit\_object\_guid** fields.</span></span> <span data-ttu-id="14683-345">O campo de **\_ sinalizadores de Ace** também está vazio, o que indica que nenhum dos sinalizadores de Ace está definido.</span><span class="sxs-lookup"><span data-stu-id="14683-345">The **ace\_flags** field is also empty, which indicates that none of the ACE flags are set.</span></span>


```C++
(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-1-0)
```



<span data-ttu-id="14683-346">A cadeia de caracteres ACE mostrada acima descreve as informações de ACE a seguir.</span><span class="sxs-lookup"><span data-stu-id="14683-346">The ACE string shown above describes the following ACE information.</span></span>


```C++
AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
AceFlags:      0x00
Access Mask:   0x100e003f
                    READ_CONTROL
                    WRITE_DAC
                    WRITE_OWNER
                    GENERIC_ALL
                    Other access rights(0x0000003f)
Ace Sid      : (S-1-1-0)
```



<span data-ttu-id="14683-347">O exemplo a seguir mostra um arquivo classificado com declarações de recurso para Windows e linguagem SQL (SQL) com PFS definido como alto impacto comercial.</span><span class="sxs-lookup"><span data-stu-id="14683-347">The following example shows a file classified with resource claims for Windows and Structured Query Language (SQL) with Secrecy set to High Business Impact.</span></span>


```C++
(RA;CI;;;;S-1-1-0; ("Project",TS,0,"Windows","SQL")) 
(RA;CI;;;;S-1-1-0; ("Secrecy",TU,0,3))
```



<span data-ttu-id="14683-348">A cadeia de caracteres ACE mostrada acima descreve as informações de ACE a seguir.</span><span class="sxs-lookup"><span data-stu-id="14683-348">The ACE string shown above describes the following ACE information.</span></span>


```C++
AceType:       0x12 (SYSTEM_RESOURCE_ATTRIBUTE_ACE_TYPE)
AceFlags:      0x1  (SDDL_CONTAINER_INHERIT)
Access Mask:   0x0
Ace Sid      : (S-1-1-0)
Resource Attributes: Project has the strings Windows and SQL, Secrecy has the unsigned int value of 3
```



<span data-ttu-id="14683-349">Para obter mais informações, consulte [Security Descriptor String Format](security-descriptor-string-format.md) e [Sid Strings](sid-strings.md).</span><span class="sxs-lookup"><span data-stu-id="14683-349">For more information, see [Security Descriptor String Format](security-descriptor-string-format.md) and [SID Strings](sid-strings.md).</span></span> <span data-ttu-id="14683-350">Para ACEs condicionais, consulte [linguagem de definição do descritor de segurança para aces condicionais](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="14683-350">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="14683-351">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="14683-351">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="14683-352">[\[MS-DTYP \] : linguagem de descrição do descritor de segurança](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="14683-352">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

