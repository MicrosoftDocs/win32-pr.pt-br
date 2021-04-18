---
description: Retorna um objeto ExtendedKeyUsage que indica os usos válidos do certificado.
ms.assetid: e974e9e2-1011-48b7-9ebc-e754e4990286
title: 'Método ICertificate2:: ExtendedKeyUsage'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ExtendedKeyUsage
- ICertificate2.ExtendedKeyUsage
- ICertificate.ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6f349b7267d58a9376b9295e3ffd5013954a0872
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754952"
---
# <a name="icertificate2extendedkeyusage-method"></a><span data-ttu-id="5c009-103">Método ICertificate2:: ExtendedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="5c009-103">ICertificate2::ExtendedKeyUsage method</span></span>

<span data-ttu-id="5c009-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5c009-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5c009-105">Em vez disso, use a [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="5c009-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="5c009-106">O método **ExtendedKeyUsage** retorna um objeto [**ExtendedKeyUsage**](extendedkeyusage.md) que indica os usos válidos do certificado.</span><span class="sxs-lookup"><span data-stu-id="5c009-106">The **ExtendedKeyUsage** method returns an [**ExtendedKeyUsage**](extendedkeyusage.md) object that indicates the valid uses of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c009-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c009-107">Syntax</span></span>


```VB
Certificate.ExtendedKeyUsage()
```



## <a name="parameters"></a><span data-ttu-id="5c009-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c009-108">Parameters</span></span>

<span data-ttu-id="5c009-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5c009-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c009-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c009-110">Return value</span></span>

<span data-ttu-id="5c009-111">O objeto [**ExtendedKeyUsage**](extendedkeyusage.md) que está associado ao certificado.</span><span class="sxs-lookup"><span data-stu-id="5c009-111">The [**ExtendedKeyUsage**](extendedkeyusage.md) object that is associated with the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c009-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c009-112">Requirements</span></span>



| <span data-ttu-id="5c009-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c009-113">Requirement</span></span> | <span data-ttu-id="5c009-114">Valor</span><span class="sxs-lookup"><span data-stu-id="5c009-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c009-115">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="5c009-115">End of client support</span></span><br/> | <span data-ttu-id="5c009-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c009-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5c009-117">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="5c009-117">End of server support</span></span><br/> | <span data-ttu-id="5c009-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c009-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5c009-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="5c009-119">Redistributable</span></span><br/>       | <span data-ttu-id="5c009-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="5c009-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5c009-121">DLL</span><span class="sxs-lookup"><span data-stu-id="5c009-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5c009-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c009-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c009-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c009-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c009-124">Objetos de criptografia</span><span class="sxs-lookup"><span data-stu-id="5c009-124">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="5c009-125">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="5c009-125">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
