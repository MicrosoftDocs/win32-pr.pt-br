---
description: Representa uma cadeia de certificados confiáveis.
ms.assetid: 45ed686f-4a7f-4df9-8366-98b825c3c657
title: Objeto chain
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fa3432767ccfdb60a2e3bc0a50ddbbcf565e0aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780169"
---
# <a name="chain-object"></a><span data-ttu-id="7015a-103">Objeto chain</span><span class="sxs-lookup"><span data-stu-id="7015a-103">Chain object</span></span>

<span data-ttu-id="7015a-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7015a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7015a-105">Em vez disso, use a [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7015a-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7015a-106">O objeto **Chain** representa uma cadeia de certificados confiáveis.</span><span class="sxs-lookup"><span data-stu-id="7015a-106">The **Chain** object represents a certificate trust chain.</span></span>

<span data-ttu-id="7015a-107">Esse objeto fornece propriedades e métodos para criar uma cadeia de certificados confiáveis para verificar a validade dos certificados.</span><span class="sxs-lookup"><span data-stu-id="7015a-107">This object provides properties and methods to build a certificate trust chain to check the validity of certificates.</span></span> <span data-ttu-id="7015a-108">A cadeia é criada usando o valor da propriedade [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) e as configurações de política de um objeto [**CertificateStatus**](certificatestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="7015a-108">The chain is built using the [**CertificateStatus.CheckFlag**](certificatestatus-checkflag.md) property value and the policy settings of a [**CertificateStatus**](certificatestatus.md) object.</span></span>

<span data-ttu-id="7015a-109">O objeto **Chain** expõe as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="7015a-109">The **Chain** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="7015a-110">**IChain2**: introduzido no capicom 2,0.</span><span class="sxs-lookup"><span data-stu-id="7015a-110">**IChain2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="7015a-111">**IChain**: introduzido no capicom 1,0.</span><span class="sxs-lookup"><span data-stu-id="7015a-111">**IChain**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="7015a-112">Quando usar</span><span class="sxs-lookup"><span data-stu-id="7015a-112">When to use</span></span>

<span data-ttu-id="7015a-113">O objeto **Chain** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="7015a-113">The **Chain** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="7015a-114">Crie uma cadeia de certificados confiáveis.</span><span class="sxs-lookup"><span data-stu-id="7015a-114">Build a certificate trust chain.</span></span>
-   <span data-ttu-id="7015a-115">Obtenha os OIDs de todas as políticas de certificado e de aplicativo válidas para a cadeia.</span><span class="sxs-lookup"><span data-stu-id="7015a-115">Obtain the OIDs of all the certificate and application policies valid for the chain.</span></span>
-   <span data-ttu-id="7015a-116">Verifique o status dos certificados na cadeia.</span><span class="sxs-lookup"><span data-stu-id="7015a-116">Verify the status of the certificates in the chain.</span></span>
-   <span data-ttu-id="7015a-117">Obter informações de erro estendidas.</span><span class="sxs-lookup"><span data-stu-id="7015a-117">Obtain extended error information.</span></span>
-   <span data-ttu-id="7015a-118">Recupere a coleção de certificados na cadeia.</span><span class="sxs-lookup"><span data-stu-id="7015a-118">Retrieve the collection of certificates in the chain.</span></span>

## <a name="members"></a><span data-ttu-id="7015a-119">Membros</span><span class="sxs-lookup"><span data-stu-id="7015a-119">Members</span></span>

<span data-ttu-id="7015a-120">O objeto **Chain** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7015a-120">The **Chain** object has these types of members:</span></span>

-   [<span data-ttu-id="7015a-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="7015a-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="7015a-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7015a-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7015a-123">Métodos</span><span class="sxs-lookup"><span data-stu-id="7015a-123">Methods</span></span>

<span data-ttu-id="7015a-124">O objeto **Chain** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7015a-124">The **Chain** object has these methods.</span></span>



| <span data-ttu-id="7015a-125">Método</span><span class="sxs-lookup"><span data-stu-id="7015a-125">Method</span></span>                                                   | <span data-ttu-id="7015a-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="7015a-126">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7015a-127">**ApplicationPolicies**</span><span class="sxs-lookup"><span data-stu-id="7015a-127">**ApplicationPolicies**</span></span>](chain-applicationpolicies.md) | <span data-ttu-id="7015a-128">Retorna uma coleção de [**OIDs**](oids.md) que representa os OIDs de política de aplicativo válidos para a cadeia.</span><span class="sxs-lookup"><span data-stu-id="7015a-128">Returns an [**OIDs**](oids.md) collection that represents the application policy OIDs valid for the chain.</span></span><br/> <span data-ttu-id="7015a-129">(Herdado de **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="7015a-129">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                          |
| [<span data-ttu-id="7015a-130">**Integrado**</span><span class="sxs-lookup"><span data-stu-id="7015a-130">**Build**</span></span>](chain-build.md)                             | <span data-ttu-id="7015a-131">Cria uma cadeia de verificação de certificado de um certificado final para o [*certificado raiz*](../secgloss/r-gly.md)confiável, retornando um valor booliano que indica a validade geral da cadeia.</span><span class="sxs-lookup"><span data-stu-id="7015a-131">Builds a certificate verification chain from an end certificate to the trusted [*root certificate*](../secgloss/r-gly.md), returning a Boolean value that indicates the overall validity of the chain.</span></span><br/> <span data-ttu-id="7015a-132">(Herdado de **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="7015a-132">(Inherited from **ChainIChain2IChain**)</span></span> |
| [<span data-ttu-id="7015a-133">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="7015a-133">**CertificatePolicies**</span></span>](chain-certificatepolicies.md) | <span data-ttu-id="7015a-134">Retorna uma coleção de [**OIDs**](oids.md) que representa os OIDs de política de certificado válidos para a cadeia.</span><span class="sxs-lookup"><span data-stu-id="7015a-134">Returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs valid for the chain.</span></span><br/> <span data-ttu-id="7015a-135">(Herdado de **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="7015a-135">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                          |
| [<span data-ttu-id="7015a-136">**ExtendedErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="7015a-136">**ExtendedErrorInfo**</span></span>](chain-extendederrorinfo.md)     | <span data-ttu-id="7015a-137">Retorna uma cadeia de caracteres que contém informações de erro adicionais sobre a entrada indexada.</span><span class="sxs-lookup"><span data-stu-id="7015a-137">Returns a string that contains additional error information about the indexed entry.</span></span><br/> <span data-ttu-id="7015a-138">(Herdado de **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="7015a-138">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="7015a-139">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7015a-139">Properties</span></span>

<span data-ttu-id="7015a-140">O objeto **Chain** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7015a-140">The **Chain** object has these properties.</span></span>



| <span data-ttu-id="7015a-141">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7015a-141">Property</span></span>                                              | <span data-ttu-id="7015a-142">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="7015a-142">Access type</span></span>          | <span data-ttu-id="7015a-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="7015a-143">Description</span></span>                                                                                                                                                                                 |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7015a-144">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="7015a-144">**Certificates**</span></span>](chain-certificates.md)<br/> | <span data-ttu-id="7015a-145">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7015a-145">Read-only</span></span><br/> | <span data-ttu-id="7015a-146">Recupera uma coleção de [**certificados**](certificates.md) que representa os certificados na cadeia.</span><span class="sxs-lookup"><span data-stu-id="7015a-146">Retrieves a [**Certificates**](certificates.md) collection that represents the certificates in the chain.</span></span> <span data-ttu-id="7015a-147">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="7015a-147">This is the default property.</span></span><br/> <span data-ttu-id="7015a-148">(Herdado de **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="7015a-148">(Inherited from **ChainIChain2IChain**)</span></span> |
| [<span data-ttu-id="7015a-149">**Status**</span><span class="sxs-lookup"><span data-stu-id="7015a-149">**Status**</span></span>](chain-status.md)<br/>             | <span data-ttu-id="7015a-150">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7015a-150">Read-only</span></span><br/> | <span data-ttu-id="7015a-151">Recupera o status de validade da cadeia ou um certificado específico na cadeia.</span><span class="sxs-lookup"><span data-stu-id="7015a-151">Retrieves the validity status of the chain or a specific certificate in the chain.</span></span><br/> <span data-ttu-id="7015a-152">(Herdado de **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="7015a-152">(Inherited from **ChainIChain2IChain**)</span></span>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="7015a-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="7015a-153">Remarks</span></span>

<span data-ttu-id="7015a-154">O objeto **Chain** pode ser criado e é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="7015a-154">The **Chain** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="7015a-155">O ProgID do objeto de **cadeia** é "CAPICOM. Chain. 2 ".</span><span class="sxs-lookup"><span data-stu-id="7015a-155">The ProgID for the **Chain** object is "CAPICOM.Chain.2".</span></span>

<span data-ttu-id="7015a-156">**CAPICOM 1. *x*:** a ProgID do objeto de **cadeia** é CAPICOM. Cadeia. 1.</span><span class="sxs-lookup"><span data-stu-id="7015a-156">**CAPICOM 1.*x*:** The ProgID for the **Chain** object is CAPICOM.Chain.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="7015a-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7015a-157">Requirements</span></span>



| <span data-ttu-id="7015a-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="7015a-158">Requirement</span></span> | <span data-ttu-id="7015a-159">Valor</span><span class="sxs-lookup"><span data-stu-id="7015a-159">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7015a-160">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7015a-160">End of client support</span></span><br/> | <span data-ttu-id="7015a-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7015a-161">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7015a-162">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="7015a-162">End of server support</span></span><br/> | <span data-ttu-id="7015a-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7015a-163">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7015a-164">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7015a-164">Redistributable</span></span><br/>       | <span data-ttu-id="7015a-165">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="7015a-165">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7015a-166">DLL</span><span class="sxs-lookup"><span data-stu-id="7015a-166">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7015a-167"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7015a-167"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7015a-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="7015a-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7015a-169">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="7015a-169">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
