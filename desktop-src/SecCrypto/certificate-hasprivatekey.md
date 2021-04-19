---
description: Determina se o certificado tem uma chave privada associada a ele. O método determina isso verificando se a \_ propriedade de ID prop da chave de certificado \_ Prov \_ \_ \_ está presente.
ms.assetid: 80478956-1ed7-4c25-9ae3-d7176649e6d7
title: 'Método ICertificate2:: HasPrivateKey'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.HasPrivateKey
- ICertificate2.HasPrivateKey
- ICertificate.HasPrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43110e48a1172977ad979d6ec2d94c5b8e3ffc50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753097"
---
# <a name="icertificate2hasprivatekey-method"></a><span data-ttu-id="2da0f-104">Método ICertificate2:: HasPrivateKey</span><span class="sxs-lookup"><span data-stu-id="2da0f-104">ICertificate2::HasPrivateKey method</span></span>

<span data-ttu-id="2da0f-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2da0f-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2da0f-106">Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="2da0f-106">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="2da0f-107">O método **HasPrivateKey** determina se o [*certificado*](../secgloss/c-gly.md) tem uma [*chave privada*](../secgloss/p-gly.md) associada a ele.</span><span class="sxs-lookup"><span data-stu-id="2da0f-107">The **HasPrivateKey** method determines whether the [*certificate*](../secgloss/c-gly.md) has a [*private key*](../secgloss/p-gly.md) associated with it.</span></span> <span data-ttu-id="2da0f-108">O método determina isso verificando se a \_ propriedade de ID prop da chave de certificado \_ Prov \_ \_ \_ está presente.</span><span class="sxs-lookup"><span data-stu-id="2da0f-108">The method determines this by checking whether the CERT\_KEY\_PROV\_INFO\_PROP\_ID property is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da0f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2da0f-109">Syntax</span></span>


```VB
Certificate.HasPrivateKey()
```



## <a name="parameters"></a><span data-ttu-id="2da0f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2da0f-110">Parameters</span></span>

<span data-ttu-id="2da0f-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2da0f-111">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="2da0f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2da0f-112">Requirements</span></span>



| <span data-ttu-id="2da0f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2da0f-113">Requirement</span></span> | <span data-ttu-id="2da0f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2da0f-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2da0f-115">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2da0f-115">End of client support</span></span><br/> | <span data-ttu-id="2da0f-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2da0f-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2da0f-117">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="2da0f-117">End of server support</span></span><br/> | <span data-ttu-id="2da0f-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2da0f-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2da0f-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2da0f-119">Redistributable</span></span><br/>       | <span data-ttu-id="2da0f-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="2da0f-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2da0f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2da0f-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2da0f-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2da0f-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da0f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2da0f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da0f-124">**PrivateKey. Open**</span><span class="sxs-lookup"><span data-stu-id="2da0f-124">**PrivateKey.Open**</span></span>](privatekey-open.md)
</dt> <dt>

[<span data-ttu-id="2da0f-125">Objetos de criptografia</span><span class="sxs-lookup"><span data-stu-id="2da0f-125">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="2da0f-126">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="2da0f-126">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
