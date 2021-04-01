---
description: As interfaces a seguir podem ser usadas para criar solicitações de certificado.
ms.assetid: 6021db79-ac90-4e0c-afbd-0f926abcab78
title: Interfaces de solicitação de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e18a4f8e1ce60348ffdf52afe210247f6d20a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090742"
---
# <a name="certificate-request-interfaces"></a><span data-ttu-id="7988f-103">Interfaces de solicitação de certificado</span><span class="sxs-lookup"><span data-stu-id="7988f-103">Certificate Request Interfaces</span></span>

<span data-ttu-id="7988f-104">As interfaces a seguir podem ser usadas para criar solicitações de certificado.</span><span class="sxs-lookup"><span data-stu-id="7988f-104">The following interfaces can be used to create certificate requests.</span></span>



| <span data-ttu-id="7988f-105">Interface</span><span class="sxs-lookup"><span data-stu-id="7988f-105">Interface</span></span>                                                                          | <span data-ttu-id="7988f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="7988f-106">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7988f-107">**IX509CertificateRequest**</span><span class="sxs-lookup"><span data-stu-id="7988f-107">**IX509CertificateRequest**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                         | <span data-ttu-id="7988f-108">Representa a interface de nível superior abstrata para uma solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="7988f-108">Represents the abstract top-level interface for a certificate request.</span></span>                                                                                        |
| [<span data-ttu-id="7988f-109">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="7988f-109">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)   | <span data-ttu-id="7988f-110">Permite que você crie certificados diretamente sem passar por um registro ou autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="7988f-110">Enables you to create certificates directly without going through a registration or certification authority.</span></span>                                                  |
| [<span data-ttu-id="7988f-111">**IX509CertificateRequestCertificate2**</span><span class="sxs-lookup"><span data-stu-id="7988f-111">**IX509CertificateRequestCertificate2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcertificate2) | <span data-ttu-id="7988f-112">Estende a interface [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) para habilitar a inicialização a partir de um modelo.</span><span class="sxs-lookup"><span data-stu-id="7988f-112">Extends the [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) interface to enable initialization from a template.</span></span>              |
| [<span data-ttu-id="7988f-113">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="7988f-113">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                   | <span data-ttu-id="7988f-114">Representa uma solicitação CMC.</span><span class="sxs-lookup"><span data-stu-id="7988f-114">Represents a CMC request.</span></span>                                                                                                                                     |
| [<span data-ttu-id="7988f-115">**IX509CertificateRequestCmc2**</span><span class="sxs-lookup"><span data-stu-id="7988f-115">**IX509CertificateRequestCmc2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcmc2)                 | <span data-ttu-id="7988f-116">Estende a interface [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) para habilitar a inicialização a partir de um modelo.</span><span class="sxs-lookup"><span data-stu-id="7988f-116">Extends the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) interface to enable initialization from a template.</span></span>                              |
| [<span data-ttu-id="7988f-117">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="7988f-117">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)             | <span data-ttu-id="7988f-118">Representa uma \# solicitação PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="7988f-118">Represents a PKCS \#10 request.</span></span>                                                                                                                               |
| [<span data-ttu-id="7988f-119">**IX509CertificateRequestPkcs10V2**</span><span class="sxs-lookup"><span data-stu-id="7988f-119">**IX509CertificateRequestPkcs10V2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v2)         | <span data-ttu-id="7988f-120">Estende a interface [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) para habilitar a inicialização a partir de um modelo.</span><span class="sxs-lookup"><span data-stu-id="7988f-120">Extends the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) interface to enable initialization from a template.</span></span>                        |
| [<span data-ttu-id="7988f-121">**IX509CertificateRequestPkcs10V3**</span><span class="sxs-lookup"><span data-stu-id="7988f-121">**IX509CertificateRequestPkcs10V3**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3)         | <span data-ttu-id="7988f-122">Estende a interface [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e adiciona propriedades que habilitam o atestado de certificado TPM.</span><span class="sxs-lookup"><span data-stu-id="7988f-122">Extends the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) interface and adds properties that enable TPM certificate attestation.</span></span> |
| [<span data-ttu-id="7988f-123">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="7988f-123">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               | <span data-ttu-id="7988f-124">Representa uma \# solicitação PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="7988f-124">Represents a PKCS \#7 request.</span></span>                                                                                                                                |
| [<span data-ttu-id="7988f-125">**IX509CertificateRequestPkcs7V2**</span><span class="sxs-lookup"><span data-stu-id="7988f-125">**IX509CertificateRequestPkcs7V2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs7v2)           | <span data-ttu-id="7988f-126">Estende a interface [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) para habilitar a inicialização a partir de um modelo.</span><span class="sxs-lookup"><span data-stu-id="7988f-126">Extends the [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) interface to enable initialization from a template.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="7988f-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7988f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7988f-128">Interfaces CertEnroll</span><span class="sxs-lookup"><span data-stu-id="7988f-128">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



