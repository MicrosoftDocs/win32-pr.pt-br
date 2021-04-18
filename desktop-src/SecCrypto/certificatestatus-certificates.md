---
description: Define ou recupera a coleção de certificados que podem ser usados para criar a cadeia de certificados.
ms.assetid: cdf378f9-0d71-4dd9-93cc-85f09a51c5fc
title: Propriedade CertificateStatus. Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 325b5c45fc6ae626363de286a6e131f1782cb83f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756154"
---
# <a name="certificatestatuscertificates-property"></a><span data-ttu-id="8940d-103">Propriedade CertificateStatus. Certificates</span><span class="sxs-lookup"><span data-stu-id="8940d-103">CertificateStatus.Certificates property</span></span>

<span data-ttu-id="8940d-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8940d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8940d-105">Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="8940d-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="8940d-106">A propriedade **Certificates** define ou recupera a coleção de certificados que pode ser usada para criar a cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="8940d-106">The **Certificates** property sets or retrieves the collection of certificates that can be used to build the certificate chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="8940d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8940d-107">Syntax</span></span>


```VB
CertificateStatus.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="8940d-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8940d-108">Property value</span></span>

<span data-ttu-id="8940d-109">Um objeto de [**certificados**](certificates.md) que representa a coleção de certificados que podem ser usados para criar a cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="8940d-109">A [**Certificates**](certificates.md) object that represents the collection of certificates that can be used to build the certificate chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="8940d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8940d-110">Requirements</span></span>



| <span data-ttu-id="8940d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="8940d-111">Requirement</span></span> | <span data-ttu-id="8940d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="8940d-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8940d-113">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8940d-113">End of client support</span></span><br/> | <span data-ttu-id="8940d-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8940d-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8940d-115">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="8940d-115">End of server support</span></span><br/> | <span data-ttu-id="8940d-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8940d-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8940d-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="8940d-117">Redistributable</span></span><br/>       | <span data-ttu-id="8940d-118">CAPICOM 2,1 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="8940d-118">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8940d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="8940d-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8940d-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8940d-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
