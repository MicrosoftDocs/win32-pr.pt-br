---
description: Recupera o nome da organização associada ao qualificador.
ms.assetid: 4ceb2c0f-903d-4fcd-8446-abf3175fe8e0
title: Propriedade Qualifier. OrganizationName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OrganizationName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1e1ebb2b948d5a933b59e86c8753b6b68a3a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747639"
---
# <a name="qualifierorganizationname-property"></a><span data-ttu-id="ccf42-103">Propriedade Qualifier. OrganizationName</span><span class="sxs-lookup"><span data-stu-id="ccf42-103">Qualifier.OrganizationName property</span></span>

<span data-ttu-id="ccf42-104">\[A propriedade **OrganizationName** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="ccf42-104">\[The **OrganizationName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ccf42-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="ccf42-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="ccf42-106">A propriedade **OrganizationName** recupera o nome da organização associada ao qualificador.</span><span class="sxs-lookup"><span data-stu-id="ccf42-106">The **OrganizationName** property retrieves the name of the organization associated with the qualifier.</span></span> <span data-ttu-id="ccf42-107">Esta propriedade pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="ccf42-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf42-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccf42-108">Syntax</span></span>


```VB
Qualifier.OrganizationName As String
```



## <a name="property-value"></a><span data-ttu-id="ccf42-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ccf42-109">Property value</span></span>

<span data-ttu-id="ccf42-110">O nome da organização associada ao qualificador.</span><span class="sxs-lookup"><span data-stu-id="ccf42-110">The name of the organization associated with the qualifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf42-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccf42-111">Requirements</span></span>



| <span data-ttu-id="ccf42-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccf42-112">Requirement</span></span> | <span data-ttu-id="ccf42-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ccf42-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf42-114">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ccf42-114">Redistributable</span></span><br/> | <span data-ttu-id="ccf42-115">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="ccf42-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ccf42-116">DLL</span><span class="sxs-lookup"><span data-stu-id="ccf42-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="ccf42-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccf42-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccf42-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccf42-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf42-119">**Qualificador**</span><span class="sxs-lookup"><span data-stu-id="ccf42-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
