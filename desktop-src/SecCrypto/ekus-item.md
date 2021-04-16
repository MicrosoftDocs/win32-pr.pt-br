---
description: Recupera o objeto EKU que representa a propriedade de EKU (uso estendido de chave) indexada.
ms.assetid: b8c12a7a-e836-48c2-958c-937b3723f85b
title: 'Propriedade IEKUs:: item'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKUs.Item
- IEKUs.get_Item
- EKUs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e3eaf8d0b303207aae3ef78cc82771e1436b1027
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752338"
---
# <a name="iekusitem-property"></a><span data-ttu-id="ba203-103">Propriedade IEKUs:: item</span><span class="sxs-lookup"><span data-stu-id="ba203-103">IEKUs::Item property</span></span>

<span data-ttu-id="ba203-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ba203-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ba203-105">Em vez disso, use a [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="ba203-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ba203-106">A propriedade **Item** recupera o objeto [**EKU**](eku.md) que representa a propriedade de EKU (uso estendido de chave) indexada.</span><span class="sxs-lookup"><span data-stu-id="ba203-106">The **Item** property retrieves the [**EKU**](eku.md) object that represents the indexed extended key usage (EKU) property.</span></span>

<span data-ttu-id="ba203-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="ba203-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba203-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba203-108">Syntax</span></span>


```VB
EKUs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="ba203-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ba203-109">Property value</span></span>

<span data-ttu-id="ba203-110">Um objeto [**EKU**](eku.md) que representa a propriedade de EKU (uso estendido de chave) indexado.</span><span class="sxs-lookup"><span data-stu-id="ba203-110">An [**EKU**](eku.md) object that represents the indexed extended key usage (EKU) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba203-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba203-111">Requirements</span></span>



| <span data-ttu-id="ba203-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba203-112">Requirement</span></span> | <span data-ttu-id="ba203-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ba203-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba203-114">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ba203-114">End of client support</span></span><br/> | <span data-ttu-id="ba203-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba203-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ba203-116">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="ba203-116">End of server support</span></span><br/> | <span data-ttu-id="ba203-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba203-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ba203-118">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ba203-118">Redistributable</span></span><br/>       | <span data-ttu-id="ba203-119">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="ba203-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ba203-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ba203-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ba203-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba203-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba203-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba203-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba203-123">**EKUs**</span><span class="sxs-lookup"><span data-stu-id="ba203-123">**EKUs**</span></span>](ekus.md)
</dt> </dl>

 

 
