---
description: Recupera um valor booliano que indica se a extensão do modelo está marcada como crítica.
ms.assetid: 37e2000a-d3c8-46b5-84e5-a3904fdbaeea
title: Propriedade modelo. IsCritical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66f9dc90828cd474497478872f154adbd3fcd12a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751924"
---
# <a name="templateiscritical-property"></a><span data-ttu-id="8bfcc-103">Propriedade modelo. IsCritical</span><span class="sxs-lookup"><span data-stu-id="8bfcc-103">Template.IsCritical property</span></span>

<span data-ttu-id="8bfcc-104">\[A propriedade **Iscriticad** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="8bfcc-104">\[The **IsCritical** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8bfcc-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para o modelo de certificado para recuperar o modelo de extensão de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="8bfcc-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="8bfcc-106">A propriedade **Iscriticat** recupera um valor booliano que indica se a extensão do modelo está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="8bfcc-106">The **IsCritical** property retrieves a Boolean value that indicates whether the template extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bfcc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bfcc-107">Syntax</span></span>


```VB
Template.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="8bfcc-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8bfcc-108">Property value</span></span>

<span data-ttu-id="8bfcc-109">Se **for true**, a extensão do modelo será marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="8bfcc-109">If **true**, the template extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bfcc-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bfcc-110">Requirements</span></span>



| <span data-ttu-id="8bfcc-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bfcc-111">Requirement</span></span> | <span data-ttu-id="8bfcc-112">Valor</span><span class="sxs-lookup"><span data-stu-id="8bfcc-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bfcc-113">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="8bfcc-113">Redistributable</span></span><br/> | <span data-ttu-id="8bfcc-114">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="8bfcc-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8bfcc-115">DLL</span><span class="sxs-lookup"><span data-stu-id="8bfcc-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="8bfcc-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bfcc-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bfcc-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="8bfcc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bfcc-118">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="8bfcc-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
