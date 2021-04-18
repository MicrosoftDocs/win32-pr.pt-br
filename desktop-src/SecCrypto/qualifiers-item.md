---
description: Recupera um qualificador com base em um índice especificado.
ms.assetid: 4d54358d-99de-4a1c-b843-41006f47a279
title: Propriedade Qualifiers. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 798b1f212aabd5b1ab34a1eefb626be4572b9c1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757064"
---
# <a name="qualifiersitem-property"></a><span data-ttu-id="c3cbc-103">Propriedade Qualifiers. Item</span><span class="sxs-lookup"><span data-stu-id="c3cbc-103">Qualifiers.Item property</span></span>

<span data-ttu-id="c3cbc-104">\[A propriedade **Item** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-104">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c3cbc-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="c3cbc-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="c3cbc-106">A propriedade **Item** recupera um qualificador com base em um índice especificado.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-106">The **Item** property retrieves a qualifier based on a specified index.</span></span> <span data-ttu-id="c3cbc-107">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3cbc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3cbc-108">Syntax</span></span>


```VB
Qualifiers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="c3cbc-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c3cbc-109">Property value</span></span>

<span data-ttu-id="c3cbc-110">Um objeto de [**qualificador**](qualifier.md) que representa o qualificador indexado da coleção.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-110">A [**Qualifier**](qualifier.md) object that represents the indexed qualifier of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3cbc-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3cbc-111">Requirements</span></span>



| <span data-ttu-id="c3cbc-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3cbc-112">Requirement</span></span> | <span data-ttu-id="c3cbc-113">Valor</span><span class="sxs-lookup"><span data-stu-id="c3cbc-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3cbc-114">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c3cbc-114">Redistributable</span></span><br/> | <span data-ttu-id="c3cbc-115">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c3cbc-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c3cbc-116">DLL</span><span class="sxs-lookup"><span data-stu-id="c3cbc-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="c3cbc-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3cbc-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3cbc-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3cbc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3cbc-119">**Qualificadores**</span><span class="sxs-lookup"><span data-stu-id="c3cbc-119">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
