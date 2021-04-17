---
description: Recupera um objeto OID que identifica o objeto de modelo.
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Propriedade Template. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a8599ac999c7d6a3e3403d94ff2c6daf0eba48b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752738"
---
# <a name="templateoid-property"></a><span data-ttu-id="2f263-103">Propriedade Template. OID</span><span class="sxs-lookup"><span data-stu-id="2f263-103">Template.OID property</span></span>

<span data-ttu-id="2f263-104">\[A propriedade **OID** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2f263-104">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2f263-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para o modelo de certificado para recuperar o modelo de extensão de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="2f263-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="2f263-106">A propriedade **OID** recupera um objeto [**OID**](oid.md) que identifica o objeto de [**modelo**](template.md) .</span><span class="sxs-lookup"><span data-stu-id="2f263-106">The **OID** property retrieves an [**OID**](oid.md) object that identifies the [**Template**](template.md) object.</span></span>

<span data-ttu-id="2f263-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2f263-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f263-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f263-108">Syntax</span></span>


```VB
Template.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="2f263-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2f263-109">Property value</span></span>

<span data-ttu-id="2f263-110">Um objeto [**OID**](oid.md) que identifica o objeto de [**modelo**](template.md) .</span><span class="sxs-lookup"><span data-stu-id="2f263-110">An [**OID**](oid.md) object that identifies the [**Template**](template.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f263-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f263-111">Requirements</span></span>



| <span data-ttu-id="2f263-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f263-112">Requirement</span></span> | <span data-ttu-id="2f263-113">Valor</span><span class="sxs-lookup"><span data-stu-id="2f263-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f263-114">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2f263-114">Redistributable</span></span><br/> | <span data-ttu-id="2f263-115">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="2f263-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2f263-116">DLL</span><span class="sxs-lookup"><span data-stu-id="2f263-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="2f263-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f263-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f263-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f263-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f263-119">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="2f263-119">**Template**</span></span>](template.md)
</dt> </dl>

 

 
