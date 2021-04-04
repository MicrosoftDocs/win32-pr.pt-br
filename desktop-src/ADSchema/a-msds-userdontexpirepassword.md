---
title: atributo ms-DS-User-is-expire-Password
description: Indica se a senha da conta que este atributo referenciará expirará.
ms.assetid: bafbcb4a-ee45-4f88-8fb2-93840efd1289
ms.tgt_platform: multiple
keywords:
- ms-DS-User-out-expire-esquema de AD do atributo de senha
- atributo msDS-UserDontExpirePassword do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-User-Dont-Expire-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d5c0fa709f549a523d628433ee2b3aa626278e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086918"
---
# <a name="ms-ds-user-dont-expire-password-attribute"></a><span data-ttu-id="91252-105">atributo ms-DS-User-is-expire-Password</span><span class="sxs-lookup"><span data-stu-id="91252-105">ms-DS-User-Dont-Expire-Password attribute</span></span>

<span data-ttu-id="91252-106">Indica se a senha da conta que este atributo referenciará expirará.</span><span class="sxs-lookup"><span data-stu-id="91252-106">Indicates whether the password for the account this attribute references will expire.</span></span> <span data-ttu-id="91252-107">True se a senha não expirar; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="91252-107">True if the password will not expire; otherwise, False.</span></span>



| <span data-ttu-id="91252-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="91252-108">Entry</span></span> | <span data-ttu-id="91252-109">Valor</span><span class="sxs-lookup"><span data-stu-id="91252-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="91252-110">CN</span><span class="sxs-lookup"><span data-stu-id="91252-110">CN</span></span>                | <span data-ttu-id="91252-111">ms-DS-User-out-expire-Password</span><span class="sxs-lookup"><span data-stu-id="91252-111">ms-DS-User-Dont-Expire-Password</span></span>      |
| <span data-ttu-id="91252-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="91252-112">Ldap-Display-Name</span></span> | <span data-ttu-id="91252-113">msDS-UserDontExpirePassword</span><span class="sxs-lookup"><span data-stu-id="91252-113">msDS-UserDontExpirePassword</span></span>          |
| <span data-ttu-id="91252-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="91252-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="91252-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="91252-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="91252-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="91252-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="91252-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="91252-117">Attribute-Id</span></span>      | <span data-ttu-id="91252-118">1.2.840.113556.1.4.1855</span><span class="sxs-lookup"><span data-stu-id="91252-118">1.2.840.113556.1.4.1855</span></span>              |
| <span data-ttu-id="91252-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="91252-119">System-Id-Guid</span></span>    | <span data-ttu-id="91252-120">8788193a-2925-43d9-a221-bb7fff397675</span><span class="sxs-lookup"><span data-stu-id="91252-120">8788193a-2925-43d9-a221-bb7fff397675</span></span> |
| <span data-ttu-id="91252-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="91252-121">Syntax</span></span>            | [<span data-ttu-id="91252-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="91252-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="91252-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="91252-123">Implementations</span></span>

-   [<span data-ttu-id="91252-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="91252-124">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="91252-125">ADAM</span><span class="sxs-lookup"><span data-stu-id="91252-125">ADAM</span></span>



| <span data-ttu-id="91252-126">Entrada</span><span class="sxs-lookup"><span data-stu-id="91252-126">Entry</span></span> | <span data-ttu-id="91252-127">Valor</span><span class="sxs-lookup"><span data-stu-id="91252-127">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="91252-128">ID do link</span><span class="sxs-lookup"><span data-stu-id="91252-128">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="91252-129">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91252-129">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="91252-130">System-Only</span><span class="sxs-lookup"><span data-stu-id="91252-130">System-Only</span></span>            | <span data-ttu-id="91252-131">Falso</span><span class="sxs-lookup"><span data-stu-id="91252-131">False</span></span>                                                             |
| <span data-ttu-id="91252-132">É de valor único</span><span class="sxs-lookup"><span data-stu-id="91252-132">Is-Single-Valued</span></span>       | <span data-ttu-id="91252-133">True</span><span class="sxs-lookup"><span data-stu-id="91252-133">True</span></span>                                                              |
| <span data-ttu-id="91252-134">É indexado</span><span class="sxs-lookup"><span data-stu-id="91252-134">Is Indexed</span></span>             | <span data-ttu-id="91252-135">Falso</span><span class="sxs-lookup"><span data-stu-id="91252-135">False</span></span>                                                             |
| <span data-ttu-id="91252-136">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="91252-136">In Global Catalog</span></span>      | <span data-ttu-id="91252-137">Falso</span><span class="sxs-lookup"><span data-stu-id="91252-137">False</span></span>                                                             |
| <span data-ttu-id="91252-138">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="91252-138">NT-Security-Descriptor</span></span> | <span data-ttu-id="91252-139">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="91252-139">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="91252-140">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91252-140">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="91252-141">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91252-141">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="91252-142">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91252-142">Search-Flags</span></span>           | <span data-ttu-id="91252-143">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91252-143">0x00000000</span></span>                                                        |
| <span data-ttu-id="91252-144">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91252-144">System-Flags</span></span>           | <span data-ttu-id="91252-145">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91252-145">0x00000010</span></span>                                                        |
| <span data-ttu-id="91252-146">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="91252-146">Classes used in</span></span>        | [<span data-ttu-id="91252-147">**ms-DS-Vinculed-Object**</span><span class="sxs-lookup"><span data-stu-id="91252-147">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="91252-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="91252-148">Remarks</span></span>

<span data-ttu-id="91252-149">No ADAM, esse atributo substitui o sinalizador de passwd da UF do ADS que não [**\_ \_ \_ expira \_**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) o atributo [**userAccountControl**](a-useraccountcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="91252-149">In ADAM, this attribute replaces the [**ADS\_UF\_DONT\_EXPIRE\_PASSWD**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) flag of the [**userAccountControl**](a-useraccountcontrol.md) attribute.</span></span>

 

