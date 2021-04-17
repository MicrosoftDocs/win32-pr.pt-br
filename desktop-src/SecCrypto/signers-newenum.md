---
description: A \_ Propriedade NewEnum de assinantes recupera uma interface IEnumVARIANT em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).
ms.assetid: 99d7ddd3-a552-4125-b220-d1b28f20d1ed
title: Propriedade Signers._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 91007e7ce282cb44267927f54ab26f8f930028f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811786"
---
# <a name="signers_newenum-property"></a><span data-ttu-id="40ecf-104">Assinantes. \_ Propriedade NewEnum</span><span class="sxs-lookup"><span data-stu-id="40ecf-104">Signers.\_NewEnum property</span></span>

<span data-ttu-id="40ecf-105">\[A propriedade **\_ NewEnum** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="40ecf-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="40ecf-106">Em vez disso, use uma coleção de objetos CmsSigner.</span><span class="sxs-lookup"><span data-stu-id="40ecf-106">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="40ecf-107">Para obter mais informações, consulte a [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="40ecf-107">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="40ecf-108">A propriedade **\_ NewEnum** recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="40ecf-108">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="40ecf-109">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="40ecf-109">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="40ecf-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="40ecf-110">Syntax</span></span>


```VB
Signers._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="40ecf-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="40ecf-111">Property value</span></span>

<span data-ttu-id="40ecf-112">Uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="40ecf-112">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="40ecf-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="40ecf-113">Remarks</span></span>

<span data-ttu-id="40ecf-114">Essa propriedade é usada automaticamente internamente quando você usa a `For Each In` construção em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="40ecf-114">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="40ecf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40ecf-115">Requirements</span></span>



| <span data-ttu-id="40ecf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="40ecf-116">Requirement</span></span> | <span data-ttu-id="40ecf-117">Valor</span><span class="sxs-lookup"><span data-stu-id="40ecf-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40ecf-118">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="40ecf-118">Redistributable</span></span><br/> | <span data-ttu-id="40ecf-119">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="40ecf-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="40ecf-120">DLL</span><span class="sxs-lookup"><span data-stu-id="40ecf-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="40ecf-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40ecf-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40ecf-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="40ecf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40ecf-123">**Signatários**</span><span class="sxs-lookup"><span data-stu-id="40ecf-123">**Signers**</span></span>](signers.md)
</dt> </dl>

 

 
