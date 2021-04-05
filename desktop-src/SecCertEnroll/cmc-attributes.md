---
description: Na prática, a estrutura de uma solicitação CMC, mostrada pela sintaxe a seguir, é relativamente complexa porque geralmente contém solicitações aninhadas.
ms.assetid: faeee338-bce4-4b35-9be9-72a6568fa259
title: Atributos CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6778575a9359ad5b8764528fb0351b68efc1e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662679"
---
# <a name="cmc-attributes"></a>Atributos CMC

Na prática, a estrutura de uma solicitação CMC, mostrada pela sintaxe a seguir, é relativamente complexa porque geralmente contém solicitações aninhadas. Por exemplo, uma solicitação CMC pode conter zero ou um PKCS \# 10 solicitações em uma sequência **TaggedRequest** , e ela pode conter zero ou uma \# mensagem PKCS 7 em uma sequência **TaggedContentInfo** . Cada mensagem PKCS \# 7 aninhada pode conter uma solicitação CMC que pode, por sua vez, conter mais solicitações. Teoricamente, o número de níveis de aninhamento é ilimitado, mas a autoridade de certificação (CA) normalmente é configurada para limitar o tamanho de uma solicitação. Os atributos podem ser aplicados à solicitação de nível superior ou às solicitações aninhadas. Isso é discutido nas seções a seguir.

## <a name="cmcdata-structure"></a>Estrutura CMCData

Uma solicitação CMC contém sequências **de estruturas** de ASN. 1 **TaggedRequest** e **TaggedContentInfo** .

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

## <a name="taggedattribute-structure"></a>Estrutura taggedattribute

Os atributos são incluídos em uma solicitação de certificado CMC adicionando-os à coleção **taggedattribute** . Cada estrutura na coleção contém uma ID de inteiro, um OID (identificador de objeto) ASN. 1 e um conjunto de valores. Os valores possíveis podem ser qualquer um dos seguintes.

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

Se os atributos nessa estrutura se aplicarem a uma solicitação de PKCS 10 aninhada \# , o campo **certReferences** conterá o **BodyPartID** que identifica a solicitação. Se os atributos se aplicarem a uma solicitação CMC aninhada, o campo **pkiDataReference** conterá o **BodyPartID** da solicitação. Atualmente, apenas um desses campos pode ser diferente de zero. Os atributos que podem ser incluídos são listados no tópico [atributos com suporte](supported-attributes.md) .

## <a name="cmcaddextensions"></a>CmcAddExtensions

Essa estrutura pode conter extensões X. 509 versão 3 mais extensões definidas pela Microsoft. Esse atributo é definido usando a interface [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) . Se as extensões se aplicarem a uma solicitação de PKCS 10 aninhada \# , o campo **certReferences** conterá o **BodyPartID** que identifica a solicitação. Se as extensões se aplicarem a uma solicitação CMC aninhada, o campo **pkiDataReference** conterá o **BodyPartID** da solicitação. Atualmente, apenas um desses campos pode ser diferente de zero.

## <a name="sendernonce"></a>SenderNonce

Um nonce são dados binários aleatórios ou pseudo aleatórios que podem ser incluídos em uma solicitação de certificado e uma transação de resposta para ajudar a garantir que a resposta ou a solicitação não seja uma repetição de uma mensagem anterior. Para obter mais informações, consulte a propriedade [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) .

## <a name="transactid"></a>Transactid

Uma transação de solicitação e resposta de certificado de ida e volta pode ser rastreada usando um identificador. O cliente gera uma ID de transação e a retém até que o certificado ou a autoridade de registro responda com uma mensagem que conclui a transação. A resposta inclui o identificador. Para obter mais informações, consulte a propriedade [**TransactionId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) .

## <a name="reginfo"></a>RegInfo

Esse atributo pode ser usado para conter qualquer informação de registro que o cliente escolha para colocar na solicitação CMC. O valor do atributo é uma cadeia de caracteres que contém pares de nome-valor concatenados. Para obter mais informações, consulte a propriedade [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos com suporte](supported-attributes.md)
</dt> </dl>

 

 



