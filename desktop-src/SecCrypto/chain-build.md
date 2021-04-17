---
description: Cria uma cadeia de verificação de certificado de um certificado final para o certificado raiz confiável e retorna um valor booliano que indica a validade geral da cadeia.
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: 'Método IChain2:: Build'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.Build
- IChain2.Build
- IChain.Build
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66ad51d94fdbd361a34e25b4b76289139abb87f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754502"
---
# <a name="ichain2build-method"></a><span data-ttu-id="2c31c-103">Método IChain2:: Build</span><span class="sxs-lookup"><span data-stu-id="2c31c-103">IChain2::Build method</span></span>

<span data-ttu-id="2c31c-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2c31c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2c31c-105">Em vez disso, use a [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="2c31c-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="2c31c-106">O método **Build** cria uma cadeia de verificação de certificado de um certificado final para o [*certificado raiz*](../secgloss/r-gly.md) confiável e retorna um valor booliano que indica a validade geral da cadeia.</span><span class="sxs-lookup"><span data-stu-id="2c31c-106">The **Build** method builds a certificate verification chain from an end certificate to the trusted [*root certificate*](../secgloss/r-gly.md) and returns a Boolean value that indicates the overall validity of the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c31c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c31c-107">Syntax</span></span>


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="2c31c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c31c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c31c-109">*Certificado* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2c31c-109">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c31c-110">Um objeto de [**certificado**](certificate.md) que representa o certificado final no qual a cadeia de verificação deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="2c31c-110">A [**Certificate**](certificate.md) object that represents the end certificate upon which the verification chain is to be built.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c31c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c31c-111">Return value</span></span>

<span data-ttu-id="2c31c-112">Um valor booliano que indica a validade geral da cadeia.</span><span class="sxs-lookup"><span data-stu-id="2c31c-112">A Boolean value that indicates the overall validity of the chain.</span></span> <span data-ttu-id="2c31c-113">A validade geral se baseia na política de verificação de validade em vigor.</span><span class="sxs-lookup"><span data-stu-id="2c31c-113">Overall validity is based on the validity checking policy in place.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c31c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c31c-114">Remarks</span></span>

<span data-ttu-id="2c31c-115">A cadeia é criada usando a propriedade [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) , bem como as políticas de aplicativo e certificado especificadas por um objeto [**CertificateStatus**](certificatestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="2c31c-115">The chain is built using the [**CertificateStatus.CheckFlag**](certificatestatus-checkflag.md) property as well as application and certificate policies specified by a [**CertificateStatus**](certificatestatus.md) object.</span></span> <span data-ttu-id="2c31c-116">A coleção retornada é ordenada; o primeiro certificado na coleção, **Certificates. Item**(1), é o certificado final da cadeia.</span><span class="sxs-lookup"><span data-stu-id="2c31c-116">The returned collection is ordered; the first certificate in the collection, **Certificates.Item**(1), is the end certificate of the chain.</span></span> <span data-ttu-id="2c31c-117">O último certificado na coleção, **Certificates. Item**(**Certificates. Count**), é o [*certificado raiz*](../secgloss/r-gly.md) da cadeia.</span><span class="sxs-lookup"><span data-stu-id="2c31c-117">The last certificate in the collection, **Certificates.Item**(**Certificates.Count**), is the [*root certificate*](../secgloss/r-gly.md) of the chain.</span></span> <span data-ttu-id="2c31c-118">**Certificates. Item**(0) representa a cadeia inteira.</span><span class="sxs-lookup"><span data-stu-id="2c31c-118">**Certificates.Item**(0) represents the entire chain.</span></span>

<span data-ttu-id="2c31c-119">Cada vez que o método **Chain. Build** é chamado, o [*estado*](../secgloss/s-gly.md) do objeto de [**cadeia**](chain.md) é redefinido.</span><span class="sxs-lookup"><span data-stu-id="2c31c-119">Each time the **Chain.Build** method is called, the [*state*](../secgloss/s-gly.md) of the [**Chain**](chain.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c31c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c31c-120">Requirements</span></span>



| <span data-ttu-id="2c31c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c31c-121">Requirement</span></span> | <span data-ttu-id="2c31c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2c31c-122">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c31c-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2c31c-123">End of client support</span></span><br/> | <span data-ttu-id="2c31c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c31c-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2c31c-125">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="2c31c-125">End of server support</span></span><br/> | <span data-ttu-id="2c31c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c31c-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2c31c-127">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2c31c-127">Redistributable</span></span><br/>       | <span data-ttu-id="2c31c-128">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="2c31c-128">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2c31c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2c31c-129">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2c31c-130"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c31c-130"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c31c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c31c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c31c-132">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="2c31c-132">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="2c31c-133">**Cadeia**</span><span class="sxs-lookup"><span data-stu-id="2c31c-133">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
