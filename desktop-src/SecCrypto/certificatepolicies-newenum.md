---
description: A \_ Propriedade NewEnum de CertificatePolicies recupera uma interface IEnumVARIANT em um objeto que pode ser usado para enumerar a coleção.
ms.assetid: 631a11c8-4442-493e-9406-bc63f79db548
title: Propriedade CertificatePolicies._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2d5e90d4b906661119936ca1e893e3b6e17c9bf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800087"
---
# <a name="certificatepolicies_newenum-property"></a><span data-ttu-id="117b7-103">CertificatePolicies. \_ Propriedade NewEnum</span><span class="sxs-lookup"><span data-stu-id="117b7-103">CertificatePolicies.\_NewEnum property</span></span>

<span data-ttu-id="117b7-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="117b7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="117b7-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para as políticas de certificado para recuperar as políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="117b7-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="117b7-106">A propriedade **\_ NewEnum** recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="117b7-106">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="117b7-107">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="117b7-107">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="117b7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="117b7-108">Syntax</span></span>


```VB
CertificatePolicies._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="117b7-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="117b7-109">Property value</span></span>

<span data-ttu-id="117b7-110">Uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="117b7-110">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="117b7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="117b7-111">Remarks</span></span>

<span data-ttu-id="117b7-112">Essa propriedade é usada automaticamente internamente quando você usa a `For Each In` construção em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="117b7-112">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="117b7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="117b7-113">Requirements</span></span>



| <span data-ttu-id="117b7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="117b7-114">Requirement</span></span> | <span data-ttu-id="117b7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="117b7-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="117b7-116">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="117b7-116">End of client support</span></span><br/> | <span data-ttu-id="117b7-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="117b7-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="117b7-118">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="117b7-118">End of server support</span></span><br/> | <span data-ttu-id="117b7-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="117b7-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="117b7-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="117b7-120">Redistributable</span></span><br/>       | <span data-ttu-id="117b7-121">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="117b7-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="117b7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="117b7-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="117b7-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="117b7-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
