---
description: A propriedade Algorithm recupera o objeto OID que identifica o algoritmo usado pela chave pública. Essa é a propriedade padrão.
ms.assetid: f804ac4b-6a33-4f25-950b-6b6838bcc638
title: Propriedade PublicKey. Algorithm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98e955279646306b1484dcd0674cf735680d44e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753396"
---
# <a name="publickeyalgorithm-property"></a><span data-ttu-id="6f14f-104">Propriedade PublicKey. Algorithm</span><span class="sxs-lookup"><span data-stu-id="6f14f-104">PublicKey.Algorithm property</span></span>

<span data-ttu-id="6f14f-105">\[A propriedade de **algoritmo** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="6f14f-105">\[The **Algorithm** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6f14f-106">Em vez disso, use a [**Propriedade X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6f14f-106">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6f14f-107">A propriedade **Algorithm** recupera o objeto [**OID**](oid.md) que identifica o algoritmo usado pela chave pública.</span><span class="sxs-lookup"><span data-stu-id="6f14f-107">The **Algorithm** property retrieves the [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span> <span data-ttu-id="6f14f-108">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="6f14f-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f14f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f14f-109">Syntax</span></span>


```VB
PublicKey.Algorithm As OID
```



## <a name="property-value"></a><span data-ttu-id="6f14f-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6f14f-110">Property value</span></span>

<span data-ttu-id="6f14f-111">O objeto [**OID**](oid.md) que identifica o algoritmo usado pela chave pública.</span><span class="sxs-lookup"><span data-stu-id="6f14f-111">The [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f14f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f14f-112">Requirements</span></span>



| <span data-ttu-id="6f14f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f14f-113">Requirement</span></span> | <span data-ttu-id="6f14f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="6f14f-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f14f-115">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6f14f-115">Redistributable</span></span><br/> | <span data-ttu-id="6f14f-116">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="6f14f-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6f14f-117">DLL</span><span class="sxs-lookup"><span data-stu-id="6f14f-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="6f14f-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f14f-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f14f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f14f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f14f-120">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="6f14f-120">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
