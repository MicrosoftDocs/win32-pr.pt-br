---
title: ms-DS-User-Encrypted-texto-Password-atributo permitido
description: Indica se Active Directory irá armazenar a senha no formato de criptografia reversível.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- ms-DS-User-Encrypted-text-password-esquema de atributo do AD permitido
- Esquema de AD do atributo ms-DS-UserEncryptedTextPasswordAllowed
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d99ae61566ceec94336fd58951214dfc3255d2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456133"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a><span data-ttu-id="3a220-105">ms-DS-User-Encrypted-texto-Password-atributo permitido</span><span class="sxs-lookup"><span data-stu-id="3a220-105">ms-DS-User-Encrypted-Text-Password-Allowed attribute</span></span>

<span data-ttu-id="3a220-106">Indica se Active Directory irá armazenar a senha no formato de criptografia reversível.</span><span class="sxs-lookup"><span data-stu-id="3a220-106">Indicates whether Active Directory will store the password in the reversible encryption format.</span></span> <span data-ttu-id="3a220-107">True se a senha for armazenada no formato de criptografia reversível; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="3a220-107">True if the password is stored in the reversible encryption format; otherwise, False.</span></span>

> [!Note]  
> <span data-ttu-id="3a220-108">Esse atributo não é usado pelo [Serviços AD LDS](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) e é incluído apenas para fins de integridade/paridade com userAccountControl.</span><span class="sxs-lookup"><span data-stu-id="3a220-108">This attribute is not used by [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) and is only included for completeness/parity with userAccountControl.</span></span> <span data-ttu-id="3a220-109">AD LDS não armazena senhas com criptografia reversível, independentemente do valor desse atributo em qualquer objeto ou política de segurança de computador pertencente à criptografia reversível no próprio computador.</span><span class="sxs-lookup"><span data-stu-id="3a220-109">AD LDS does not store passwords with reversible encryption, regardless of this attribute's value on any given object or the computer security policy pertaining to reversible encryption on the computer itself.</span></span>

 



| <span data-ttu-id="3a220-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="3a220-110">Entry</span></span> | <span data-ttu-id="3a220-111">Valor</span><span class="sxs-lookup"><span data-stu-id="3a220-111">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="3a220-112">CN</span><span class="sxs-lookup"><span data-stu-id="3a220-112">CN</span></span>                | <span data-ttu-id="3a220-113">ms-DS-User-Encrypted-texto-senha-permitido</span><span class="sxs-lookup"><span data-stu-id="3a220-113">ms-DS-User-Encrypted-Text-Password-Allowed</span></span> |
| <span data-ttu-id="3a220-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3a220-114">Ldap-Display-Name</span></span> | <span data-ttu-id="3a220-115">ms-DS-UserEncryptedTextPasswordAllowed</span><span class="sxs-lookup"><span data-stu-id="3a220-115">ms-DS-UserEncryptedTextPasswordAllowed</span></span>     |
| <span data-ttu-id="3a220-116">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3a220-116">Size</span></span>              | \-                                         |
| <span data-ttu-id="3a220-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="3a220-117">Update Privilege</span></span>  | \-                                         |
| <span data-ttu-id="3a220-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="3a220-118">Update Frequency</span></span>  | \-                                         |
| <span data-ttu-id="3a220-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3a220-119">Attribute-Id</span></span>      | <span data-ttu-id="3a220-120">1.2.840.113556.1.4.1856</span><span class="sxs-lookup"><span data-stu-id="3a220-120">1.2.840.113556.1.4.1856</span></span>                    |
| <span data-ttu-id="3a220-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3a220-121">System-Id-Guid</span></span>    | <span data-ttu-id="3a220-122">5a87c7f2-93c5-454c-a8c5-8cb09613292e</span><span class="sxs-lookup"><span data-stu-id="3a220-122">5a87c7f2-93c5-454c-a8c5-8cb09613292e</span></span>       |
| <span data-ttu-id="3a220-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a220-123">Syntax</span></span>            | [<span data-ttu-id="3a220-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3a220-124">**Boolean**</span></span>](s-boolean.md)               |



## <a name="implementations"></a><span data-ttu-id="3a220-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="3a220-125">Implementations</span></span>

-   [<span data-ttu-id="3a220-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3a220-126">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="3a220-127">ADAM</span><span class="sxs-lookup"><span data-stu-id="3a220-127">ADAM</span></span>



| <span data-ttu-id="3a220-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="3a220-128">Entry</span></span> | <span data-ttu-id="3a220-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3a220-129">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="3a220-130">ID do link</span><span class="sxs-lookup"><span data-stu-id="3a220-130">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="3a220-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3a220-131">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="3a220-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="3a220-132">System-Only</span></span>            | <span data-ttu-id="3a220-133">Falso</span><span class="sxs-lookup"><span data-stu-id="3a220-133">False</span></span>                                                             |
| <span data-ttu-id="3a220-134">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3a220-134">Is-Single-Valued</span></span>       | <span data-ttu-id="3a220-135">True</span><span class="sxs-lookup"><span data-stu-id="3a220-135">True</span></span>                                                              |
| <span data-ttu-id="3a220-136">É indexado</span><span class="sxs-lookup"><span data-stu-id="3a220-136">Is Indexed</span></span>             | <span data-ttu-id="3a220-137">Falso</span><span class="sxs-lookup"><span data-stu-id="3a220-137">False</span></span>                                                             |
| <span data-ttu-id="3a220-138">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3a220-138">In Global Catalog</span></span>      | <span data-ttu-id="3a220-139">Falso</span><span class="sxs-lookup"><span data-stu-id="3a220-139">False</span></span>                                                             |
| <span data-ttu-id="3a220-140">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3a220-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="3a220-141">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3a220-141">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="3a220-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3a220-142">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="3a220-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3a220-143">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="3a220-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3a220-144">Search-Flags</span></span>           | <span data-ttu-id="3a220-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3a220-145">0x00000000</span></span>                                                        |
| <span data-ttu-id="3a220-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3a220-146">System-Flags</span></span>           | <span data-ttu-id="3a220-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3a220-147">0x00000010</span></span>                                                        |
| <span data-ttu-id="3a220-148">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3a220-148">Classes used in</span></span>        | [<span data-ttu-id="3a220-149">**ms-DS-Vinculed-Object**</span><span class="sxs-lookup"><span data-stu-id="3a220-149">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3a220-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a220-150">Remarks</span></span>

<span data-ttu-id="3a220-151">No ADAM, esse atributo substitui o [**sinalizador \_ \_ permitido pela \_ \_ senha de \_ texto criptografado da UF do ADS**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) do atributo [**userAccountControl**](a-useraccountcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="3a220-151">In ADAM, this attribute replaces the [**ADS\_UF\_ENCRYPTED\_TEXT\_PASSWORD\_ALLOWED**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) flag of the [**userAccountControl**](a-useraccountcontrol.md) attribute.</span></span>

 

