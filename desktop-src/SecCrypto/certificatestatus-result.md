---
description: A propriedade Result recupera um valor que indica se o certificado é válido. Essa é a propriedade padrão.
ms.assetid: b1edfbde-9d54-4e9c-ba9b-33e4c354c23f
title: Propriedade CertificateStatus. Result
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Result
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df13e9a9fb0454d30ce855b3d272fa521e96e0f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755313"
---
# <a name="certificatestatusresult-property"></a><span data-ttu-id="533eb-104">Propriedade CertificateStatus. Result</span><span class="sxs-lookup"><span data-stu-id="533eb-104">CertificateStatus.Result property</span></span>

<span data-ttu-id="533eb-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="533eb-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="533eb-106">Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="533eb-106">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="533eb-107">A propriedade **Result** recupera um valor que indica se o certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="533eb-107">The **Result** property retrieves a value that indicates whether the certificate is valid.</span></span> <span data-ttu-id="533eb-108">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="533eb-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="533eb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="533eb-109">Syntax</span></span>


```VB
CertificateStatus.Result As Boolean
```



## <a name="property-value"></a><span data-ttu-id="533eb-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="533eb-110">Property value</span></span>

<span data-ttu-id="533eb-111">Se **for true**, o certificado será válido.</span><span class="sxs-lookup"><span data-stu-id="533eb-111">If **true**, the certificate is valid.</span></span> <span data-ttu-id="533eb-112">A validade do certificado é verificada usando a configuração atual da propriedade [**CheckFlag**](certificatestatus-checkflag.md) e as várias configurações de política.</span><span class="sxs-lookup"><span data-stu-id="533eb-112">The certificate's validity is checked using the current setting of the [**CheckFlag**](certificatestatus-checkflag.md) property and the various policy settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="533eb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="533eb-113">Requirements</span></span>



| <span data-ttu-id="533eb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="533eb-114">Requirement</span></span> | <span data-ttu-id="533eb-115">Valor</span><span class="sxs-lookup"><span data-stu-id="533eb-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="533eb-116">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="533eb-116">End of client support</span></span><br/> | <span data-ttu-id="533eb-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="533eb-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="533eb-118">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="533eb-118">End of server support</span></span><br/> | <span data-ttu-id="533eb-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="533eb-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="533eb-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="533eb-120">Redistributable</span></span><br/>       | <span data-ttu-id="533eb-121">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="533eb-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="533eb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="533eb-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="533eb-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="533eb-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
