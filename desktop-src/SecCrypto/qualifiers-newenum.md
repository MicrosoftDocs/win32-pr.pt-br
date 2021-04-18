---
description: A \_ Propriedade NewEnum de qualificadores recupera uma interface IEnumVARIANT em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).
ms.assetid: e51f8ca1-ef1f-475b-8368-e8296fae0f04
title: Propriedade Qualifiers._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 01a4d62604dabacd2d78d5d2f6cbee0db7189196
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810509"
---
# <a name="qualifiers_newenum-property"></a><span data-ttu-id="c6812-104">Qualificadores. \_ Propriedade NewEnum</span><span class="sxs-lookup"><span data-stu-id="c6812-104">Qualifiers.\_NewEnum property</span></span>

<span data-ttu-id="c6812-105">\[A propriedade **\_ NewEnum** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="c6812-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c6812-106">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="c6812-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="c6812-107">A propriedade **\_ NewEnum** recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="c6812-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="c6812-108">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="c6812-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="c6812-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6812-109">Syntax</span></span>


```VB
Qualifiers._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="c6812-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c6812-110">Property value</span></span>

<span data-ttu-id="c6812-111">Uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="c6812-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6812-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6812-112">Remarks</span></span>

<span data-ttu-id="c6812-113">Essa propriedade é usada automaticamente internamente quando você usa a `For Each In` construção em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="c6812-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6812-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6812-114">Requirements</span></span>



| <span data-ttu-id="c6812-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6812-115">Requirement</span></span> | <span data-ttu-id="c6812-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c6812-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6812-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c6812-117">Redistributable</span></span><br/> | <span data-ttu-id="c6812-118">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c6812-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c6812-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c6812-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="c6812-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6812-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6812-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6812-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6812-122">**Qualificadores**</span><span class="sxs-lookup"><span data-stu-id="c6812-122">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
