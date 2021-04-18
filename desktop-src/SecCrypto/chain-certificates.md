---
description: A propriedade Certificates recupera uma coleção de certificados que representa os certificados na cadeia. Essa é a propriedade padrão.
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: 'Propriedade IChain2:: Certificates'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Certificates
- IChain2.get_Certificates
- IChain.Certificates
- IChain.get_Certificates
- Chain.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a166f1d0dfa7f027058be65c3371d5c055cdb7bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756377"
---
# <a name="ichain2certificates-property"></a><span data-ttu-id="13cc5-104">Propriedade IChain2:: Certificates</span><span class="sxs-lookup"><span data-stu-id="13cc5-104">IChain2::Certificates property</span></span>

<span data-ttu-id="13cc5-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="13cc5-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="13cc5-106">Em vez disso, use a [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="13cc5-106">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="13cc5-107">A propriedade **Certificates** recupera uma coleção de [**certificados**](certificates.md) que representa os certificados na cadeia.</span><span class="sxs-lookup"><span data-stu-id="13cc5-107">The **Certificates** property retrieves a [**Certificates**](certificates.md) collection that represents the certificates in the chain.</span></span> <span data-ttu-id="13cc5-108">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="13cc5-108">This is the default property.</span></span>

<span data-ttu-id="13cc5-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="13cc5-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="13cc5-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13cc5-110">Syntax</span></span>


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="13cc5-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="13cc5-111">Property value</span></span>

<span data-ttu-id="13cc5-112">Uma coleção de [**certificados**](certificates.md) que é usada para recuperar informações sobre cada certificado na cadeia.</span><span class="sxs-lookup"><span data-stu-id="13cc5-112">A [**Certificates**](certificates.md) collection that is used to retrieve information about each certificate in the chain.</span></span> <span data-ttu-id="13cc5-113">O primeiro certificado na coleção retornada, **Certificates. Item**(1), é o certificado final da cadeia.</span><span class="sxs-lookup"><span data-stu-id="13cc5-113">The first certificate in the returned collection, **Certificates.Item**(1), is the end certificate of the chain.</span></span> <span data-ttu-id="13cc5-114">O último certificado na coleção, **Certificates. Item**(**Certificates. Count**), é o [*certificado raiz*](../secgloss/r-gly.md) da cadeia.</span><span class="sxs-lookup"><span data-stu-id="13cc5-114">The last certificate in the collection, **Certificates.Item**(**Certificates.Count**), is the [*root certificate*](../secgloss/r-gly.md) of the chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="13cc5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13cc5-115">Requirements</span></span>



| <span data-ttu-id="13cc5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="13cc5-116">Requirement</span></span> | <span data-ttu-id="13cc5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="13cc5-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13cc5-118">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="13cc5-118">End of client support</span></span><br/> | <span data-ttu-id="13cc5-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13cc5-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="13cc5-120">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="13cc5-120">End of server support</span></span><br/> | <span data-ttu-id="13cc5-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13cc5-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="13cc5-122">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="13cc5-122">Redistributable</span></span><br/>       | <span data-ttu-id="13cc5-123">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="13cc5-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="13cc5-124">DLL</span><span class="sxs-lookup"><span data-stu-id="13cc5-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="13cc5-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13cc5-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
