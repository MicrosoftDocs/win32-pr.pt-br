---
description: Recupera um objeto OID da coleção. Essa é a propriedade padrão.
ms.assetid: af0de567-e520-411d-850d-fbdbcb2ace69
title: Propriedade OIDs. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dfdf65f013c5e5e1a031c03c19af9d08b8fc72c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760012"
---
# <a name="oidsitem-property"></a><span data-ttu-id="ee38e-104">Propriedade OIDs. Item</span><span class="sxs-lookup"><span data-stu-id="ee38e-104">OIDs.Item property</span></span>

<span data-ttu-id="ee38e-105">\[A propriedade **Item** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="ee38e-105">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ee38e-106">Em vez disso, use a [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="ee38e-106">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="ee38e-107">A propriedade **Item** recupera um objeto [**OID**](oid.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="ee38e-107">The **Item** property retrieves an [**OID**](oid.md) object from the collection.</span></span> <span data-ttu-id="ee38e-108">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="ee38e-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee38e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee38e-109">Syntax</span></span>


```VB
OIDs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="ee38e-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ee38e-110">Property value</span></span>

<span data-ttu-id="ee38e-111">O objeto [**OID**](oid.md) no índice especificado ou o objeto **OID** com o valor pontilhado especificado.</span><span class="sxs-lookup"><span data-stu-id="ee38e-111">The [**OID**](oid.md) object at the specified index, or the **OID** object with the specified dotted value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee38e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee38e-112">Requirements</span></span>



| <span data-ttu-id="ee38e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee38e-113">Requirement</span></span> | <span data-ttu-id="ee38e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ee38e-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee38e-115">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ee38e-115">Redistributable</span></span><br/> | <span data-ttu-id="ee38e-116">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="ee38e-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ee38e-117">DLL</span><span class="sxs-lookup"><span data-stu-id="ee38e-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="ee38e-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee38e-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee38e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee38e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee38e-120">**OID**</span><span class="sxs-lookup"><span data-stu-id="ee38e-120">**OIDs**</span></span>](oids.md)
</dt> </dl>

 

 
