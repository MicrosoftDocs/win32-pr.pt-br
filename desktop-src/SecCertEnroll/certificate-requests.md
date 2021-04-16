---
description: O SDK de registro de certificado pode ser usado para criar \# solicitações de certificado PKCS 10, PKCS \# 7, CMC e autoassinados.
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: Solicitações de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690f3a5117abfa0ae262f0a8fa38f68528abf02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758027"
---
# <a name="certificate-requests"></a><span data-ttu-id="a4fc9-103">Solicitações de certificado</span><span class="sxs-lookup"><span data-stu-id="a4fc9-103">Certificate Requests</span></span>

<span data-ttu-id="a4fc9-104">O SDK de registro de certificado pode ser usado para criar \# solicitações de certificado PKCS 10, PKCS \# 7, CMC e autoassinados.</span><span class="sxs-lookup"><span data-stu-id="a4fc9-104">The Certificate Enrollment SDK can be used to create PKCS \#10, PKCS \#7, CMC, and self-signed certificate requests.</span></span> <span data-ttu-id="a4fc9-105">Cada tipo de solicitação é representado por uma das interfaces listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4fc9-105">Each type of request is represented by one of the interfaces listed in the following table.</span></span> <span data-ttu-id="a4fc9-106">Todas as interfaces de solicitação herdam direta ou indiretamente da interface [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) .</span><span class="sxs-lookup"><span data-stu-id="a4fc9-106">All request interfaces inherit directly or indirectly from the [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) interface.</span></span> 

| <span data-ttu-id="a4fc9-107">Interface</span><span class="sxs-lookup"><span data-stu-id="a4fc9-107">Interface</span></span>                                                                        | <span data-ttu-id="a4fc9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4fc9-108">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4fc9-109">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="a4fc9-109">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | <span data-ttu-id="a4fc9-110">Representa uma \# solicitação PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="a4fc9-110">Represents a PKCS \#10 request.</span></span> <span data-ttu-id="a4fc9-111">Essa interface herda de [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span><span class="sxs-lookup"><span data-stu-id="a4fc9-111">This interface inherits from [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span></span>                   |
| [<span data-ttu-id="a4fc9-112">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="a4fc9-112">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | <span data-ttu-id="a4fc9-113">Representa uma \# solicitação PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="a4fc9-113">Represents a PKCS \#7 request.</span></span> <span data-ttu-id="a4fc9-114">Essa interface herda de [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span><span class="sxs-lookup"><span data-stu-id="a4fc9-114">This interface inherits from [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span></span>                    |
| [<span data-ttu-id="a4fc9-115">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="a4fc9-115">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | <span data-ttu-id="a4fc9-116">Representa um certificado autoassinado.</span><span class="sxs-lookup"><span data-stu-id="a4fc9-116">Represents a self-signed certificate.</span></span> <span data-ttu-id="a4fc9-117">Essa interface herda de [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10).</span><span class="sxs-lookup"><span data-stu-id="a4fc9-117">This interface inherits from [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10).</span></span> |
| [<span data-ttu-id="a4fc9-118">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="a4fc9-118">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | <span data-ttu-id="a4fc9-119">Representa uma solicitação CMC.</span><span class="sxs-lookup"><span data-stu-id="a4fc9-119">Represents a CMC request.</span></span> <span data-ttu-id="a4fc9-120">Essa interface herda de [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).</span><span class="sxs-lookup"><span data-stu-id="a4fc9-120">This interface inherits from [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).</span></span>               |



 

<span data-ttu-id="a4fc9-121">A ilustração a seguir mostra a estrutura de herança dos objetos de solicitação com suporte pela API de registro de certificado.</span><span class="sxs-lookup"><span data-stu-id="a4fc9-121">The following illustration shows the inheritance structure of the request objects supported by the Certificate Enrollment API.</span></span> <span data-ttu-id="a4fc9-122">Um objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) serve, direta ou indiretamente, como a classe base para todos os objetos de solicitação disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a4fc9-122">An [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) object serves, directly or indirectly, as the base class for all of the available request objects.</span></span>

![estrutura de herança para as interfaces de solicitação](images/certificate-request-inheritance.png)

<span data-ttu-id="a4fc9-124">Independentemente do tipo, uma solicitação de certificado contém informações sobre o assunto que faz a solicitação, a chave pública da entidade, um conjunto de atributos, um conjunto de extensões X. 509 versão 3 (que podem ser enviadas como parte dos atributos) e uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a4fc9-124">Regardless of type, a certificate request contains information about the subject making the request, the subject's public key, a set of attributes, a set of X.509 version 3 extensions (which may be submitted as part of the attributes), and a signature.</span></span> <span data-ttu-id="a4fc9-125">Esses problemas são abordados pelos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="a4fc9-125">These issues are addressed by the following topics:</span></span>

-   [<span data-ttu-id="a4fc9-126">Nomes de Entidades</span><span class="sxs-lookup"><span data-stu-id="a4fc9-126">Subject Names</span></span>](subject-names.md)
-   [<span data-ttu-id="a4fc9-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="a4fc9-127">Attributes</span></span>](attributes.md)
-   [<span data-ttu-id="a4fc9-128">Extensões</span><span class="sxs-lookup"><span data-stu-id="a4fc9-128">Extensions</span></span>](extensions.md)

## <a name="related-topics"></a><span data-ttu-id="a4fc9-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4fc9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4fc9-130">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="a4fc9-130">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[<span data-ttu-id="a4fc9-131">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="a4fc9-131">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[<span data-ttu-id="a4fc9-132">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="a4fc9-132">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[<span data-ttu-id="a4fc9-133">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="a4fc9-133">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> </dl>

 

 



