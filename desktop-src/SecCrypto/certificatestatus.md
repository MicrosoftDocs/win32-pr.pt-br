---
description: Contém informações sobre como construir uma cadeia de certificados confiáveis.
ms.assetid: 120cd79e-7c9b-45f3-8596-091b674e73d8
title: Objeto CertificateStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e9a6cb31a00f4d2943e68670930e6cbc4436b6b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756378"
---
# <a name="certificatestatus-object"></a><span data-ttu-id="a87f9-103">Objeto CertificateStatus</span><span class="sxs-lookup"><span data-stu-id="a87f9-103">CertificateStatus object</span></span>

<span data-ttu-id="a87f9-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a87f9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a87f9-105">Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a87f9-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a87f9-106">O objeto **CertificateStatus** contém informações sobre como construir uma cadeia de certificados confiáveis.</span><span class="sxs-lookup"><span data-stu-id="a87f9-106">The **CertificateStatus** object contains information about how to construct a certificate trust chain.</span></span>

## <a name="members"></a><span data-ttu-id="a87f9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="a87f9-107">Members</span></span>

<span data-ttu-id="a87f9-108">O objeto **CertificateStatus** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a87f9-108">The **CertificateStatus** object has these types of members:</span></span>

-   [<span data-ttu-id="a87f9-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a87f9-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="a87f9-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a87f9-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a87f9-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a87f9-111">Methods</span></span>

<span data-ttu-id="a87f9-112">O objeto **CertificateStatus** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a87f9-112">The **CertificateStatus** object has these methods.</span></span>



| <span data-ttu-id="a87f9-113">Método</span><span class="sxs-lookup"><span data-stu-id="a87f9-113">Method</span></span>                                                               | <span data-ttu-id="a87f9-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a87f9-114">Description</span></span>                                                                                                                                  |
|:---------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a87f9-115">**ApplicationPolicies**</span><span class="sxs-lookup"><span data-stu-id="a87f9-115">**ApplicationPolicies**</span></span>](certificatestatus-applicationpolicies.md) | <span data-ttu-id="a87f9-116">Retorna uma coleção de [**OIDs**](oids.md) que representa os OIDs de política de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a87f9-116">Returns an [**OIDs**](oids.md) collection that represents the application policy OIDs.</span></span><br/>                                           |
| [<span data-ttu-id="a87f9-117">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="a87f9-117">**CertificatePolicies**</span></span>](certificatestatus-certificatepolicies.md) | <span data-ttu-id="a87f9-118">Retorna uma coleção de [**OIDs**](oids.md) que representa os OIDs de política de certificado usados durante a criação de cadeia.</span><span class="sxs-lookup"><span data-stu-id="a87f9-118">Returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs used during chain building.</span></span><br/>                |
| [<span data-ttu-id="a87f9-119">**EKU**</span><span class="sxs-lookup"><span data-stu-id="a87f9-119">**EKU**</span></span>](certificatestatus-eku.md)                                 | <span data-ttu-id="a87f9-120">Retorna o objeto [**EKU**](eku.md) usado para definir os elementos EKU a serem verificados no estabelecimento do status de validade de um certificado.</span><span class="sxs-lookup"><span data-stu-id="a87f9-120">Returns the [**EKU**](eku.md) object used to set the EKU elements to be checked in establishing a certificate's validity status.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a87f9-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a87f9-121">Properties</span></span>

<span data-ttu-id="a87f9-122">O objeto **CertificateStatus** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a87f9-122">The **CertificateStatus** object has these properties.</span></span>



| <span data-ttu-id="a87f9-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a87f9-123">Property</span></span>                                                                        | <span data-ttu-id="a87f9-124">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="a87f9-124">Access type</span></span>           | <span data-ttu-id="a87f9-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="a87f9-125">Description</span></span>                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a87f9-126">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="a87f9-126">**Certificates**</span></span>](certificatestatus-certificates.md)<br/>               | <span data-ttu-id="a87f9-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a87f9-127">Read/write</span></span><br/> | <span data-ttu-id="a87f9-128">Define ou recupera a coleção de certificados que podem ser usados para criar a cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="a87f9-128">Sets or retrieves the collection of certificates that can be used to build the certificate chain.</span></span><br/> <span data-ttu-id="a87f9-129">**CAPICOM 2.0.0.3 e anteriores:** Não há suporte para a propriedade [**Certificates**](certificatestatus-certificates.md) .</span><span class="sxs-lookup"><span data-stu-id="a87f9-129">**CAPICOM 2.0.0.3 and earlier:** The [**Certificates**](certificatestatus-certificates.md) property is not supported.</span></span><br/>                    |
| [<span data-ttu-id="a87f9-130">**CheckFlag**</span><span class="sxs-lookup"><span data-stu-id="a87f9-130">**CheckFlag**</span></span>](certificatestatus-checkflag.md)<br/>                     | <span data-ttu-id="a87f9-131">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a87f9-131">Read/write</span></span><br/> | <span data-ttu-id="a87f9-132">Sinalizador de verificação de validade.</span><span class="sxs-lookup"><span data-stu-id="a87f9-132">Validity check flag.</span></span> <span data-ttu-id="a87f9-133">Os valores podem ser Unidos usando um operador **or** lógico.</span><span class="sxs-lookup"><span data-stu-id="a87f9-133">Values can be joined by using a logical **OR** operator.</span></span> <span data-ttu-id="a87f9-134">O sinalizador de verificação padrão é [**Capicot \_ verificar \_ \_ tudo online**](capicom-check-flag.md).</span><span class="sxs-lookup"><span data-stu-id="a87f9-134">The default check flag is [**CAPICOM\_CHECK\_ONLINE\_ALL**](capicom-check-flag.md).</span></span><br/>                                                                                     |
| [<span data-ttu-id="a87f9-135">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="a87f9-135">**Result**</span></span>](certificatestatus-result.md)<br/>                           | <span data-ttu-id="a87f9-136">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a87f9-136">Read-only</span></span><br/>  | <span data-ttu-id="a87f9-137">Indica se o certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="a87f9-137">Indicates whether the certificate is valid.</span></span> <span data-ttu-id="a87f9-138">A validade do certificado é verificada usando a configuração atual da propriedade [**CheckFlag**](certificatestatus-checkflag.md) e as configurações de política do certificado.</span><span class="sxs-lookup"><span data-stu-id="a87f9-138">The certificate's validity is checked using the current setting of the [**CheckFlag**](certificatestatus-checkflag.md) property and the policy settings of the certificate.</span></span> <span data-ttu-id="a87f9-139">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="a87f9-139">This is the default property.</span></span><br/> |
| [<span data-ttu-id="a87f9-140">**UrlRetrievalTimeout**</span><span class="sxs-lookup"><span data-stu-id="a87f9-140">**UrlRetrievalTimeout**</span></span>](certificatestatus-urlretrievaltimeout.md)<br/> | <span data-ttu-id="a87f9-141">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a87f9-141">Read/write</span></span><br/> | <span data-ttu-id="a87f9-142">Define ou recupera o período de tempo antes que uma URL seja determinada como inacessível.</span><span class="sxs-lookup"><span data-stu-id="a87f9-142">Sets or retrieves the length of time before a URL is determined to be unreachable.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="a87f9-143">**Verificação de**</span><span class="sxs-lookup"><span data-stu-id="a87f9-143">**VerificationTime**</span></span>](certificatestatus-verificationtime.md)<br/>       | <span data-ttu-id="a87f9-144">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a87f9-144">Read/write</span></span><br/> | <span data-ttu-id="a87f9-145">Define ou recupera a hora em que o certificado foi verificado.</span><span class="sxs-lookup"><span data-stu-id="a87f9-145">Sets or retrieves the time that the certificate was verified.</span></span><br/>                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="a87f9-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="a87f9-146">Remarks</span></span>

<span data-ttu-id="a87f9-147">O objeto **CertificateStatus** não pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="a87f9-147">The **CertificateStatus** object cannot be created.</span></span>

<span data-ttu-id="a87f9-148">O objeto **CertificateStatus** é retornado pelo método [**Certificate. IsValid**](certificate-isvalid.md) .</span><span class="sxs-lookup"><span data-stu-id="a87f9-148">The **CertificateStatus** object is returned by the [**Certificate.IsValid**](certificate-isvalid.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a87f9-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a87f9-149">Requirements</span></span>



| <span data-ttu-id="a87f9-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="a87f9-150">Requirement</span></span> | <span data-ttu-id="a87f9-151">Valor</span><span class="sxs-lookup"><span data-stu-id="a87f9-151">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a87f9-152">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a87f9-152">End of client support</span></span><br/> | <span data-ttu-id="a87f9-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a87f9-153">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a87f9-154">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a87f9-154">End of server support</span></span><br/> | <span data-ttu-id="a87f9-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a87f9-155">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a87f9-156">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a87f9-156">Redistributable</span></span><br/>       | <span data-ttu-id="a87f9-157">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="a87f9-157">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a87f9-158">DLL</span><span class="sxs-lookup"><span data-stu-id="a87f9-158">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a87f9-159"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a87f9-159"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a87f9-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="a87f9-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a87f9-161">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="a87f9-161">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="a87f9-162">**Cadeia**</span><span class="sxs-lookup"><span data-stu-id="a87f9-162">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
