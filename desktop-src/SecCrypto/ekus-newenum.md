---
description: A \_ Propriedade NewEnum de EKUs recupera uma interface IEnumVARIANT em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).
ms.assetid: c7d038c0-416f-47f7-94ba-74ca877da7ba
title: Propriedade EKUs._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 72605e0ad7bbb8671ff9a5885a79f1d7836c6efb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752128"
---
# <a name="ekus_newenum-property"></a><span data-ttu-id="96661-104">EKUs. \_ Propriedade NewEnum</span><span class="sxs-lookup"><span data-stu-id="96661-104">EKUs.\_NewEnum property</span></span>

<span data-ttu-id="96661-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="96661-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="96661-106">Em vez disso, use a [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="96661-106">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="96661-107">A propriedade **\_ NewEnum** recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="96661-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="96661-108">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="96661-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="96661-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="96661-109">Syntax</span></span>


```VB
EKUs._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="96661-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="96661-110">Property value</span></span>

<span data-ttu-id="96661-111">Uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="96661-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="96661-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="96661-112">Remarks</span></span>

<span data-ttu-id="96661-113">Essa propriedade é usada automaticamente internamente quando você usa a `For Each In` construção em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="96661-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="96661-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96661-114">Requirements</span></span>



| <span data-ttu-id="96661-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="96661-115">Requirement</span></span> | <span data-ttu-id="96661-116">Valor</span><span class="sxs-lookup"><span data-stu-id="96661-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96661-117">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="96661-117">End of client support</span></span><br/> | <span data-ttu-id="96661-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96661-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="96661-119">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="96661-119">End of server support</span></span><br/> | <span data-ttu-id="96661-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96661-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="96661-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="96661-121">Redistributable</span></span><br/>       | <span data-ttu-id="96661-122">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="96661-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="96661-123">DLL</span><span class="sxs-lookup"><span data-stu-id="96661-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="96661-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96661-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96661-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="96661-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96661-126">**EKUs**</span><span class="sxs-lookup"><span data-stu-id="96661-126">**EKUs**</span></span>](ekus.md)
</dt> </dl>

 

 
