---
description: Fornece acesso somente leitura às propriedades de uso de chave de um certificado.
ms.assetid: 8b8e9076-1a4f-4383-ac4b-1322d52949f0
title: Objeto KeyUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d2324b4e1e06650f2eed7b63337f2bd48520498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758008"
---
# <a name="keyusage-object"></a><span data-ttu-id="39ae8-103">Objeto KeyUsage</span><span class="sxs-lookup"><span data-stu-id="39ae8-103">KeyUsage object</span></span>

<span data-ttu-id="39ae8-104">\[O objeto **KeyUsage** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="39ae8-104">\[The **KeyUsage** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="39ae8-105">Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="39ae8-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="39ae8-106">O objeto **KeyUsage** fornece acesso somente leitura às propriedades de uso de chave de um certificado.</span><span class="sxs-lookup"><span data-stu-id="39ae8-106">The **KeyUsage** object provides read-only access to key usage properties of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="39ae8-107">Membros</span><span class="sxs-lookup"><span data-stu-id="39ae8-107">Members</span></span>

<span data-ttu-id="39ae8-108">O objeto **KeyUsage** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="39ae8-108">The **KeyUsage** object has these types of members:</span></span>

-   [<span data-ttu-id="39ae8-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39ae8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39ae8-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39ae8-110">Properties</span></span>

<span data-ttu-id="39ae8-111">O objeto **KeyUsage** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="39ae8-111">The **KeyUsage** object has these properties.</span></span>



| <span data-ttu-id="39ae8-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="39ae8-112">Property</span></span>                                                                           | <span data-ttu-id="39ae8-113">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="39ae8-113">Access type</span></span>          | <span data-ttu-id="39ae8-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="39ae8-114">Description</span></span>                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39ae8-115">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="39ae8-115">**IsCritical**</span></span>](keyusage-iscritical.md)<br/>                               | <span data-ttu-id="39ae8-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39ae8-116">Read-only</span></span><br/> | <span data-ttu-id="39ae8-117">Recupera um valor booliano que indica se a extensão **KeyUsage** está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="39ae8-117">Retrieves a Boolean value that indicates whether the **KeyUsage** extension is marked critical.</span></span><br/>                                  |
| [<span data-ttu-id="39ae8-118">**IsCRLSignEnabled**</span><span class="sxs-lookup"><span data-stu-id="39ae8-118">**IsCRLSignEnabled**</span></span>](keyusage-iscrlsignenabled.md)<br/>                   | <span data-ttu-id="39ae8-119">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39ae8-119">Read-only</span></span><br/> | <span data-ttu-id="39ae8-120">Recupera um valor booliano que indica se o bit CRLSign está definido.</span><span class="sxs-lookup"><span data-stu-id="39ae8-120">Retrieves a Boolean value that indicates whether the CRLSign bit is set.</span></span><br/>                                                         |
| [<span data-ttu-id="39ae8-121">**IsDataEnciphermentEnabled**</span><span class="sxs-lookup"><span data-stu-id="39ae8-121">**IsDataEnciphermentEnabled**</span></span>](keyusage-isdataenciphermentenabled.md)<br/> | <span data-ttu-id="39ae8-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39ae8-122">Read-only</span></span><br/> | <span data-ttu-id="39ae8-123">Recupera um valor booliano que indica se o bit dataEncipherment está definido.</span><span class="sxs-lookup"><span data-stu-id="39ae8-123">Retrieves a Boolean value that indicates whether the dataEncipherment bit is set.</span></span><br/>                                                |
| [<span data-ttu-id="39ae8-124">**IsDecipherOnlyEnabled**</span><span class="sxs-lookup"><span data-stu-id="39ae8-124">**IsDecipherOnlyEnabled**</span></span>](keyusage-isdecipheronlyenabled.md)<br/>         | <span data-ttu-id="39ae8-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39ae8-125">Read-only</span></span><br/> | <span data-ttu-id="39ae8-126">Recupera um valor booliano que indica se o bit decipherOnly está definido.</span><span class="sxs-lookup"><span data-stu-id="39ae8-126">Retrieves a Boolean value that indicates whether the decipherOnly bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="39ae8-127">**IsDigitalSignatureEnabled**</span><span class="sxs-lookup"><span data-stu-id="39ae8-127">**IsDigitalSignatureEnabled**</span></span>](keyusage-isdigitalsignatureenabled.md)<br/> | <span data-ttu-id="39ae8-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39ae8-128">Read-only</span></span><br/> | <span data-ttu-id="39ae8-129">Recupera um valor booliano que indica se o bit digitalSignature está definido.</span><span class="sxs-lookup"><span data-stu-id="39ae8-129">Retrieves a Boolean value that indicates whether the digitalSignature bit is set.</span></span><br/>                                                |
| [<span data-ttu-id="39ae8-130">**IsEncipherOnlyEnabled**</span><span class="sxs-lookup"><span data-stu-id="39ae8-130">**IsEncipherOnlyEnabled**</span></span>](keyusage-isencipheronlyenabled.md)<br/>         | <span data-ttu-id="39ae8-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39ae8-131">Read-only</span></span><br/> | <span data-ttu-id="39ae8-132">Recupera um valor booliano que indica se o bit encipherOnly está definido.</span><span class="sxs-lookup"><span data-stu-id="39ae8-132">Retrieves a Boolean value that indicates whether the encipherOnly bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="39ae8-133">**IsKeyAgreementEnabled**</span><span class="sxs-lookup"><span data-stu-id="39ae8-133">**IsKeyAgreementEnabled**</span></span>](keyusage-iskeyagreementenabled.md)<br/>         | <span data-ttu-id="39ae8-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39ae8-134">Read-only</span></span><br/> | <span data-ttu-id="39ae8-135">Recupera um valor booliano que indica se o bit do keyagreement está definido.</span><span class="sxs-lookup"><span data-stu-id="39ae8-135">Retrieves a Boolean value that indicates whether the keyAgreement bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="39ae8-136">**IsKeyCertSignEnabled**</span><span class="sxs-lookup"><span data-stu-id="39ae8-136">**IsKeyCertSignEnabled**</span></span>](keyusage-iskeycertsignenabled.md)<br/>           | <span data-ttu-id="39ae8-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39ae8-137">Read-only</span></span><br/> | <span data-ttu-id="39ae8-138">Recupera um valor booliano que indica se o bit keyCertSign está definido.</span><span class="sxs-lookup"><span data-stu-id="39ae8-138">Retrieves a Boolean value that indicates whether the keyCertSign bit is set.</span></span><br/>                                                     |
| [<span data-ttu-id="39ae8-139">**IsKeyEnciphermentEnabled**</span><span class="sxs-lookup"><span data-stu-id="39ae8-139">**IsKeyEnciphermentEnabled**</span></span>](keyusage-iskeyenciphermentenabled.md)<br/>   | <span data-ttu-id="39ae8-140">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39ae8-140">Read-only</span></span><br/> | <span data-ttu-id="39ae8-141">Recupera um valor booliano que indica se o bit keyEncipherment está definido.</span><span class="sxs-lookup"><span data-stu-id="39ae8-141">Retrieves a Boolean value that indicates whether the keyEncipherment bit is set.</span></span><br/>                                                 |
| [<span data-ttu-id="39ae8-142">**IsNonRepudiationEnabled**</span><span class="sxs-lookup"><span data-stu-id="39ae8-142">**IsNonRepudiationEnabled**</span></span>](keyusage-isnonrepudiationenabled.md)<br/>     | <span data-ttu-id="39ae8-143">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39ae8-143">Read-only</span></span><br/> | <span data-ttu-id="39ae8-144">Recupera um valor booliano que indica se o bit nonRepudiationEnabled está definido.</span><span class="sxs-lookup"><span data-stu-id="39ae8-144">Retrieves a Boolean value that indicates whether the nonRepudiationEnabled bit is set.</span></span><br/>                                           |
| [<span data-ttu-id="39ae8-145">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="39ae8-145">**IsPresent**</span></span>](keyusage-ispresent.md)<br/>                                 | <span data-ttu-id="39ae8-146">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39ae8-146">Read-only</span></span><br/> | <span data-ttu-id="39ae8-147">Recupera um valor booliano que indica se a extensão **KeyUsage** está presente.</span><span class="sxs-lookup"><span data-stu-id="39ae8-147">Retrieves a Boolean value that indicates whether the **KeyUsage** extension is present.</span></span><br/> <span data-ttu-id="39ae8-148">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="39ae8-148">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="39ae8-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="39ae8-149">Remarks</span></span>

<span data-ttu-id="39ae8-150">Não é possível criar o objeto **KeyUsage** .</span><span class="sxs-lookup"><span data-stu-id="39ae8-150">The **KeyUsage** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="39ae8-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39ae8-151">Requirements</span></span>



| <span data-ttu-id="39ae8-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="39ae8-152">Requirement</span></span> | <span data-ttu-id="39ae8-153">Valor</span><span class="sxs-lookup"><span data-stu-id="39ae8-153">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39ae8-154">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="39ae8-154">Redistributable</span></span><br/> | <span data-ttu-id="39ae8-155">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="39ae8-155">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="39ae8-156">DLL</span><span class="sxs-lookup"><span data-stu-id="39ae8-156">DLL</span></span><br/>             | <dl> <span data-ttu-id="39ae8-157"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39ae8-157"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39ae8-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="39ae8-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39ae8-159">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="39ae8-159">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
