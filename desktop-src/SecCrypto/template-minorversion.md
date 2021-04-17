---
description: Recupera o número de versão secundária do modelo.
ms.assetid: 3fc51d43-9113-4b4b-88ab-27cf6e5c4fa0
title: Propriedade Template. MinorVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MinorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a1de0beb41cbe87ca86b443c5cc2145c2058073
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749881"
---
# <a name="templateminorversion-property"></a><span data-ttu-id="ee49f-103">Propriedade Template. MinorVersion</span><span class="sxs-lookup"><span data-stu-id="ee49f-103">Template.MinorVersion property</span></span>

<span data-ttu-id="ee49f-104">\[A propriedade **MinorVersion** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="ee49f-104">\[The **MinorVersion** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ee49f-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para o modelo de certificado para recuperar o modelo de extensão de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="ee49f-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="ee49f-106">A propriedade **MinorVersion** recupera o número de versão secundária do modelo.</span><span class="sxs-lookup"><span data-stu-id="ee49f-106">The **MinorVersion** property retrieves the minor version number of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee49f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee49f-107">Syntax</span></span>


```VB
Template.MinorVersion As Long
```



## <a name="property-value"></a><span data-ttu-id="ee49f-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ee49f-108">Property value</span></span>

<span data-ttu-id="ee49f-109">O número de versão secundária do modelo.</span><span class="sxs-lookup"><span data-stu-id="ee49f-109">The minor version number of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee49f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee49f-110">Requirements</span></span>



| <span data-ttu-id="ee49f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee49f-111">Requirement</span></span> | <span data-ttu-id="ee49f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ee49f-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee49f-113">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ee49f-113">Redistributable</span></span><br/> | <span data-ttu-id="ee49f-114">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="ee49f-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ee49f-115">DLL</span><span class="sxs-lookup"><span data-stu-id="ee49f-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="ee49f-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee49f-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee49f-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee49f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee49f-118">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="ee49f-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
