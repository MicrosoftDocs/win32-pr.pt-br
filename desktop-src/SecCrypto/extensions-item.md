---
description: A propriedade item recupera uma extensão, por índice, da coleção. Essa é a propriedade padrão.
ms.assetid: 0242dc14-abf2-49df-b75a-9005b2376cfc
title: Propriedade Extensions. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b2cefe9ac1dd278c17161cc8e2349c051dccabff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761865"
---
# <a name="extensionsitem-property"></a><span data-ttu-id="04b4f-104">Propriedade Extensions. Item</span><span class="sxs-lookup"><span data-stu-id="04b4f-104">Extensions.Item property</span></span>

<span data-ttu-id="04b4f-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="04b4f-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="04b4f-106">Em vez disso, use a [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="04b4f-106">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="04b4f-107">A propriedade **Item** recupera uma extensão, por índice, da coleção.</span><span class="sxs-lookup"><span data-stu-id="04b4f-107">The **Item** property retrieves an extension, by index, from the collection.</span></span> <span data-ttu-id="04b4f-108">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="04b4f-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b4f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="04b4f-109">Syntax</span></span>


```VB
Extensions.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="04b4f-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="04b4f-110">Property value</span></span>

<span data-ttu-id="04b4f-111">Um objeto de [**extensão**](extension.md) que representa a extensão de certificado indexado da coleção.</span><span class="sxs-lookup"><span data-stu-id="04b4f-111">An [**Extension**](extension.md) object that represents the indexed certificate extension of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="04b4f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04b4f-112">Requirements</span></span>



| <span data-ttu-id="04b4f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="04b4f-113">Requirement</span></span> | <span data-ttu-id="04b4f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="04b4f-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04b4f-115">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="04b4f-115">End of client support</span></span><br/> | <span data-ttu-id="04b4f-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04b4f-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="04b4f-117">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="04b4f-117">End of server support</span></span><br/> | <span data-ttu-id="04b4f-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04b4f-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="04b4f-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="04b4f-119">Redistributable</span></span><br/>       | <span data-ttu-id="04b4f-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="04b4f-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="04b4f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="04b4f-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="04b4f-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04b4f-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04b4f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="04b4f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b4f-124">**Extensões**</span><span class="sxs-lookup"><span data-stu-id="04b4f-124">**Extensions**</span></span>](extensions.md)
</dt> </dl>

 

 
