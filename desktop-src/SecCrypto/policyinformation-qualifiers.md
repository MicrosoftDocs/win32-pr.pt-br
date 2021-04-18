---
description: Recupera uma coleção dos qualificadores da política.
ms.assetid: aa5e2225-0a39-40bc-868c-d96f5953edaa
title: Propriedade PolicyInformation. Qualifiers (IADs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 89f24e21acd24cbcaa021f7c668fc8c208102c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811050"
---
# <a name="policyinformationqualifiers-property"></a><span data-ttu-id="5d9d0-103">Propriedade PolicyInformation. Qualifiers</span><span class="sxs-lookup"><span data-stu-id="5d9d0-103">PolicyInformation.Qualifiers property</span></span>

<span data-ttu-id="5d9d0-104">\[A propriedade **Qualifiers** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="5d9d0-104">\[The **Qualifiers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5d9d0-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar informações de política na extensão de políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="5d9d0-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="5d9d0-106">A propriedade **Qualifiers** recupera uma coleção dos qualificadores da política.</span><span class="sxs-lookup"><span data-stu-id="5d9d0-106">The **Qualifiers** property retrieves a collection of the policy's qualifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d9d0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d9d0-107">Syntax</span></span>


```VB
PolicyInformation.Qualifiers As Qualifiers
```



## <a name="property-value"></a><span data-ttu-id="5d9d0-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5d9d0-108">Property value</span></span>

<span data-ttu-id="5d9d0-109">O ponteiro do CPS (instrução de prática de certificação) da política ou os qualificadores de aviso do usuário, como um objeto de [**qualificadores**](qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="5d9d0-109">The policy's Certification Practice Statement (CPS) pointer or user notice qualifiers, as a [**Qualifiers**](qualifiers.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d9d0-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d9d0-110">Requirements</span></span>



| <span data-ttu-id="5d9d0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d9d0-111">Requirement</span></span> | <span data-ttu-id="5d9d0-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5d9d0-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d9d0-113">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="5d9d0-113">Redistributable</span></span><br/> | <span data-ttu-id="5d9d0-114">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="5d9d0-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5d9d0-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d9d0-115">Header</span></span><br/>          | <dl> <span data-ttu-id="5d9d0-116"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d9d0-116"><dt>Iads.h</dt></span></span> </dl>      |
| <span data-ttu-id="5d9d0-117">DLL</span><span class="sxs-lookup"><span data-stu-id="5d9d0-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="5d9d0-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d9d0-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d9d0-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d9d0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d9d0-120">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="5d9d0-120">**PolicyInformation**</span></span>](policyinformation.md)
</dt> </dl>

 

 
