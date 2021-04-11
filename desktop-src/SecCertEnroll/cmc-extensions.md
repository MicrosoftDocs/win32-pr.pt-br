---
description: As extensões são incluídas em uma solicitação CMC adicionando-as à estrutura Marcadoattributes mostrada no seguinte exemplo de sintaxe ASN. 1. Para obter mais informações, consulte o tópico atributos.
ms.assetid: 3aa9175b-f889-4d5d-8eb2-a8a42f9fe750
title: Extensões CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b104af2b28470627ea593321627ae5e5076b1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170645"
---
# <a name="cmc-extensions"></a>Extensões CMC

As extensões são incluídas em uma solicitação CMC adicionando-as à estrutura **marcadoattributes** mostrada no seguinte exemplo de sintaxe ASN. 1. Para obter mais informações, consulte o tópico [atributos](attributes.md) .

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

Cada estrutura na coleção **taggedattributes** contém uma ID de inteiro, um OID (identificador de objeto) ASN. 1 e um conjunto de valores. As extensões são incorporadas a uma solicitação adicionando uma estrutura **CmcAddExtensions** ao campo **valores** . A sintaxe de estrutura ASN. 1 é mostrada no exemplo a seguir. O identificador de objeto é **XCN \_ OID \_ CMC \_ Add \_ Extensions** (1.3.6.1.5.5.7.7.8).

``` syntax
CmcAddExtensions ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   extensions              Extensions
}

Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
   extnId              EncodedObjectID,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTETSTRING
}
```

O procedimento a seguir discute como usar a API de registro de certificado para adicionar extensões a uma solicitação de certificado CMC.

**Para usar a API de registro de certificado para adicionar extensões a uma solicitação de certificado CMC**

1.  Crie uma extensão usando qualquer uma das interfaces disponíveis que derivam da interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) ou use o objeto **IX509Extension** diretamente para criar extensões personalizadas.
2.  Chame a propriedade [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) no objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) para recuperar uma coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
3.  Adicione as extensões criadas na etapa 1 à coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
4.  Chame o [**registro**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) para executar automaticamente as seguintes ações:
    -   Recupere um objeto [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) do objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .
    -   Crie e inicialize um objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) usando a coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) recuperada na etapa 2.
    -   Crie uma coleção [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) e adicione o objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) a ela.
    -   Use a coleção [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) para inicializar um objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .
    -   Adicione o objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) à coleção [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos](attributes.md)
</dt> <dt>

[Arquitetura de atributo](attribute-architecture.md)
</dt> <dt>

[Atributos CMC](cmc-attributes.md)
</dt> <dt>

[Extensões](extensions.md)
</dt> </dl>

 

 



