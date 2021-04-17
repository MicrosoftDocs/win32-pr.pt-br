---
description: Define ou recupera a hora em que o certificado foi verificado.
ms.assetid: 1bd17df3-2fa1-4b99-ab00-659b4ad5fcd9
title: Propriedade CertificateStatus. Verification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.VerificationTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 178402861c9830efbea78a31081ae7e8b31800b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760016"
---
# <a name="certificatestatusverificationtime-property"></a><span data-ttu-id="81505-103">Propriedade CertificateStatus. Verification</span><span class="sxs-lookup"><span data-stu-id="81505-103">CertificateStatus.VerificationTime property</span></span>

<span data-ttu-id="81505-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="81505-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="81505-105">Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="81505-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="81505-106">A propriedade **verificatime** define ou recupera a hora em que o certificado foi verificado.</span><span class="sxs-lookup"><span data-stu-id="81505-106">The **VerificationTime** property sets or retrieves the time that the certificate was verified.</span></span>

## <a name="syntax"></a><span data-ttu-id="81505-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="81505-107">Syntax</span></span>


```VB
CertificateStatus.VerificationTime As Date
```



## <a name="property-value"></a><span data-ttu-id="81505-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="81505-108">Property value</span></span>

<span data-ttu-id="81505-109">A hora em que o certificado foi verificado.</span><span class="sxs-lookup"><span data-stu-id="81505-109">The time that the certificate was verified.</span></span>

## <a name="remarks"></a><span data-ttu-id="81505-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="81505-110">Remarks</span></span>

<span data-ttu-id="81505-111">Se essa propriedade não for definida, a hora atual será usada.</span><span class="sxs-lookup"><span data-stu-id="81505-111">If this property is not set, the current time is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="81505-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81505-112">Requirements</span></span>



| <span data-ttu-id="81505-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="81505-113">Requirement</span></span> | <span data-ttu-id="81505-114">Valor</span><span class="sxs-lookup"><span data-stu-id="81505-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81505-115">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="81505-115">End of client support</span></span><br/> | <span data-ttu-id="81505-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81505-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="81505-117">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="81505-117">End of server support</span></span><br/> | <span data-ttu-id="81505-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81505-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="81505-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="81505-119">Redistributable</span></span><br/>       | <span data-ttu-id="81505-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="81505-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="81505-121">DLL</span><span class="sxs-lookup"><span data-stu-id="81505-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="81505-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81505-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
