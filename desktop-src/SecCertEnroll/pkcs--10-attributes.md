---
description: Os atributos são incluídos em uma \# solicitação de certificado PKCS 10 adicionando-os à estrutura CertificationRequestInfo mostrada no seguinte exemplo de sintaxe ASN. 1.
ms.assetid: 5f00f638-9edb-474b-a7e4-f6f7b62c89a4
title: '\#Atributos PKCS 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c69260fa09b99c4d91fa1f8bcdafeb4b0da285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297686"
---
# <a name="pkcs-10-attributes"></a><span data-ttu-id="2b223-103">\#Atributos PKCS 10</span><span class="sxs-lookup"><span data-stu-id="2b223-103">PKCS \#10 Attributes</span></span>

<span data-ttu-id="2b223-104">Os atributos são incluídos em uma \# solicitação de certificado PKCS 10 adicionando-os à estrutura **CertificationRequestInfo** mostrada no seguinte exemplo de sintaxe ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="2b223-104">Attributes are included in a PKCS \#10 certificate request by adding them to the **CertificationRequestInfo** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="2b223-105">Para obter mais informações sobre como você pode adicionar atributos a uma solicitação, consulte o tópico [arquitetura de atributo](attribute-architecture.md) .</span><span class="sxs-lookup"><span data-stu-id="2b223-105">For more information about how you can add attributes to a request, see the [Attribute Architecture](attribute-architecture.md) topic.</span></span>

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

<span data-ttu-id="2b223-106">O atributo mais comumente adicionado a uma \# solicitação PKCS 10 é uma coleção de extensões da versão 3 definida por um objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .</span><span class="sxs-lookup"><span data-stu-id="2b223-106">The attribute most commonly added to a PKCS \#10 request is a collection of version 3 extensions defined by an [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object.</span></span> <span data-ttu-id="2b223-107">Como uma \# solicitação PKCS 10 não contém um campo ao qual as extensões podem ser adicionadas diretamente, elas devem ser adicionadas como um atributo.</span><span class="sxs-lookup"><span data-stu-id="2b223-107">Because a PKCS \#10 request does not contain a field to which the extensions can be directly added, they must be added as an attribute.</span></span> <span data-ttu-id="2b223-108">Os atributos **ClientID**, **CspProvider**, **OSVersion** e **RENEWALCERTIFICATE** também podem ser adicionados a um Pkcs) tópico.</span><span class="sxs-lookup"><span data-stu-id="2b223-108">The **ClientId**, **CspProvider**, **OSVersion**, and **RenewalCertificate** attributes can also be added to a PKCS ) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b223-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b223-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b223-110">Atributos com suporte</span><span class="sxs-lookup"><span data-stu-id="2b223-110">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



