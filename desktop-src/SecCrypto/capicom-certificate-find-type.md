---
description: O tipo de enumeração do certificado CAPICOM de \_ \_ localizar \_ tipo define o tipo de critério de pesquisa usado para localizar certificados específicos. Esse tipo de enumeração foi introduzido no CAPICOM 2,0.
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: Enumeração de CAPICOM_CERTIFICATE_FIND_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_FIND_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: c5c867b230ba2045d97619d7f55e257bd7803b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755055"
---
# <a name="capicom_certificate_find_type-enumeration"></a><span data-ttu-id="729f7-104">\_Enumeração de \_ tipo de localização de certificado capicor \_</span><span class="sxs-lookup"><span data-stu-id="729f7-104">CAPICOM\_CERTIFICATE\_FIND\_TYPE enumeration</span></span>

<span data-ttu-id="729f7-105">O tipo de enumeração do **certificado CAPICOM de \_ \_ localizar \_ tipo** define o tipo de critério de pesquisa usado para localizar certificados específicos.</span><span class="sxs-lookup"><span data-stu-id="729f7-105">The **CAPICOM\_CERTIFICATE\_FIND\_TYPE** enumeration type defines the type of search criteria used to find specific certificates.</span></span> <span data-ttu-id="729f7-106">Esse tipo de enumeração foi introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="729f7-106">This enumeration type was introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="729f7-107">Membros</span><span class="sxs-lookup"><span data-stu-id="729f7-107">Members</span></span>



| <span data-ttu-id="729f7-108">Membro</span><span class="sxs-lookup"><span data-stu-id="729f7-108">Member</span></span>                                                | <span data-ttu-id="729f7-109">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="729f7-109">Description</span></span>                                                                                                                                 | <span data-ttu-id="729f7-110">Valor</span><span class="sxs-lookup"><span data-stu-id="729f7-110">Value</span></span> |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="729f7-111">**Certificado capicor \_ \_ localizar \_ \_ hash SHA1**</span><span class="sxs-lookup"><span data-stu-id="729f7-111">**CAPICOM\_CERTIFICATE\_FIND\_SHA1\_HASH**</span></span>            | <span data-ttu-id="729f7-112">Retorna certificados que correspondem a um hash SHA1 especificado.</span><span class="sxs-lookup"><span data-stu-id="729f7-112">Returns certificates matching a specified SHA1 hash.</span></span><br/>                                                                             | <span data-ttu-id="729f7-113">0</span><span class="sxs-lookup"><span data-stu-id="729f7-113">0</span></span>     |
| <span data-ttu-id="729f7-114">**certificado CAPICOM \_ \_ localizar \_ nome da entidade \_**</span><span class="sxs-lookup"><span data-stu-id="729f7-114">**CAPICOM\_CERTIFICATE\_FIND\_SUBJECT\_NAME**</span></span>         | <span data-ttu-id="729f7-115">Retorna certificados cujo nome da entidade corresponde exatamente ou parcialmente com um nome de entidade especificado.</span><span class="sxs-lookup"><span data-stu-id="729f7-115">Returns certificates whose subject name exactly or partially matches a specified subject name.</span></span><br/>                                   | <span data-ttu-id="729f7-116">1</span><span class="sxs-lookup"><span data-stu-id="729f7-116">1</span></span>     |
| <span data-ttu-id="729f7-117">**\_nome do \_ emissor da localização do certificado CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="729f7-117">**CAPICOM\_CERTIFICATE\_FIND\_ISSUER\_NAME**</span></span>          | <span data-ttu-id="729f7-118">Retorna certificados cujo nome do emissor corresponde exatamente ou parcialmente a um nome de emissor especificado.</span><span class="sxs-lookup"><span data-stu-id="729f7-118">Returns certificates whose issuer name exactly or partially matches a specified issuer name.</span></span><br/>                                     | <span data-ttu-id="729f7-119">2</span><span class="sxs-lookup"><span data-stu-id="729f7-119">2</span></span>     |
| <span data-ttu-id="729f7-120">**\_nome da \_ raiz de localização do certificado CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="729f7-120">**CAPICOM\_CERTIFICATE\_FIND\_ROOT\_NAME**</span></span>            | <span data-ttu-id="729f7-121">Retorna certificados cujo nome da entidade raiz corresponde exatamente ou parcialmente a um nome de entidade raiz especificado.</span><span class="sxs-lookup"><span data-stu-id="729f7-121">Returns certificates whose root subject name exactly or partially matches a specified root subject name.</span></span><br/>                         | <span data-ttu-id="729f7-122">3</span><span class="sxs-lookup"><span data-stu-id="729f7-122">3</span></span>     |
| <span data-ttu-id="729f7-123">**\_nome do \_ modelo de localização do certificado CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="729f7-123">**CAPICOM\_CERTIFICATE\_FIND\_TEMPLATE\_NAME**</span></span>        | <span data-ttu-id="729f7-124">Retorna certificados cujo nome de modelo corresponde a um nome de modelo especificado.</span><span class="sxs-lookup"><span data-stu-id="729f7-124">Returns certificates whose template name matches a specified template name.</span></span><br/>                                                      | <span data-ttu-id="729f7-125">4</span><span class="sxs-lookup"><span data-stu-id="729f7-125">4</span></span>     |
| <span data-ttu-id="729f7-126">**\_extensão de \_ localização de certificado CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="729f7-126">**CAPICOM\_CERTIFICATE\_FIND\_EXTENSION**</span></span>             | <span data-ttu-id="729f7-127">Retorna certificados que têm uma extensão que corresponde a uma extensão especificada.</span><span class="sxs-lookup"><span data-stu-id="729f7-127">Returns certificates that have an extension that matches a specified extension.</span></span><br/>                                                  | <span data-ttu-id="729f7-128">5</span><span class="sxs-lookup"><span data-stu-id="729f7-128">5</span></span>     |
| <span data-ttu-id="729f7-129">**certificado capicor \_ \_ localizar \_ propriedade estendida \_**</span><span class="sxs-lookup"><span data-stu-id="729f7-129">**CAPICOM\_CERTIFICATE\_FIND\_EXTENDED\_PROPERTY**</span></span>    | <span data-ttu-id="729f7-130">Retorna certificados que têm uma propriedade estendida cujo identificador de propriedade corresponde a um identificador de propriedade especificado.</span><span class="sxs-lookup"><span data-stu-id="729f7-130">Returns certificates that have an extended property whose property identifier matches a specified property identifier.</span></span><br/>           | <span data-ttu-id="729f7-131">6</span><span class="sxs-lookup"><span data-stu-id="729f7-131">6</span></span>     |
| <span data-ttu-id="729f7-132">**certificado CAPICOM ao \_ \_ localizar \_ política de aplicativo \_**</span><span class="sxs-lookup"><span data-stu-id="729f7-132">**CAPICOM\_CERTIFICATE\_FIND\_APPLICATION\_POLICY**</span></span>   | <span data-ttu-id="729f7-133">Retorna certificados no repositório que têm uma extensão ou propriedade de uso avançado de chave combinada com um identificador de uso.</span><span class="sxs-lookup"><span data-stu-id="729f7-133">Returns certificates in the store that have either an enhanced key usage extension or property combined with a usage identifier.</span></span><br/> | <span data-ttu-id="729f7-134">7</span><span class="sxs-lookup"><span data-stu-id="729f7-134">7</span></span>     |
| <span data-ttu-id="729f7-135">**\_política de \_ certificado de localização de certificado CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="729f7-135">**CAPICOM\_CERTIFICATE\_FIND\_CERTIFICATE\_POLICY**</span></span>   | <span data-ttu-id="729f7-136">Retorna certificados que contêm um OID de política especificado.</span><span class="sxs-lookup"><span data-stu-id="729f7-136">Returns certificates containing a specified policy OID.</span></span><br/>                                                                          | <span data-ttu-id="729f7-137">8</span><span class="sxs-lookup"><span data-stu-id="729f7-137">8</span></span>     |
| <span data-ttu-id="729f7-138">**tempo de localização de certificado capicor \_ \_ \_ \_ válido**</span><span class="sxs-lookup"><span data-stu-id="729f7-138">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_VALID**</span></span>           | <span data-ttu-id="729f7-139">Retorna certificados cujo tempo é válido.</span><span class="sxs-lookup"><span data-stu-id="729f7-139">Returns certificates whose time is valid.</span></span><br/>                                                                                        | <span data-ttu-id="729f7-140">9</span><span class="sxs-lookup"><span data-stu-id="729f7-140">9</span></span>     |
| <span data-ttu-id="729f7-141">**tempo de localização de certificado capico \_ \_ \_ \_ \_ ainda não \_ válido**</span><span class="sxs-lookup"><span data-stu-id="729f7-141">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_NOT\_YET\_VALID**</span></span> | <span data-ttu-id="729f7-142">Retorna certificados cujo tempo ainda não é válido.</span><span class="sxs-lookup"><span data-stu-id="729f7-142">Returns certificates whose time is not yet valid.</span></span><br/>                                                                                | <span data-ttu-id="729f7-143">10</span><span class="sxs-lookup"><span data-stu-id="729f7-143">10</span></span>    |
| <span data-ttu-id="729f7-144">**tempo limite de localização do certificado CAPICOM \_ \_ \_ \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="729f7-144">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_EXPIRED**</span></span>         | <span data-ttu-id="729f7-145">Retorna certificados cujo tempo expirou.</span><span class="sxs-lookup"><span data-stu-id="729f7-145">Returns certificates whose time has expired.</span></span><br/>                                                                                     | <span data-ttu-id="729f7-146">11</span><span class="sxs-lookup"><span data-stu-id="729f7-146">11</span></span>    |
| <span data-ttu-id="729f7-147">**\_uso da \_ chave de localização de certificado CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="729f7-147">**CAPICOM\_CERTIFICATE\_FIND\_KEY\_USAGE**</span></span>            | <span data-ttu-id="729f7-148">Retorna certificados que contêm uma chave que pode ser usada na maneira especificada.</span><span class="sxs-lookup"><span data-stu-id="729f7-148">Returns certificates containing a key that can be used in the specified manner.</span></span><br/>                                                  | <span data-ttu-id="729f7-149">12</span><span class="sxs-lookup"><span data-stu-id="729f7-149">12</span></span>    |



## <a name="remarks"></a><span data-ttu-id="729f7-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="729f7-150">Remarks</span></span>

<span data-ttu-id="729f7-151">O tipo de enumeração de **\_ tipo de \_ localização \_ do certificado capicor** é usado pelo método [**Certificates. Find**](certificates-find.md) .</span><span class="sxs-lookup"><span data-stu-id="729f7-151">The **CAPICOM\_CERTIFICATE\_FIND\_TYPE** enumeration type is used by the [**Certificates.Find**](certificates-find.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="729f7-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="729f7-152">Requirements</span></span>



| <span data-ttu-id="729f7-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="729f7-153">Requirement</span></span> | <span data-ttu-id="729f7-154">Valor</span><span class="sxs-lookup"><span data-stu-id="729f7-154">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="729f7-155">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="729f7-155">Redistributable</span></span><br/> | <span data-ttu-id="729f7-156">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="729f7-156">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="729f7-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="729f7-157">Header</span></span><br/>          | <dl> <span data-ttu-id="729f7-158"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="729f7-158"><dt>Capicom.h</dt></span></span> </dl> |



 

 




