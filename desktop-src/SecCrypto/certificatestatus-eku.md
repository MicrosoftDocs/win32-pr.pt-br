---
description: Retorna o objeto EKU usado para criar o objeto de cadeia.
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: Método CertificateStatus. EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d386251c6d7f674d3850de275559bcb87ea6d61e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770251"
---
# <a name="certificatestatuseku-method"></a><span data-ttu-id="66dca-103">Método CertificateStatus. EKU</span><span class="sxs-lookup"><span data-stu-id="66dca-103">CertificateStatus.EKU method</span></span>

<span data-ttu-id="66dca-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="66dca-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="66dca-105">Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="66dca-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="66dca-106">O método **EKU** retorna o objeto [**EKU**](eku.md) usado para criar o objeto de [**cadeia**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="66dca-106">The **EKU** method returns the [**EKU**](eku.md) object used to build the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="66dca-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66dca-107">Syntax</span></span>


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a><span data-ttu-id="66dca-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66dca-108">Parameters</span></span>

<span data-ttu-id="66dca-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="66dca-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66dca-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66dca-110">Return value</span></span>

<span data-ttu-id="66dca-111">Esse método retorna um objeto [**EKU**](eku.md) que indica a configuração de uso estendido de chave do [*certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="66dca-111">This method returns an [**EKU**](eku.md) object that indicates the extended key usage setting of the [*certificate*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="66dca-112">A configuração EKU estabelece o uso válido de um certificado.</span><span class="sxs-lookup"><span data-stu-id="66dca-112">The EKU setting establishes a certificate's valid use.</span></span> <span data-ttu-id="66dca-113">Apenas um único objeto **EKU** pode ser definido para cada certificado.</span><span class="sxs-lookup"><span data-stu-id="66dca-113">Only a single **EKU** object can be set for each certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="66dca-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="66dca-114">Remarks</span></span>

<span data-ttu-id="66dca-115">O método [**CertificateStatus. ApplicationPolicies**](certificatestatus-applicationpolicies.md) fornece a mesma funcionalidade que esse método, mas permite que muitas configurações sejam especificadas em vez de apenas um.</span><span class="sxs-lookup"><span data-stu-id="66dca-115">The [**CertificateStatus.ApplicationPolicies**](certificatestatus-applicationpolicies.md) method provides the same functionality as this method but allows many settings to be specified instead of only one.</span></span> <span data-ttu-id="66dca-116">Se a coleção de [**OIDs**](oids.md) retornada pelo método **ApplicationPolicies** contiver um ou mais objetos [**OID**](oid.md) , o objeto [**EKU**](eku.md) retornado por esse método será ignorado.</span><span class="sxs-lookup"><span data-stu-id="66dca-116">If the [**OIDs**](oids.md) collection returned by the **ApplicationPolicies** method contains one or more [**OID**](oid.md) objects, the [**EKU**](eku.md) object returned by this method is ignored.</span></span> <span data-ttu-id="66dca-117">Use o método **ApplicationPolicies** em vez desse método.</span><span class="sxs-lookup"><span data-stu-id="66dca-117">Use the **ApplicationPolicies** method instead of this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="66dca-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66dca-118">Requirements</span></span>



| <span data-ttu-id="66dca-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="66dca-119">Requirement</span></span> | <span data-ttu-id="66dca-120">Valor</span><span class="sxs-lookup"><span data-stu-id="66dca-120">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66dca-121">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="66dca-121">End of client support</span></span><br/> | <span data-ttu-id="66dca-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66dca-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="66dca-123">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="66dca-123">End of server support</span></span><br/> | <span data-ttu-id="66dca-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66dca-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="66dca-125">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="66dca-125">Redistributable</span></span><br/>       | <span data-ttu-id="66dca-126">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="66dca-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="66dca-127">DLL</span><span class="sxs-lookup"><span data-stu-id="66dca-127">DLL</span></span><br/>                   | <dl> <span data-ttu-id="66dca-128"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66dca-128"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66dca-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="66dca-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66dca-130">**CertificateStatus**</span><span class="sxs-lookup"><span data-stu-id="66dca-130">**CertificateStatus**</span></span>](certificatestatus.md)
</dt> <dt>

[<span data-ttu-id="66dca-131">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="66dca-131">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="66dca-132">**EKU**</span><span class="sxs-lookup"><span data-stu-id="66dca-132">**EKU**</span></span>](eku.md)
</dt> </dl>

 

 
