---
description: Recupera a ID de objeto do qualificador.
ms.assetid: 58ec2af7-f085-43bc-8ea8-926cb840abe9
title: Propriedade Qualifier. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a86aaf7b60b98811e2d1fbef79c520448f1d47f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758001"
---
# <a name="qualifieroid-property"></a><span data-ttu-id="f23f5-103">Propriedade Qualifier. OID</span><span class="sxs-lookup"><span data-stu-id="f23f5-103">Qualifier.OID property</span></span>

<span data-ttu-id="f23f5-104">\[A propriedade **OID** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="f23f5-104">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f23f5-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="f23f5-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="f23f5-106">A propriedade **OID** recupera a ID de objeto do qualificador.</span><span class="sxs-lookup"><span data-stu-id="f23f5-106">The **OID** property retrieves the object ID of the qualifier.</span></span> <span data-ttu-id="f23f5-107">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="f23f5-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f23f5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f23f5-108">Syntax</span></span>


```VB
Qualifier.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="f23f5-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f23f5-109">Property value</span></span>

<span data-ttu-id="f23f5-110">Um objeto [**OID**](oid.md) que identifica o qualificador.</span><span class="sxs-lookup"><span data-stu-id="f23f5-110">An [**OID**](oid.md) object that identifies the qualifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="f23f5-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f23f5-111">Requirements</span></span>



| <span data-ttu-id="f23f5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f23f5-112">Requirement</span></span> | <span data-ttu-id="f23f5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f23f5-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f23f5-114">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f23f5-114">Redistributable</span></span><br/> | <span data-ttu-id="f23f5-115">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="f23f5-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f23f5-116">DLL</span><span class="sxs-lookup"><span data-stu-id="f23f5-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="f23f5-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f23f5-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f23f5-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="f23f5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f23f5-119">**Qualificador**</span><span class="sxs-lookup"><span data-stu-id="f23f5-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
