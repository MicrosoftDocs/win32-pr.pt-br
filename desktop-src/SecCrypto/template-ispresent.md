---
description: Recupera um valor booliano que indica se a extensão do modelo está presente.
ms.assetid: cc7f9853-8212-470d-b372-43a4bbd517f7
title: Propriedade Template. IsPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23dcd8cc5ee92a689300078d439998e43933af93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751311"
---
# <a name="templateispresent-property"></a><span data-ttu-id="b8cda-103">Propriedade Template. IsPresent</span><span class="sxs-lookup"><span data-stu-id="b8cda-103">Template.IsPresent property</span></span>

<span data-ttu-id="b8cda-104">\[A propriedade **IsPresent** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b8cda-104">\[The **IsPresent** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b8cda-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para o modelo de certificado para recuperar o modelo de extensão de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="b8cda-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="b8cda-106">A propriedade **IsPresent** recupera um valor booliano que indica se a extensão do modelo está presente.</span><span class="sxs-lookup"><span data-stu-id="b8cda-106">The **IsPresent** property retrieves a Boolean value that indicates whether the template extension is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8cda-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8cda-107">Syntax</span></span>


```VB
Template.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="b8cda-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b8cda-108">Property value</span></span>

<span data-ttu-id="b8cda-109">Se for **true**, a extensão do modelo estará presente.</span><span class="sxs-lookup"><span data-stu-id="b8cda-109">If **true**, the template extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8cda-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8cda-110">Requirements</span></span>



| <span data-ttu-id="b8cda-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8cda-111">Requirement</span></span> | <span data-ttu-id="b8cda-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b8cda-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8cda-113">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="b8cda-113">Redistributable</span></span><br/> | <span data-ttu-id="b8cda-114">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="b8cda-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b8cda-115">DLL</span><span class="sxs-lookup"><span data-stu-id="b8cda-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="b8cda-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8cda-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8cda-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8cda-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8cda-118">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="b8cda-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
