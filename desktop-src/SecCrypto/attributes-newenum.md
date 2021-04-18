---
description: A \_ Propriedade NewEnum de atributos recupera uma interface IEnumVARIANT em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).
ms.assetid: a90ef28b-3926-4542-bcd2-27f0eda4e339
title: Propriedade Attributes._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9948c55943a8374665fe5e4883013742188665c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757480"
---
# <a name="attributes_newenum-property"></a><span data-ttu-id="52bfe-104">Atributos. \_ Propriedade NewEnum</span><span class="sxs-lookup"><span data-stu-id="52bfe-104">Attributes.\_NewEnum property</span></span>

<span data-ttu-id="52bfe-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="52bfe-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="52bfe-106">Em vez disso, use a [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="52bfe-106">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="52bfe-107">A propriedade **\_ NewEnum** recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="52bfe-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="52bfe-108">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="52bfe-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="52bfe-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="52bfe-109">Syntax</span></span>


```VB
Attributes._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="52bfe-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="52bfe-110">Property value</span></span>

<span data-ttu-id="52bfe-111">Uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="52bfe-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="52bfe-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="52bfe-112">Remarks</span></span>

<span data-ttu-id="52bfe-113">Essa propriedade é usada automaticamente internamente quando você usa a `For Each In` construção em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="52bfe-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="52bfe-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52bfe-114">Requirements</span></span>



| <span data-ttu-id="52bfe-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="52bfe-115">Requirement</span></span> | <span data-ttu-id="52bfe-116">Valor</span><span class="sxs-lookup"><span data-stu-id="52bfe-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52bfe-117">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="52bfe-117">End of client support</span></span><br/> | <span data-ttu-id="52bfe-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52bfe-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="52bfe-119">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="52bfe-119">End of server support</span></span><br/> | <span data-ttu-id="52bfe-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52bfe-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="52bfe-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="52bfe-121">Redistributable</span></span><br/>       | <span data-ttu-id="52bfe-122">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="52bfe-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="52bfe-123">DLL</span><span class="sxs-lookup"><span data-stu-id="52bfe-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="52bfe-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52bfe-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52bfe-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="52bfe-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52bfe-126">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="52bfe-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
