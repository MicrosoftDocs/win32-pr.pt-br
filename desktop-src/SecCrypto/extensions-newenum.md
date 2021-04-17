---
description: A \_ Propriedade NewEnum de extensões recupera uma interface IEnumVARIANT em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).
ms.assetid: 0e461683-bb48-4961-91ef-36af1c3f863e
title: Propriedade Extensions._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5b605241e8173b8a41779fa00b661a9e2f383ac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811796"
---
# <a name="extensions_newenum-property"></a><span data-ttu-id="c2506-104">Extensões. \_ Propriedade NewEnum</span><span class="sxs-lookup"><span data-stu-id="c2506-104">Extensions.\_NewEnum property</span></span>

<span data-ttu-id="c2506-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c2506-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c2506-106">Em vez disso, use a [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="c2506-106">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c2506-107">A propriedade **\_ NewEnum** recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="c2506-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="c2506-108">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="c2506-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2506-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2506-109">Syntax</span></span>


```VB
Extensions._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="c2506-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c2506-110">Property value</span></span>

<span data-ttu-id="c2506-111">Uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="c2506-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2506-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2506-112">Remarks</span></span>

<span data-ttu-id="c2506-113">Essa propriedade é usada automaticamente internamente quando você usa a `For Each In` construção em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="c2506-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2506-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2506-114">Requirements</span></span>



| <span data-ttu-id="c2506-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2506-115">Requirement</span></span> | <span data-ttu-id="c2506-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c2506-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2506-117">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c2506-117">End of client support</span></span><br/> | <span data-ttu-id="c2506-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2506-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c2506-119">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="c2506-119">End of server support</span></span><br/> | <span data-ttu-id="c2506-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2506-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c2506-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c2506-121">Redistributable</span></span><br/>       | <span data-ttu-id="c2506-122">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c2506-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c2506-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c2506-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c2506-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2506-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2506-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2506-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2506-126">**Extensões**</span><span class="sxs-lookup"><span data-stu-id="c2506-126">**Extensions**</span></span>](extensions.md)
</dt> </dl>

 

 
