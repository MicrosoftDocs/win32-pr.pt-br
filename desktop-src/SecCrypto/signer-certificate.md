---
description: Define ou recupera o objeto de certificado que representa o certificado de um signatário dos dados.
ms.assetid: 92ac209e-59b5-4a75-922d-d61629ca41b1
title: Propriedade signatário. Certificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 96652f85e6058682dedd3370965ea7ff2408b3b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811048"
---
# <a name="signercertificate-property"></a><span data-ttu-id="a571c-103">Propriedade signatário. Certificate</span><span class="sxs-lookup"><span data-stu-id="a571c-103">Signer.Certificate property</span></span>

<span data-ttu-id="a571c-104">\[A propriedade de **certificado** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="a571c-104">\[The **Certificate** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a571c-105">Em vez disso, use a [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="a571c-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="a571c-106">A propriedade de **certificado** define ou recupera o objeto de [**certificado**](certificate.md) que representa o certificado de um signatário dos dados.</span><span class="sxs-lookup"><span data-stu-id="a571c-106">The **Certificate** property sets or retrieves the [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span> <span data-ttu-id="a571c-107">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="a571c-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a571c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a571c-108">Syntax</span></span>


```VB
Signer.Certificate As Certificate
```



## <a name="property-value"></a><span data-ttu-id="a571c-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a571c-109">Property value</span></span>

<span data-ttu-id="a571c-110">O objeto de [**certificado**](certificate.md) que representa o certificado de um signatário dos dados.</span><span class="sxs-lookup"><span data-stu-id="a571c-110">The [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span>

## <a name="remarks"></a><span data-ttu-id="a571c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a571c-111">Remarks</span></span>

<span data-ttu-id="a571c-112">Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido.</span><span class="sxs-lookup"><span data-stu-id="a571c-112">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="a571c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a571c-113">Requirements</span></span>



| <span data-ttu-id="a571c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a571c-114">Requirement</span></span> | <span data-ttu-id="a571c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a571c-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a571c-116">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a571c-116">Redistributable</span></span><br/> | <span data-ttu-id="a571c-117">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="a571c-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a571c-118">DLL</span><span class="sxs-lookup"><span data-stu-id="a571c-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="a571c-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a571c-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a571c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="a571c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a571c-121">**Signatário**</span><span class="sxs-lookup"><span data-stu-id="a571c-121">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
