---
description: Os atributos são incluídos em uma solicitação de certificado PKCS 10 adicionando-os à estrutura CertificationRequestInfo mostrada no exemplo de \# sintaxe ASN.1 a seguir.
ms.assetid: 5f00f638-9edb-474b-a7e4-f6f7b62c89a4
title: Atributos PKCS \# 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7922f7d308c6956af4c0098ea278a859113af45861ef3d21a20548081e7eee3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993286"
---
# <a name="pkcs-10-attributes"></a>Atributos PKCS \# 10

Os atributos são incluídos em uma solicitação de certificado PKCS 10 adicionando-os à estrutura CertificationRequestInfo mostrada no exemplo de \# sintaxe ASN.1 a seguir.  Para obter mais informações sobre como você pode adicionar atributos a uma solicitação, consulte o [tópico Arquitetura de](attribute-architecture.md) atributo.

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

O atributo mais comumente adicionado a uma solicitação PKCS 10 é uma coleção de extensões da versão 3 definidas por um objeto \# [**IX509AttributeExtensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) Como uma solicitação PKCS 10 não contém um campo ao qual as extensões podem ser adicionadas diretamente, elas devem ser \# adicionadas como um atributo. Os **atributos ClientId**, **CspProvider,** **OSVersion** e **RenewalCertificate** também podem ser adicionados a um tópico PKCS ).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos com suporte](supported-attributes.md)
</dt> </dl>

 

 



