---
description: Na prática, a estrutura de uma solicitação de CMC, mostrada pela sintaxe a seguir, é relativamente complexa porque geralmente contém solicitações aninhadas.
ms.assetid: faeee338-bce4-4b35-9be9-72a6568fa259
title: Atributos do CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b98e30c257234ebee864a1749ceecee7b79e25a9e11c9f1f190c60f3154ef64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902059"
---
# <a name="cmc-attributes"></a>Atributos do CMC

Na prática, a estrutura de uma solicitação de CMC, mostrada pela sintaxe a seguir, é relativamente complexa porque geralmente contém solicitações aninhadas. Por exemplo, uma solicitação cmc pode conter zero ou uma solicitação PKCS 10 em uma sequência TaggedRequest e pode conter zero ou uma mensagem PKCS 7 em uma sequência \#  \# **TaggedContentInfo.** Cada mensagem PKCS 7 aninhada pode conter uma solicitação de CMC que pode, por sua \# vez, conter mais solicitações. O número de níveis de aninhamento é teoricamente ilimitado, mas a AC (autoridade de certificação) normalmente é configurada para limitar o tamanho de uma solicitação. Os atributos podem ser aplicados à solicitação de nível superior ou às solicitações aninhadas. Isso é discutido nas seções a seguir.

## <a name="cmcdata-structure"></a>Estrutura CMCData

Uma solicitação do CMC contém sequências de estruturas **TaggedAttribute**, **TaggedRequest** e **TaggedContentInfo** ASN.1.

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute
ReqSequence      ::=    SEQUENCE OF TaggedRequest
CmsSequence      ::=    SEQUENCE OF TaggedContentInfo

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

TaggedRequest ::= CHOICE 
{
   tcr                     [0] IMPLICIT TaggedCertificationRequest
}

TaggedContentInfo ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   contentInfo             ANY
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

## <a name="taggedattribute-structure"></a>Estrutura TaggedAttribute

Os atributos são incluídos em uma solicitação de certificado do CMC adicionando-os à coleção **TaggedAttribute.** Cada estrutura na coleção contém uma ID de inteiro, um OID (identificador de objeto ASN.1) e um conjunto de valores. Os valores possíveis podem ser qualquer um dos seguintes.

``` syntax
CmcAddAttributes ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   attributes              Attributes
}

Attributes ::= SET OF Attribute
Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}

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

SenderNonce ::= OCTET STRING

TransactID ::= OCTET STRING

RegInfo ::= OCTET STRING
```

## <a name="cmcaddattributes"></a>CMCAddAttributes

Se os atributos nessa estrutura se aplicarem a uma solicitação PKCS 10 aninhada, o \# **campo certReferences** conterá **o BodyPartID** que identifica a solicitação. Se os atributos se aplicarem a uma solicitação de CMC aninhada, o **campo pkiDataReference** conterá **o BodyPartID** da solicitação. Atualmente, apenas um desses campos pode ser diferente de zero. Os atributos que podem ser incluídos são listados no [tópico Atributos com](supported-attributes.md) suporte.

## <a name="cmcaddextensions"></a>CmcAddExtensions

Essa estrutura pode conter extensões X.509 versão 3 mais extensões definidas pela Microsoft. Esse atributo é definido usando a interface [**IX509AttributeExtensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) Se as extensões se aplicarem a uma solicitação PKCS 10 aninhada, o \# **campo certReferences** conterá **o BodyPartID** que identifica a solicitação. Se as extensões se aplicarem a uma solicitação de CMC aninhada, o campo **pkiDataReference** conterá **o BodyPartID** da solicitação. Atualmente, apenas um desses campos pode ser diferente de zero.

## <a name="sendernonce"></a>SenderNonce

Um nonce são dados binários aleatórios ou pseudo-aleatórios que podem ser incluídos em uma solicitação de certificado e transação de resposta para ajudar a garantir que a resposta ou solicitação não seja uma repetição de uma mensagem anterior. Para obter mais informações, consulte a [**propriedade SenderNonce.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce)

## <a name="transactid"></a>TransactID

Uma solicitação de certificado de ida e volta e uma transação de resposta podem ser rastreadas usando um identificador. O cliente gera uma ID de transação e a retém até que o certificado ou a autoridade de registro responda com uma mensagem que conclui a transação. A resposta inclui o identificador. Para obter mais informações, consulte a [**propriedade TransactionId.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid)

## <a name="reginfo"></a>RegInfo

Esse atributo pode ser usado para conter qualquer informação de registro que o cliente opte por colocar na solicitação do CMC. O valor do atributo é uma cadeia de caracteres que contém pares nome-valor concatenados. Para obter mais informações, consulte a [**propriedade NameValuePairs.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos com suporte](supported-attributes.md)
</dt> </dl>

 

 



