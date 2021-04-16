---
description: As extensões são incluídas em uma \# solicitação de certificado PKCS 10 adicionando-as ao campo atributos da estrutura CertificationRequestInfo mostrada no seguinte exemplo de sintaxe ASN. 1. Para obter mais informações, consulte o tópico atributos.
ms.assetid: 26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e
title: '\#Extensões PKCS 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba71f0a24f50503fd92b3b9670b787dea3b9ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750441"
---
# <a name="pkcs-10-extensions"></a><span data-ttu-id="151af-104">\#Extensões PKCS 10</span><span class="sxs-lookup"><span data-stu-id="151af-104">PKCS \#10 Extensions</span></span>

<span data-ttu-id="151af-105">As extensões são incluídas em uma \# solicitação de certificado PKCS 10 adicionando-as ao campo **atributos** da estrutura **CertificationRequestInfo** mostrada no seguinte exemplo de sintaxe ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="151af-105">Extensions are included in a PKCS \#10 certificate request by adding them to the **attributes** field of the **CertificationRequestInfo** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="151af-106">Para obter mais informações, consulte o tópico [atributos](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="151af-106">For more information, see the [Attributes](attributes.md) topic.</span></span>

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

<span data-ttu-id="151af-107">O procedimento a seguir discute como usar a API de registro de certificado para adicionar extensões a uma \# solicitação de certificado PKCS 10:</span><span class="sxs-lookup"><span data-stu-id="151af-107">The following procedure discusses how to use the Certificate Enrollment API to add extensions to a PKCS \#10 certificate request:</span></span>

1.  <span data-ttu-id="151af-108">Recupere uma coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) chamando a propriedade [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) no objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .</span><span class="sxs-lookup"><span data-stu-id="151af-108">Retrieve an [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection by calling the [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) property on the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span>
2.  <span data-ttu-id="151af-109">Crie uma extensão usando qualquer uma das interfaces disponíveis que derivam da interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .</span><span class="sxs-lookup"><span data-stu-id="151af-109">Create an extension by using any of the available interfaces that derive from the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface.</span></span>
3.  <span data-ttu-id="151af-110">Adicione as extensões criadas na etapa 2 à coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) recuperada na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="151af-110">Add the extensions created in step 2 to the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection retrieved in step 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="151af-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="151af-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="151af-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="151af-112">Attributes</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="151af-113">Arquitetura de atributo</span><span class="sxs-lookup"><span data-stu-id="151af-113">Attribute Architecture</span></span>](attribute-architecture.md)
</dt> <dt>

[<span data-ttu-id="151af-114">\#Atributos PKCS 10</span><span class="sxs-lookup"><span data-stu-id="151af-114">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
</dt> <dt>

[<span data-ttu-id="151af-115">Extensões</span><span class="sxs-lookup"><span data-stu-id="151af-115">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



