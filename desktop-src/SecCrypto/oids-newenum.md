---
description: A \_ Propriedade NewEnum de OIDs recupera uma interface IEnumVARIANT em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).
ms.assetid: 7c09fd11-064b-451e-bd6b-e6c13ab228a0
title: Propriedade OIDs._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d20856c17dda18a10b85c01453cbe043144742d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758006"
---
# <a name="oids_newenum-property"></a><span data-ttu-id="2f7ff-104">OIDs. \_ Propriedade NewEnum</span><span class="sxs-lookup"><span data-stu-id="2f7ff-104">OIDs.\_NewEnum property</span></span>

<span data-ttu-id="2f7ff-105">\[A propriedade **\_ NewEnum** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2f7ff-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2f7ff-106">Em vez disso, use a [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="2f7ff-106">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="2f7ff-107">A propriedade **\_ NewEnum** recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="2f7ff-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="2f7ff-108">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="2f7ff-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f7ff-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f7ff-109">Syntax</span></span>


```VB
OIDs._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="2f7ff-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2f7ff-110">Property value</span></span>

<span data-ttu-id="2f7ff-111">Uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="2f7ff-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f7ff-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f7ff-112">Remarks</span></span>

<span data-ttu-id="2f7ff-113">Essa propriedade é usada automaticamente internamente quando você usa a `For Each In` construção em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="2f7ff-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f7ff-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f7ff-114">Requirements</span></span>



| <span data-ttu-id="2f7ff-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f7ff-115">Requirement</span></span> | <span data-ttu-id="2f7ff-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2f7ff-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f7ff-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2f7ff-117">Redistributable</span></span><br/> | <span data-ttu-id="2f7ff-118">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="2f7ff-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2f7ff-119">DLL</span><span class="sxs-lookup"><span data-stu-id="2f7ff-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="2f7ff-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f7ff-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f7ff-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f7ff-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f7ff-122">**OID**</span><span class="sxs-lookup"><span data-stu-id="2f7ff-122">**OIDs**</span></span>](oids.md)
</dt> </dl>

 

 
