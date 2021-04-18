---
description: Recupera o conteúdo do aviso do usuário.
ms.assetid: dcf73357-253d-4160-be4e-f826296f5eaa
title: Propriedade Qualifier. ExplicitText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.ExplicitText
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d2ba5e6bbf6bb46e28c5dbb6fa9754c72b66dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792672"
---
# <a name="qualifierexplicittext-property"></a><span data-ttu-id="31096-103">Propriedade Qualifier. ExplicitText</span><span class="sxs-lookup"><span data-stu-id="31096-103">Qualifier.ExplicitText property</span></span>

<span data-ttu-id="31096-104">\[A propriedade **ExplicitText** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="31096-104">\[The **ExplicitText** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="31096-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="31096-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="31096-106">A propriedade **ExplicitText** recupera o conteúdo do aviso do usuário.</span><span class="sxs-lookup"><span data-stu-id="31096-106">The **ExplicitText** property retrieves the content of the user notice.</span></span> <span data-ttu-id="31096-107">Esta propriedade pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="31096-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="31096-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="31096-108">Syntax</span></span>


```VB
Qualifier.ExplicitText As String
```



## <a name="property-value"></a><span data-ttu-id="31096-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="31096-109">Property value</span></span>

<span data-ttu-id="31096-110">O conteúdo do aviso do usuário.</span><span class="sxs-lookup"><span data-stu-id="31096-110">The content of the user notice.</span></span>

## <a name="requirements"></a><span data-ttu-id="31096-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31096-111">Requirements</span></span>



| <span data-ttu-id="31096-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="31096-112">Requirement</span></span> | <span data-ttu-id="31096-113">Valor</span><span class="sxs-lookup"><span data-stu-id="31096-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31096-114">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="31096-114">Redistributable</span></span><br/> | <span data-ttu-id="31096-115">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="31096-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="31096-116">DLL</span><span class="sxs-lookup"><span data-stu-id="31096-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="31096-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31096-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31096-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="31096-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31096-119">**Qualificador**</span><span class="sxs-lookup"><span data-stu-id="31096-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
