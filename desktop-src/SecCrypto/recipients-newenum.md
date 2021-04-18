---
description: A \_ Propriedade NewEnum de Recipients recupera uma interface IEnumVARIANT em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).
ms.assetid: affdc695-b78c-48b5-b66d-5f94e1a86ff2
title: Propriedade Recipients._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a4a1e7db31ceead23509604edddee05ec64380ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758908"
---
# <a name="recipients_newenum-property"></a><span data-ttu-id="fcc72-104">Destinatários. \_ Propriedade NewEnum</span><span class="sxs-lookup"><span data-stu-id="fcc72-104">Recipients.\_NewEnum property</span></span>

<span data-ttu-id="fcc72-105">\[A propriedade **\_ NewEnum** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="fcc72-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fcc72-106">Em vez disso, use a [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="fcc72-106">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="fcc72-107">A propriedade **\_ NewEnum** recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="fcc72-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="fcc72-108">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="fcc72-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="fcc72-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcc72-109">Syntax</span></span>


```VB
Recipients._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="fcc72-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fcc72-110">Property value</span></span>

<span data-ttu-id="fcc72-111">Uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="fcc72-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcc72-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcc72-112">Remarks</span></span>

<span data-ttu-id="fcc72-113">Essa propriedade é usada automaticamente internamente quando você usa a `For Each In` construção em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="fcc72-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcc72-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcc72-114">Requirements</span></span>



| <span data-ttu-id="fcc72-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcc72-115">Requirement</span></span> | <span data-ttu-id="fcc72-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fcc72-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc72-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="fcc72-117">Redistributable</span></span><br/> | <span data-ttu-id="fcc72-118">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="fcc72-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fcc72-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fcc72-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="fcc72-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcc72-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcc72-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcc72-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcc72-122">**Destinatários**</span><span class="sxs-lookup"><span data-stu-id="fcc72-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
