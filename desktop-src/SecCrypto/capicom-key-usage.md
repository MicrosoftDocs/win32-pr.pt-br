---
description: A enumeração uso da chave capicor \_ \_ define as maneiras em que uma chave pode ser usada. Introduzido no CAPICOM 2,0.
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: Enumeração de CAPICOM_KEY_USAGE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_USAGE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1d44c7f3ecf35ddeb55dd96e5513261691010990
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748459"
---
# <a name="capicom_key_usage-enumeration"></a><span data-ttu-id="858a9-104">Enumeração de uso de \_ chave CApicom \_</span><span class="sxs-lookup"><span data-stu-id="858a9-104">CAPICOM\_KEY\_USAGE enumeration</span></span>

<span data-ttu-id="858a9-105">A **enumeração \_ \_ uso da chave capicor** define as maneiras em que uma chave pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="858a9-105">The **CAPICOM\_KEY\_USAGE** enumeration defines the ways in which a key can be used.</span></span> <span data-ttu-id="858a9-106">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="858a9-106">Introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="858a9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="858a9-107">Members</span></span>



| <span data-ttu-id="858a9-108">Membro</span><span class="sxs-lookup"><span data-stu-id="858a9-108">Member</span></span>                                      | <span data-ttu-id="858a9-109">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="858a9-109">Description</span></span>                                                                                                                      | <span data-ttu-id="858a9-110">Valor</span><span class="sxs-lookup"><span data-stu-id="858a9-110">Value</span></span>      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| <span data-ttu-id="858a9-111">**\_uso de \_ chave de assinatura digital \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="858a9-111">**CAPICOM\_DIGITAL\_SIGNATURE\_KEY\_USAGE**</span></span> | <span data-ttu-id="858a9-112">A chave pode ser usada para criar uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="858a9-112">The key can be used to create a digital signature.</span></span><br/>                                                                    | <span data-ttu-id="858a9-113">0x00000080</span><span class="sxs-lookup"><span data-stu-id="858a9-113">0x00000080</span></span> |
| <span data-ttu-id="858a9-114">**\_uso da \_ chave de não repúdio \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="858a9-114">**CAPICOM\_NON\_REPUDIATION\_KEY\_USAGE**</span></span>   | <span data-ttu-id="858a9-115">A chave pode ser usada para não- [*repúdio*](../secgloss/n-gly.md).</span><span class="sxs-lookup"><span data-stu-id="858a9-115">The key can be used for [*nonrepudiation*](../secgloss/n-gly.md).</span></span><br/> | <span data-ttu-id="858a9-116">0x00000040</span><span class="sxs-lookup"><span data-stu-id="858a9-116">0x00000040</span></span> |
| <span data-ttu-id="858a9-117">**\_uso da \_ chave de codificação de chave CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="858a9-117">**CAPICOM\_KEY\_ENCIPHERMENT\_KEY\_USAGE**</span></span>  | <span data-ttu-id="858a9-118">A chave pode ser usada para criptografar uma chave.</span><span class="sxs-lookup"><span data-stu-id="858a9-118">The key can be used to encrypt a key.</span></span><br/>                                                                                 | <span data-ttu-id="858a9-119">0x00000020</span><span class="sxs-lookup"><span data-stu-id="858a9-119">0x00000020</span></span> |
| <span data-ttu-id="858a9-120">**\_uso da \_ chave de codificação de dados CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="858a9-120">**CAPICOM\_DATA\_ENCIPHERMENT\_KEY\_USAGE**</span></span> | <span data-ttu-id="858a9-121">A chave pode ser usada para criptografar dados.</span><span class="sxs-lookup"><span data-stu-id="858a9-121">The key can be used to encrypt data.</span></span><br/>                                                                                  | <span data-ttu-id="858a9-122">0x00000010</span><span class="sxs-lookup"><span data-stu-id="858a9-122">0x00000010</span></span> |
| <span data-ttu-id="858a9-123">**\_uso da \_ chave do contrato de chave CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="858a9-123">**CAPICOM\_KEY\_AGREEMENT\_KEY\_USAGE**</span></span>     | <span data-ttu-id="858a9-124">A chave pode ser usada para o contrato de chave.</span><span class="sxs-lookup"><span data-stu-id="858a9-124">The key can be used for key agreement.</span></span><br/>                                                                                | <span data-ttu-id="858a9-125">0x00000008</span><span class="sxs-lookup"><span data-stu-id="858a9-125">0x00000008</span></span> |
| <span data-ttu-id="858a9-126">**\_uso da \_ chave de assinatura de certificado de chave CAPICOM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="858a9-126">**CAPICOM\_KEY\_CERT\_SIGN\_KEY\_USAGE**</span></span>    | <span data-ttu-id="858a9-127">A chave pode ser usada para a assinatura de certificado de chave.</span><span class="sxs-lookup"><span data-stu-id="858a9-127">The key can be used for key certificate signing.</span></span> <span data-ttu-id="858a9-128">Esse valor é equivalente ao \_ \_ \_ uso da chave de assinatura offline \_ do \_ CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="858a9-128">This value is equivalent to CAPICOM\_OFFLINE\_CRL\_SIGN\_KEY\_USAGE.</span></span><br/> | <span data-ttu-id="858a9-129">0x00000004</span><span class="sxs-lookup"><span data-stu-id="858a9-129">0x00000004</span></span> |
| <span data-ttu-id="858a9-130">**\_ \_ \_ uso da chave de \_ assinatura \_ de capico offline CRL**</span><span class="sxs-lookup"><span data-stu-id="858a9-130">**CAPICOM\_OFFLINE\_CRL\_SIGN\_KEY\_USAGE**</span></span> | <span data-ttu-id="858a9-131">A chave pode ser usada para a assinatura de certificado de chave.</span><span class="sxs-lookup"><span data-stu-id="858a9-131">The key can be used for key certificate signing.</span></span> <span data-ttu-id="858a9-132">Esse valor é equivalente ao uso de chave de certificado de chave de CAPICOM \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="858a9-132">This value is equivalent to CAPICOM\_KEY\_CERT\_SIGN\_KEY\_USAGE.</span></span><br/>    | <span data-ttu-id="858a9-133">0x00000002</span><span class="sxs-lookup"><span data-stu-id="858a9-133">0x00000002</span></span> |
| <span data-ttu-id="858a9-134">**\_uso da \_ chave de assinatura do \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="858a9-134">**CAPICOM\_CRL\_SIGN\_KEY\_USAGE**</span></span>          | <span data-ttu-id="858a9-135">A chave pode ser usada para assinatura.</span><span class="sxs-lookup"><span data-stu-id="858a9-135">The key can be used for signing.</span></span><br/>                                                                                      | <span data-ttu-id="858a9-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="858a9-136">0x00000002</span></span> |
| <span data-ttu-id="858a9-137">**somente criptografia de capicos de \_ \_ \_ uso de chave \_**</span><span class="sxs-lookup"><span data-stu-id="858a9-137">**CAPICOM\_ENCIPHER\_ONLY\_KEY\_USAGE**</span></span>     | <span data-ttu-id="858a9-138">A chave só pode ser usada para criptografar.</span><span class="sxs-lookup"><span data-stu-id="858a9-138">The key can only be used to encrypt.</span></span><br/>                                                                                  | <span data-ttu-id="858a9-139">0x00000001</span><span class="sxs-lookup"><span data-stu-id="858a9-139">0x00000001</span></span> |
| <span data-ttu-id="858a9-140">**CAPICOM o \_ \_ \_ uso da chave somente de codificação \_**</span><span class="sxs-lookup"><span data-stu-id="858a9-140">**CAPICOM\_DECIPHER\_ONLY\_KEY\_USAGE**</span></span>     | <span data-ttu-id="858a9-141">A chave só pode ser usada para descriptografar.</span><span class="sxs-lookup"><span data-stu-id="858a9-141">The key can only be used to decrypt.</span></span><br/>                                                                                  | <span data-ttu-id="858a9-142">0x00008000</span><span class="sxs-lookup"><span data-stu-id="858a9-142">0x00008000</span></span> |



## <a name="requirements"></a><span data-ttu-id="858a9-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="858a9-143">Requirements</span></span>



| <span data-ttu-id="858a9-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="858a9-144">Requirement</span></span> | <span data-ttu-id="858a9-145">Valor</span><span class="sxs-lookup"><span data-stu-id="858a9-145">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="858a9-146">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="858a9-146">Redistributable</span></span><br/> | <span data-ttu-id="858a9-147">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="858a9-147">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="858a9-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="858a9-148">Header</span></span><br/>          | <dl> <span data-ttu-id="858a9-149"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="858a9-149"><dt>Capicom.h</dt></span></span> </dl> |



 

 
