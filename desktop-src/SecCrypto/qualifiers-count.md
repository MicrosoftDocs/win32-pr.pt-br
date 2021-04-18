---
description: Recupera o número de objetos de qualificador na coleção.
ms.assetid: 9dafb83a-ff7f-4317-8ed4-2a46dcebf409
title: Propriedade qualifierrs. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ffb79941a78602bfda8f5287b0f4df7205d4d86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792671"
---
# <a name="qualifierscount-property"></a><span data-ttu-id="8e743-103">Propriedade qualifierrs. Count</span><span class="sxs-lookup"><span data-stu-id="8e743-103">Qualifiers.Count property</span></span>

<span data-ttu-id="8e743-104">\[A propriedade **Count** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="8e743-104">\[The **Count** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8e743-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="8e743-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="8e743-106">A propriedade **Count** recupera o número de objetos de [**qualificador**](qualifier.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="8e743-106">The **Count** property retrieves the number of [**Qualifier**](qualifier.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e743-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e743-107">Syntax</span></span>


```VB
Qualifiers.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="8e743-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8e743-108">Property value</span></span>

<span data-ttu-id="8e743-109">Número de objetos de [**qualificador**](qualifier.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="8e743-109">Number of [**Qualifier**](qualifier.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e743-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e743-110">Requirements</span></span>



| <span data-ttu-id="8e743-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e743-111">Requirement</span></span> | <span data-ttu-id="8e743-112">Valor</span><span class="sxs-lookup"><span data-stu-id="8e743-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e743-113">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="8e743-113">Redistributable</span></span><br/> | <span data-ttu-id="8e743-114">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="8e743-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8e743-115">DLL</span><span class="sxs-lookup"><span data-stu-id="8e743-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="8e743-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e743-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e743-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e743-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e743-118">**Qualificadores**</span><span class="sxs-lookup"><span data-stu-id="8e743-118">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
