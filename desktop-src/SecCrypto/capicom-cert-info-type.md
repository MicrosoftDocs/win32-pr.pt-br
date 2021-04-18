---
description: Define quais informações serão consultadas a partir de um certificado.
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: Enumeração de CAPICOM_CERT_INFO_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERT_INFO_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8e38bb8940645bbefecb3822bce8de8c2e0eb902
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753100"
---
# <a name="capicom_cert_info_type-enumeration"></a><span data-ttu-id="e0719-103">\_Enumeração de \_ tipo de informações de certificado CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="e0719-103">CAPICOM\_CERT\_INFO\_TYPE enumeration</span></span>

<span data-ttu-id="e0719-104">O tipo de enumeração do **\_ tipo de \_ informações \_ do certificado capicor** define quais informações serão consultadas de um certificado.</span><span class="sxs-lookup"><span data-stu-id="e0719-104">The **CAPICOM\_CERT\_INFO\_TYPE** enumeration type defines what information is to be queried from a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="e0719-105">Membros</span><span class="sxs-lookup"><span data-stu-id="e0719-105">Members</span></span>



| <span data-ttu-id="e0719-106">Membro</span><span class="sxs-lookup"><span data-stu-id="e0719-106">Member</span></span>                                         | <span data-ttu-id="e0719-107">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="e0719-107">Description</span></span>                                                                                  | <span data-ttu-id="e0719-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e0719-108">Value</span></span> |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="e0719-109">**informações de certificado capicor \_ \_ \_ \_ nome simples da entidade \_**</span><span class="sxs-lookup"><span data-stu-id="e0719-109">**CAPICOM\_CERT\_INFO\_SUBJECT\_SIMPLE\_NAME**</span></span> | <span data-ttu-id="e0719-110">Retorna o nome de exibição da entidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="e0719-110">Returns the display name of the certificate subject.</span></span><br/>                              | <span data-ttu-id="e0719-111">0</span><span class="sxs-lookup"><span data-stu-id="e0719-111">0</span></span>     |
| <span data-ttu-id="e0719-112">**\_ \_ \_ nome simples do emissor de informações de \_ certificado CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="e0719-112">**CAPICOM\_CERT\_INFO\_ISSUER\_SIMPLE\_NAME**</span></span>  | <span data-ttu-id="e0719-113">Retorna o nome de exibição do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="e0719-113">Returns the display name of the issuer of the certificate.</span></span><br/>                        | <span data-ttu-id="e0719-114">1</span><span class="sxs-lookup"><span data-stu-id="e0719-114">1</span></span>     |
| <span data-ttu-id="e0719-115">**CAPICOM \_ informações de certificado \_ nome de \_ email da entidade \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e0719-115">**CAPICOM\_CERT\_INFO\_SUBJECT\_EMAIL\_NAME**</span></span>  | <span data-ttu-id="e0719-116">Retorna o endereço de email da entidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="e0719-116">Returns the email address of the certificate subject.</span></span><br/>                             | <span data-ttu-id="e0719-117">2</span><span class="sxs-lookup"><span data-stu-id="e0719-117">2</span></span>     |
| <span data-ttu-id="e0719-118">**capicor \_ informações do certificado \_ nome do \_ email do emissor \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e0719-118">**CAPICOM\_CERT\_INFO\_ISSUER\_EMAIL\_NAME**</span></span>   | <span data-ttu-id="e0719-119">Retorna o endereço de email do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="e0719-119">Returns the email address of the issuer of the certificate.</span></span><br/>                       | <span data-ttu-id="e0719-120">3</span><span class="sxs-lookup"><span data-stu-id="e0719-120">3</span></span>     |
| <span data-ttu-id="e0719-121">**informações de certificado capicor \_ \_ \_ UPN da entidade \_**</span><span class="sxs-lookup"><span data-stu-id="e0719-121">**CAPICOM\_CERT\_INFO\_SUBJECT\_UPN**</span></span>          | <span data-ttu-id="e0719-122">Retorna o UPN da entidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="e0719-122">Returns the UPN of the certificate subject.</span></span> <span data-ttu-id="e0719-123">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e0719-123">Introduced in CAPICOM 2.0.</span></span><br/>            | <span data-ttu-id="e0719-124">4</span><span class="sxs-lookup"><span data-stu-id="e0719-124">4</span></span>     |
| <span data-ttu-id="e0719-125">**\_UPN do \_ emissor de informações de certificado CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e0719-125">**CAPICOM\_CERT\_INFO\_ISSUER\_UPN**</span></span>           | <span data-ttu-id="e0719-126">Retorna o UPN do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="e0719-126">Returns the UPN of the issuer of the certificate.</span></span> <span data-ttu-id="e0719-127">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e0719-127">Introduced in CAPICOM 2.0.</span></span><br/>      | <span data-ttu-id="e0719-128">5</span><span class="sxs-lookup"><span data-stu-id="e0719-128">5</span></span>     |
| <span data-ttu-id="e0719-129">**CAPICOM \_ informações do certificado \_ \_ \_ nome DNS da entidade \_**</span><span class="sxs-lookup"><span data-stu-id="e0719-129">**CAPICOM\_CERT\_INFO\_SUBJECT\_DNS\_NAME**</span></span>    | <span data-ttu-id="e0719-130">Retorna o nome DNS da entidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="e0719-130">Returns the DNS name of the certificate subject.</span></span> <span data-ttu-id="e0719-131">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e0719-131">Introduced in CAPICOM 2.0.</span></span><br/>       | <span data-ttu-id="e0719-132">6</span><span class="sxs-lookup"><span data-stu-id="e0719-132">6</span></span>     |
| <span data-ttu-id="e0719-133">**CAPICOM \_ informações do certificado \_ \_ \_ nome DNS do emissor \_**</span><span class="sxs-lookup"><span data-stu-id="e0719-133">**CAPICOM\_CERT\_INFO\_ISSUER\_DNS\_NAME**</span></span>     | <span data-ttu-id="e0719-134">Retorna o nome DNS do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="e0719-134">Returns the DNS name of the issuer of the certificate.</span></span> <span data-ttu-id="e0719-135">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e0719-135">Introduced in CAPICOM 2.0.</span></span><br/> | <span data-ttu-id="e0719-136">7</span><span class="sxs-lookup"><span data-stu-id="e0719-136">7</span></span>     |



## <a name="remarks"></a><span data-ttu-id="e0719-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0719-137">Remarks</span></span>

<span data-ttu-id="e0719-138">O tipo de enumeração de **\_ tipo de \_ informações \_ do certificado capicor** é usado pelo método [**Certificate. GetInfo**](certificate-getinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="e0719-138">The **CAPICOM\_CERT\_INFO\_TYPE** enumeration type is used by the [**Certificate.GetInfo**](certificate-getinfo.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0719-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0719-139">Requirements</span></span>



| <span data-ttu-id="e0719-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0719-140">Requirement</span></span> | <span data-ttu-id="e0719-141">Valor</span><span class="sxs-lookup"><span data-stu-id="e0719-141">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0719-142">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e0719-142">Redistributable</span></span><br/> | <span data-ttu-id="e0719-143">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e0719-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="e0719-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0719-144">Header</span></span><br/>          | <dl> <span data-ttu-id="e0719-145"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0719-145"><dt>Capicom.h</dt></span></span> </dl> |



 

 




