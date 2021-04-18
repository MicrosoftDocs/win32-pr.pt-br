---
description: Recupera o OID da política. Essa é a propriedade padrão.
ms.assetid: c78bbbcb-befd-491c-afbd-80c3ba124d29
title: Propriedade PolicyInformation. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9acab40130ef6c55bf014058b3e5a6d935ed8a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800079"
---
# <a name="policyinformationoid-property"></a><span data-ttu-id="224ab-104">Propriedade PolicyInformation. OID</span><span class="sxs-lookup"><span data-stu-id="224ab-104">PolicyInformation.OID property</span></span>

<span data-ttu-id="224ab-105">\[A propriedade **OID** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="224ab-105">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="224ab-106">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar informações de política na extensão de políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="224ab-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="224ab-107">A propriedade **OID** recupera o OID da política.</span><span class="sxs-lookup"><span data-stu-id="224ab-107">The **OID** property retrieves the policy's OID.</span></span> <span data-ttu-id="224ab-108">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="224ab-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="224ab-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="224ab-109">Syntax</span></span>


```VB
PolicyInformation.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="224ab-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="224ab-110">Property value</span></span>

<span data-ttu-id="224ab-111">O identificador de objeto da política como um objeto de [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="224ab-111">The policy's object identifier as an [**OID**](oid.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="224ab-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="224ab-112">Requirements</span></span>



| <span data-ttu-id="224ab-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="224ab-113">Requirement</span></span> | <span data-ttu-id="224ab-114">Valor</span><span class="sxs-lookup"><span data-stu-id="224ab-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="224ab-115">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="224ab-115">Redistributable</span></span><br/> | <span data-ttu-id="224ab-116">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="224ab-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="224ab-117">DLL</span><span class="sxs-lookup"><span data-stu-id="224ab-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="224ab-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="224ab-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="224ab-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="224ab-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="224ab-120">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="224ab-120">**PolicyInformation**</span></span>](policyinformation.md)
</dt> </dl>

 

 
