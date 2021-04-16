---
description: Define os nomes de uso de chave estendidos com base em onde eles podem ser usados.
ms.assetid: 78f9f9cb-46e7-4f81-a16e-503750a0d743
title: Enumeração de CAPICOM_EKU (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EKU
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: e1d2f4f435fa31df00b87e20254aad57b690b047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757479"
---
# <a name="capicom_eku-enumeration"></a><span data-ttu-id="f360d-103">Enumeração EKU de CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="f360d-103">CAPICOM\_EKU enumeration</span></span>

<span data-ttu-id="f360d-104">O tipo de enumeração **\_ EKU capicor** define os nomes de uso de chave estendidos com base em onde eles podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="f360d-104">The **CAPICOM\_EKU** enumeration type defines the extended key usage names based on where they can be used.</span></span>

## <a name="members"></a><span data-ttu-id="f360d-105">Membros</span><span class="sxs-lookup"><span data-stu-id="f360d-105">Members</span></span>



| <span data-ttu-id="f360d-106">Membro</span><span class="sxs-lookup"><span data-stu-id="f360d-106">Member</span></span>                                     | <span data-ttu-id="f360d-107">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="f360d-107">Description</span></span>                                                                                                                                                 | <span data-ttu-id="f360d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f360d-108">Value</span></span> |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="f360d-109">**\_outro EKU de CApicom \_**</span><span class="sxs-lookup"><span data-stu-id="f360d-109">**CAPICOM\_EKU\_OTHER**</span></span>                    | <span data-ttu-id="f360d-110">O certificado tem usos definidos na política local.</span><span class="sxs-lookup"><span data-stu-id="f360d-110">Certificate has uses defined in local policy.</span></span> <span data-ttu-id="f360d-111">Isso será usado se o EKU necessário não for predefinido e o valor de OID precisar ser definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f360d-111">This is used if the EKU needed is not predefined and the OID value must be set by the application.</span></span><br/> | <span data-ttu-id="f360d-112">0</span><span class="sxs-lookup"><span data-stu-id="f360d-112">0</span></span>     |
| <span data-ttu-id="f360d-113">**\_autenticação de \_ servidor de EKU capicor \_**</span><span class="sxs-lookup"><span data-stu-id="f360d-113">**CAPICOM\_EKU\_SERVER\_AUTH**</span></span>             | <span data-ttu-id="f360d-114">O certificado pode ser usado para autenticar um servidor.</span><span class="sxs-lookup"><span data-stu-id="f360d-114">Certificate can be used to authenticate a server.</span></span><br/>                                                                                                | <span data-ttu-id="f360d-115">1</span><span class="sxs-lookup"><span data-stu-id="f360d-115">1</span></span>     |
| <span data-ttu-id="f360d-116">**\_autenticação de \_ cliente de EKU capicor \_**</span><span class="sxs-lookup"><span data-stu-id="f360d-116">**CAPICOM\_EKU\_CLIENT\_AUTH**</span></span>             | <span data-ttu-id="f360d-117">O certificado pode ser usado para autenticar um cliente.</span><span class="sxs-lookup"><span data-stu-id="f360d-117">Certificate can be used to authenticate a client.</span></span><br/>                                                                                                | <span data-ttu-id="f360d-118">2</span><span class="sxs-lookup"><span data-stu-id="f360d-118">2</span></span>     |
| <span data-ttu-id="f360d-119">**\_assinatura de \_ código de EKU CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="f360d-119">**CAPICOM\_EKU\_CODE\_SIGNING**</span></span>            | <span data-ttu-id="f360d-120">O certificado pode ser usado para criar uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="f360d-120">Certificate can be used to create a digital signature.</span></span><br/>                                                                                           | <span data-ttu-id="f360d-121">3</span><span class="sxs-lookup"><span data-stu-id="f360d-121">3</span></span>     |
| <span data-ttu-id="f360d-122">**\_proteção de \_ email de EKU CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="f360d-122">**CAPICOM\_EKU\_EMAIL\_PROTECTION**</span></span>        | <span data-ttu-id="f360d-123">O certificado pode ser usado para proteção de email.</span><span class="sxs-lookup"><span data-stu-id="f360d-123">Certificate can be used for email protection.</span></span><br/>                                                                                                    | <span data-ttu-id="f360d-124">4</span><span class="sxs-lookup"><span data-stu-id="f360d-124">4</span></span>     |
| <span data-ttu-id="f360d-125">**\_logon de \_ cartão inteligente \_ capicor EKU**</span><span class="sxs-lookup"><span data-stu-id="f360d-125">**CAPICOM\_EKU\_SMARTCARD\_LOGON**</span></span>         | <span data-ttu-id="f360d-126">O certificado pode ser usado para logon de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="f360d-126">Certificate can be used for smart card logon.</span></span> <span data-ttu-id="f360d-127">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="f360d-127">Introduced in CAPICOM 2.0.</span></span><br/>                                                                         | <span data-ttu-id="f360d-128">5</span><span class="sxs-lookup"><span data-stu-id="f360d-128">5</span></span>     |
| <span data-ttu-id="f360d-129">**\_sistema de \_ arquivos com criptografia EKU \_ de CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="f360d-129">**CAPICOM\_EKU\_ENCRYPTING\_FILE\_SYSTEM**</span></span> | <span data-ttu-id="f360d-130">O certificado pode ser usado para o EFS.</span><span class="sxs-lookup"><span data-stu-id="f360d-130">Certificate can be used for EFS.</span></span> <span data-ttu-id="f360d-131">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="f360d-131">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                      | <span data-ttu-id="f360d-132">6</span><span class="sxs-lookup"><span data-stu-id="f360d-132">6</span></span>     |



## <a name="remarks"></a><span data-ttu-id="f360d-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="f360d-133">Remarks</span></span>

<span data-ttu-id="f360d-134">O tipo de enumeração **\_ EKU capicor** é usado pelo [**EKU. Propriedade Name**](eku-name.md) .</span><span class="sxs-lookup"><span data-stu-id="f360d-134">The **CAPICOM\_EKU** enumeration type is used by the [**EKU.Name**](eku-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f360d-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f360d-135">Requirements</span></span>



| <span data-ttu-id="f360d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f360d-136">Requirement</span></span> | <span data-ttu-id="f360d-137">Valor</span><span class="sxs-lookup"><span data-stu-id="f360d-137">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f360d-138">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f360d-138">Redistributable</span></span><br/> | <span data-ttu-id="f360d-139">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="f360d-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="f360d-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f360d-140">Header</span></span><br/>          | <dl> <span data-ttu-id="f360d-141"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="f360d-141"><dt>Capicom.h</dt></span></span> </dl> |



 

 




