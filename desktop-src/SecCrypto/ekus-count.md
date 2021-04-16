---
description: Recupera o número de objetos EKU na coleção.
ms.assetid: a38ac480-4f9b-4d69-a7e6-fae4993fe2cf
title: Propriedade EKUs. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41e77f3803fa65db1573c6619ebf1265b7418924
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751517"
---
# <a name="ekuscount-property"></a><span data-ttu-id="00a4b-103">Propriedade EKUs. Count</span><span class="sxs-lookup"><span data-stu-id="00a4b-103">EKUs.Count property</span></span>

<span data-ttu-id="00a4b-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="00a4b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="00a4b-105">Em vez disso, use a [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="00a4b-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="00a4b-106">A propriedade **Count** recupera o número de objetos [**EKU**](eku.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="00a4b-106">The **Count** property retrieves the number of [**EKU**](eku.md) objects in the collection.</span></span>

<span data-ttu-id="00a4b-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="00a4b-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="00a4b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00a4b-108">Syntax</span></span>


```VB
EKUs.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="00a4b-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="00a4b-109">Property value</span></span>

<span data-ttu-id="00a4b-110">O número de objetos [**EKU**](eku.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="00a4b-110">The number of [**EKU**](eku.md) objects in the collection.</span></span> <span data-ttu-id="00a4b-111">Cada objeto **EKU** representa uma única propriedade EKU (uso estendido de chave) de um certificado.</span><span class="sxs-lookup"><span data-stu-id="00a4b-111">Each **EKU** object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="00a4b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="00a4b-112">Remarks</span></span>

<span data-ttu-id="00a4b-113">A propriedade **Count** pode ser usada para especificar o último objeto [**EKU**](eku.md) em uma coleção ao recuperar um objeto **EKU** específico usando a propriedade [**EKUs. Item**](ekus-item.md) .</span><span class="sxs-lookup"><span data-stu-id="00a4b-113">The **Count** property can be used to specify the last [**EKU**](eku.md) object in a collection when retrieving a specific **EKU** object using the [**EKUs.Item**](ekus-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="00a4b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00a4b-114">Requirements</span></span>



| <span data-ttu-id="00a4b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="00a4b-115">Requirement</span></span> | <span data-ttu-id="00a4b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="00a4b-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00a4b-117">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="00a4b-117">End of client support</span></span><br/> | <span data-ttu-id="00a4b-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00a4b-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="00a4b-119">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="00a4b-119">End of server support</span></span><br/> | <span data-ttu-id="00a4b-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00a4b-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="00a4b-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="00a4b-121">Redistributable</span></span><br/>       | <span data-ttu-id="00a4b-122">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="00a4b-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="00a4b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="00a4b-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="00a4b-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00a4b-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
