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
# <a name="pkcs-10-extensions"></a>\#Extensões PKCS 10

As extensões são incluídas em uma \# solicitação de certificado PKCS 10 adicionando-as ao campo **atributos** da estrutura **CertificationRequestInfo** mostrada no seguinte exemplo de sintaxe ASN. 1. Para obter mais informações, consulte o tópico [atributos](attributes.md) .

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

O procedimento a seguir discute como usar a API de registro de certificado para adicionar extensões a uma \# solicitação de certificado PKCS 10:

1.  Recupere uma coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) chamando a propriedade [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) no objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
2.  Crie uma extensão usando qualquer uma das interfaces disponíveis que derivam da interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .
3.  Adicione as extensões criadas na etapa 2 à coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) recuperada na etapa 1.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos](attributes.md)
</dt> <dt>

[Arquitetura de atributo](attribute-architecture.md)
</dt> <dt>

[\#Atributos PKCS 10](pkcs--10-attributes.md)
</dt> <dt>

[Extensões](extensions.md)
</dt> </dl>

 

 



