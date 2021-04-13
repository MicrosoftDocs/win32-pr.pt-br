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
# <a name="pkcs-10-attributes"></a>\#Atributos PKCS 10

Os atributos são incluídos em uma \# solicitação de certificado PKCS 10 adicionando-os à estrutura **CertificationRequestInfo** mostrada no seguinte exemplo de sintaxe ASN. 1. Para obter mais informações sobre como você pode adicionar atributos a uma solicitação, consulte o tópico [arquitetura de atributo](attribute-architecture.md) .

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

O atributo mais comumente adicionado a uma \# solicitação PKCS 10 é uma coleção de extensões da versão 3 definida por um objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) . Como uma \# solicitação PKCS 10 não contém um campo ao qual as extensões podem ser adicionadas diretamente, elas devem ser adicionadas como um atributo. Os atributos **ClientID**, **CspProvider**, **OSVersion** e **RENEWALCERTIFICATE** também podem ser adicionados a um Pkcs) tópico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos com suporte](supported-attributes.md)
</dt> </dl>

 

 



