---
description: Recupera o número de objetos PolicyInformation na coleção.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: Propriedade CertificatePolicies. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0ee51e37b3fd4ac66c4e615eaf068edc98a64807
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758168"
---
# <a name="certificatepoliciescount-property"></a><span data-ttu-id="364ca-103">Propriedade CertificatePolicies. Count</span><span class="sxs-lookup"><span data-stu-id="364ca-103">CertificatePolicies.Count property</span></span>

<span data-ttu-id="364ca-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="364ca-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="364ca-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para as políticas de certificado para recuperar as políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="364ca-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="364ca-106">A propriedade **Count** recupera o número de objetos [**PolicyInformation**](policyinformation.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="364ca-106">The **Count** property retrieves the number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span>

<span data-ttu-id="364ca-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="364ca-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="364ca-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="364ca-108">Syntax</span></span>


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="364ca-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="364ca-109">Property value</span></span>

<span data-ttu-id="364ca-110">O número de objetos [**PolicyInformation**](policyinformation.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="364ca-110">The number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span> <span data-ttu-id="364ca-111">Cada objeto **PolicyInformation** representa uma única política de certificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="364ca-111">Each **PolicyInformation** object represents a single certificate policy in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="364ca-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="364ca-112">Remarks</span></span>

<span data-ttu-id="364ca-113">A propriedade **Count** pode ser usada para especificar o último objeto [**PolicyInformation**](policyinformation.md) na coleção ao recuperar um objeto **PolicyInformation** específico usando a propriedade [**CertificatePolicies. Item**](certificatepolicies-item.md) .</span><span class="sxs-lookup"><span data-stu-id="364ca-113">The **Count** property can be used to specify the last [**PolicyInformation**](policyinformation.md) object in the collection when retrieving a specific **PolicyInformation** object using the [**CertificatePolicies.Item**](certificatepolicies-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="364ca-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="364ca-114">Requirements</span></span>



| <span data-ttu-id="364ca-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="364ca-115">Requirement</span></span> | <span data-ttu-id="364ca-116">Valor</span><span class="sxs-lookup"><span data-stu-id="364ca-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="364ca-117">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="364ca-117">End of client support</span></span><br/> | <span data-ttu-id="364ca-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="364ca-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="364ca-119">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="364ca-119">End of server support</span></span><br/> | <span data-ttu-id="364ca-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="364ca-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="364ca-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="364ca-121">Redistributable</span></span><br/>       | <span data-ttu-id="364ca-122">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="364ca-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="364ca-123">DLL</span><span class="sxs-lookup"><span data-stu-id="364ca-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="364ca-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="364ca-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
