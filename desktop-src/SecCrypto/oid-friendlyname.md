---
description: Define ou recupera o nome de exibição para o identificador.
ms.assetid: 53f84d0d-c189-4fd2-a383-29fd0d22de08
title: OIDs. Propriedade FriendlyName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.FriendlyName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1976980d1a22f4246f0ace686941cc4bcec87c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780913"
---
# <a name="oidfriendlyname-property"></a><span data-ttu-id="d9d64-103">OIDs. Propriedade FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d9d64-103">OID.FriendlyName property</span></span>

<span data-ttu-id="d9d64-104">\[A propriedade **FriendlyName** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="d9d64-104">\[The **FriendlyName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d9d64-105">Em vez disso, use a [**classe Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="d9d64-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="d9d64-106">A propriedade **FriendlyName** define ou recupera o nome de exibição para o identificador.</span><span class="sxs-lookup"><span data-stu-id="d9d64-106">The **FriendlyName** property sets or retrieves the display name for the identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9d64-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9d64-107">Syntax</span></span>


```VB
OID.FriendlyName As String
```



## <a name="property-value"></a><span data-ttu-id="d9d64-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d9d64-108">Property value</span></span>

<span data-ttu-id="d9d64-109">O nome de exibição para o [**OID**](oid.md).</span><span class="sxs-lookup"><span data-stu-id="d9d64-109">The display name for the [**OID**](oid.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d9d64-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9d64-110">Remarks</span></span>

<span data-ttu-id="d9d64-111">Se a propriedade **FriendlyName** for definida, a propriedade [**Value**](oid-value.md) será definida como o valor pontilhado correspondente.</span><span class="sxs-lookup"><span data-stu-id="d9d64-111">If the **FriendlyName** property is set, the [**Value**](oid-value.md) property is set to the corresponding dotted value.</span></span> <span data-ttu-id="d9d64-112">Se a propriedade **Value** for definida, a propriedade **FriendlyName** será definida como o nome de exibição correspondente.</span><span class="sxs-lookup"><span data-stu-id="d9d64-112">If the **Value** property is set, the **FriendlyName** property is set to the corresponding display name.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9d64-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9d64-113">Requirements</span></span>



| <span data-ttu-id="d9d64-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9d64-114">Requirement</span></span> | <span data-ttu-id="d9d64-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d9d64-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9d64-116">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d9d64-116">Redistributable</span></span><br/> | <span data-ttu-id="d9d64-117">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="d9d64-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d9d64-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d9d64-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="d9d64-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9d64-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9d64-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9d64-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9d64-121">**OIDs**</span><span class="sxs-lookup"><span data-stu-id="d9d64-121">**OID**</span></span>](oid.md)
</dt> </dl>

 

 
