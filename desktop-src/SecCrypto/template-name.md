---
description: Recupera o nome do modelo.
ms.assetid: f92346bc-89b6-4063-aa66-85e2fb88d67d
title: Propriedade Template.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 005a9cc961b1d7be0ebda0b8e76307b95d92a6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780462"
---
# <a name="templatename-property"></a><span data-ttu-id="0f069-103">Propriedade Template.Name</span><span class="sxs-lookup"><span data-stu-id="0f069-103">Template.Name property</span></span>

<span data-ttu-id="0f069-104">\[A propriedade **Name** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="0f069-104">\[The **Name** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0f069-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para o modelo de certificado para recuperar o modelo de extensão de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="0f069-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="0f069-106">A propriedade **Name** recupera o nome do modelo.</span><span class="sxs-lookup"><span data-stu-id="0f069-106">The **Name** property retrieves the name of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f069-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f069-107">Syntax</span></span>


```VB
Template.Name As String
```



## <a name="property-value"></a><span data-ttu-id="0f069-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0f069-108">Property value</span></span>

<span data-ttu-id="0f069-109">O nome do modelo.</span><span class="sxs-lookup"><span data-stu-id="0f069-109">The name of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f069-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f069-110">Requirements</span></span>



| <span data-ttu-id="0f069-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f069-111">Requirement</span></span> | <span data-ttu-id="0f069-112">Valor</span><span class="sxs-lookup"><span data-stu-id="0f069-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f069-113">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="0f069-113">Redistributable</span></span><br/> | <span data-ttu-id="0f069-114">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="0f069-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0f069-115">DLL</span><span class="sxs-lookup"><span data-stu-id="0f069-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="0f069-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f069-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f069-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f069-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f069-118">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="0f069-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
