---
description: Define ou recupera o valor do número de OID pontilhado do identificador.
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: OIDs. Propriedade Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d8c3c59cfd3eadfb8aec56c6814a2af6ce9ff900
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769278"
---
# <a name="oidvalue-property"></a><span data-ttu-id="ea21a-103">OIDs. Propriedade Value</span><span class="sxs-lookup"><span data-stu-id="ea21a-103">OID.Value property</span></span>

<span data-ttu-id="ea21a-104">\[A propriedade **Value** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="ea21a-104">\[The **Value** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ea21a-105">Em vez disso, use a [**classe Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="ea21a-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="ea21a-106">A propriedade **Value** define ou recupera o valor do número de OID pontilhado do identificador.</span><span class="sxs-lookup"><span data-stu-id="ea21a-106">The **Value** property sets or retrieves the value of the OID dotted number of the identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea21a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea21a-107">Syntax</span></span>


```VB
OID.Value As String
```



## <a name="property-value"></a><span data-ttu-id="ea21a-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ea21a-108">Property value</span></span>

<span data-ttu-id="ea21a-109">O valor do número de OID pontilhado do identificador.</span><span class="sxs-lookup"><span data-stu-id="ea21a-109">The value of the OID dotted number of the identifier.</span></span> <span data-ttu-id="ea21a-110">Para obter os valores possíveis, consulte Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="ea21a-110">For possible values, see Wincrypt.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea21a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea21a-111">Remarks</span></span>

<span data-ttu-id="ea21a-112">Se a propriedade **Value** for definida, a propriedade [**FriendlyName**](oid-friendlyname.md) será definida como o nome de exibição correspondente.</span><span class="sxs-lookup"><span data-stu-id="ea21a-112">If the **Value** property is set, the [**FriendlyName**](oid-friendlyname.md) property is set to the corresponding display name.</span></span> <span data-ttu-id="ea21a-113">Se a propriedade **FriendlyName** for definida, a propriedade **Value** será definida como o valor pontilhado correspondente.</span><span class="sxs-lookup"><span data-stu-id="ea21a-113">If the **FriendlyName** property is set, the **Value** property is set to the corresponding dotted value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea21a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea21a-114">Requirements</span></span>



| <span data-ttu-id="ea21a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea21a-115">Requirement</span></span> | <span data-ttu-id="ea21a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ea21a-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea21a-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ea21a-117">Redistributable</span></span><br/> | <span data-ttu-id="ea21a-118">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="ea21a-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ea21a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ea21a-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="ea21a-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea21a-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea21a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea21a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea21a-122">**OIDs**</span><span class="sxs-lookup"><span data-stu-id="ea21a-122">**OID**</span></span>](oid.md)
</dt> </dl>

 

 
