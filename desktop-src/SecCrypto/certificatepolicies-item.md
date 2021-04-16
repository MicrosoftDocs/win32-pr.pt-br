---
description: Recupera o objeto PolicyInformation que representa a política indexada. Essa é a propriedade padrão.
ms.assetid: 0143629a-97cf-43f4-8f96-774f0f5cfeca
title: Propriedade CertificatePolicies. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a41cfb88f5f3ad59a8dbf62c85eca2a13c69f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758167"
---
# <a name="certificatepoliciesitem-property"></a><span data-ttu-id="ed939-104">Propriedade CertificatePolicies. Item</span><span class="sxs-lookup"><span data-stu-id="ed939-104">CertificatePolicies.Item property</span></span>

<span data-ttu-id="ed939-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ed939-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ed939-106">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para as políticas de certificado para recuperar as políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="ed939-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="ed939-107">A propriedade **Item** recupera o objeto [**PolicyInformation**](policyinformation.md) que representa a política indexada.</span><span class="sxs-lookup"><span data-stu-id="ed939-107">The **Item** property retrieves the [**PolicyInformation**](policyinformation.md) object that represents the indexed policy.</span></span> <span data-ttu-id="ed939-108">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="ed939-108">This is the default property.</span></span>

<span data-ttu-id="ed939-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="ed939-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed939-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed939-110">Syntax</span></span>


```VB
CertificatePolicies.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="ed939-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ed939-111">Property value</span></span>

<span data-ttu-id="ed939-112">Um objeto [**PolicyInformation**](policyinformation.md) que representa a política indexada.</span><span class="sxs-lookup"><span data-stu-id="ed939-112">A [**PolicyInformation**](policyinformation.md) object that represents the indexed policy.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed939-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed939-113">Requirements</span></span>



| <span data-ttu-id="ed939-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed939-114">Requirement</span></span> | <span data-ttu-id="ed939-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ed939-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed939-116">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ed939-116">End of client support</span></span><br/> | <span data-ttu-id="ed939-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed939-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ed939-118">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="ed939-118">End of server support</span></span><br/> | <span data-ttu-id="ed939-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed939-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ed939-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ed939-120">Redistributable</span></span><br/>       | <span data-ttu-id="ed939-121">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="ed939-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ed939-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ed939-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ed939-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed939-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
