---
description: Recupera o número de objetos de certificado na coleção.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Propriedade Certificates. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a67554530ce8c8dfdc1bfcfba1198cf778397ac2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760392"
---
# <a name="certificatescount-property"></a><span data-ttu-id="6d757-103">Propriedade Certificates. Count</span><span class="sxs-lookup"><span data-stu-id="6d757-103">Certificates.Count property</span></span>

<span data-ttu-id="6d757-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6d757-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6d757-105">Em vez disso, use a [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6d757-105">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6d757-106">A propriedade **Count** recupera o número de objetos de [**certificado**](certificate.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="6d757-106">The **Count** property retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d757-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d757-107">Syntax</span></span>


```VB
Certificates.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="6d757-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6d757-108">Property value</span></span>

<span data-ttu-id="6d757-109">O número de objetos de [**certificado**](certificate.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="6d757-109">The number of [**Certificate**](certificate.md) objects in the collection.</span></span> <span data-ttu-id="6d757-110">Cada objeto de **certificado** representa um único certificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="6d757-110">Each **Certificate** object represents a single certificate in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d757-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d757-111">Remarks</span></span>

<span data-ttu-id="6d757-112">O capicor dá suporte apenas a um único certificado para o repositório de [*cartão inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="6d757-112">CAPICOM only supports a single certificate for the [*smart card*](../secgloss/s-gly.md) store.</span></span> <span data-ttu-id="6d757-113">Mesmo que o armazenamento de cartão inteligente contenha mais de um certificado, essa propriedade conterá 1.</span><span class="sxs-lookup"><span data-stu-id="6d757-113">Even if the smart card store contains more than one certificate, this property will contain 1.</span></span> <span data-ttu-id="6d757-114">Para obter mais informações sobre o repositório de cartão inteligente, consulte o membro do **\_ repositório de \_ \_ usuários \_ do cartão inteligente CAPICOM** da enumeração do [**\_ \_ local de armazenamento CAPICOM**](capicom-store-location.md) .</span><span class="sxs-lookup"><span data-stu-id="6d757-114">For more information about the smart card store, see the **CAPICOM\_SMART\_CARD\_USER\_STORE** member of the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d757-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d757-115">Requirements</span></span>



| <span data-ttu-id="6d757-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d757-116">Requirement</span></span> | <span data-ttu-id="6d757-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6d757-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d757-118">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6d757-118">End of client support</span></span><br/> | <span data-ttu-id="6d757-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d757-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6d757-120">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="6d757-120">End of server support</span></span><br/> | <span data-ttu-id="6d757-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d757-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6d757-122">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6d757-122">Redistributable</span></span><br/>       | <span data-ttu-id="6d757-123">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="6d757-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6d757-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6d757-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6d757-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d757-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d757-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d757-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d757-127">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="6d757-127">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
