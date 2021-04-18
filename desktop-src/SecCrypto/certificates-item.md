---
description: Recupera um objeto de certificado que representa o certificado indexado da coleção. Essa é a propriedade padrão.
ms.assetid: 733f2b93-c059-4041-b7cd-8c20218f1462
title: Propriedade Certificates. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bbafaf20f74910e8ea5eb525f48374a2807fa030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794430"
---
# <a name="certificatesitem-property"></a><span data-ttu-id="35e9e-104">Propriedade Certificates. Item</span><span class="sxs-lookup"><span data-stu-id="35e9e-104">Certificates.Item property</span></span>

<span data-ttu-id="35e9e-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="35e9e-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="35e9e-106">Em vez disso, use a [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="35e9e-106">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="35e9e-107">A propriedade **Item** recupera um objeto de [**certificado**](certificate.md) que representa o certificado indexado da coleção.</span><span class="sxs-lookup"><span data-stu-id="35e9e-107">The **Item** property retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="35e9e-108">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="35e9e-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e9e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="35e9e-109">Syntax</span></span>


```VB
Certificates.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="35e9e-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="35e9e-110">Property value</span></span>

<span data-ttu-id="35e9e-111">Um objeto de [**certificado**](certificate.md) que representa o certificado indexado.</span><span class="sxs-lookup"><span data-stu-id="35e9e-111">A [**Certificate**](certificate.md) object that represents the indexed certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="35e9e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35e9e-112">Requirements</span></span>



| <span data-ttu-id="35e9e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="35e9e-113">Requirement</span></span> | <span data-ttu-id="35e9e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="35e9e-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35e9e-115">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="35e9e-115">End of client support</span></span><br/> | <span data-ttu-id="35e9e-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35e9e-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="35e9e-117">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="35e9e-117">End of server support</span></span><br/> | <span data-ttu-id="35e9e-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35e9e-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="35e9e-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="35e9e-119">Redistributable</span></span><br/>       | <span data-ttu-id="35e9e-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="35e9e-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="35e9e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="35e9e-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="35e9e-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35e9e-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35e9e-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="35e9e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35e9e-124">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="35e9e-124">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
