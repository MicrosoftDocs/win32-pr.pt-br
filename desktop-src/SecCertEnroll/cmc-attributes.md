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
# <a name="cmc-attributes"></a><span data-ttu-id="3bbac-103">Atributos CMC</span><span class="sxs-lookup"><span data-stu-id="3bbac-103">CMC Attributes</span></span>

<span data-ttu-id="3bbac-104">Na prática, a estrutura de uma solicitação CMC, mostrada pela sintaxe a seguir, é relativamente complexa porque geralmente contém solicitações aninhadas.</span><span class="sxs-lookup"><span data-stu-id="3bbac-104">In practice, the structure of a CMC request, shown by the following syntax, is relatively complex because it often contains nested requests.</span></span> <span data-ttu-id="3bbac-105">Por exemplo, uma solicitação CMC pode conter zero ou um PKCS \# 10 solicitações em uma sequência **TaggedRequest** , e ela pode conter zero ou uma \# mensagem PKCS 7 em uma sequência **TaggedContentInfo** .</span><span class="sxs-lookup"><span data-stu-id="3bbac-105">For example, a CMC request can contain zero or one PKCS \#10 requests in a **TaggedRequest** sequence, and it can contain zero or one PKCS \#7 messages in a **TaggedContentInfo** sequence.</span></span> <span data-ttu-id="3bbac-106">Cada mensagem PKCS \# 7 aninhada pode conter uma solicitação CMC que pode, por sua vez, conter mais solicitações.</span><span class="sxs-lookup"><span data-stu-id="3bbac-106">Each nested PKCS \#7 message can contain a CMC request which can, in turn, contain more requests.</span></span> <span data-ttu-id="3bbac-107">Teoricamente, o número de níveis de aninhamento é ilimitado, mas a autoridade de certificação (CA) normalmente é configurada para limitar o tamanho de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="3bbac-107">The number of nesting levels is theoretically unlimited, but the certification authority (CA) is typically configured to limit the size of a request.</span></span> <span data-ttu-id="3bbac-108">Os atributos podem ser aplicados à solicitação de nível superior ou às solicitações aninhadas.</span><span class="sxs-lookup"><span data-stu-id="3bbac-108">Attributes can be applied to the top level request or to the nested requests.</span></span> <span data-ttu-id="3bbac-109">Isso é discutido nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="3bbac-109">This is discussed in the following sections.</span></span>

## <a name="cmcdata-structure"></a><span data-ttu-id="3bbac-110">Estrutura CMCData</span><span class="sxs-lookup"><span data-stu-id="3bbac-110">CMCData Structure</span></span>

<span data-ttu-id="3bbac-111">Uma solicitação CMC contém sequências **de estruturas** de ASN. 1 **TaggedRequest** e **TaggedContentInfo** .</span><span class="sxs-lookup"><span data-stu-id="3bbac-111">A CMC request contains sequences of **TaggedAttribute**, **TaggedRequest**, and **TaggedContentInfo** ASN.1 structures.</span></span>

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

## <a name="taggedattribute-structure"></a><span data-ttu-id="3bbac-112">Estrutura taggedattribute</span><span class="sxs-lookup"><span data-stu-id="3bbac-112">TaggedAttribute Structure</span></span>

<span data-ttu-id="3bbac-113">Os atributos são incluídos em uma solicitação de certificado CMC adicionando-os à coleção **taggedattribute** .</span><span class="sxs-lookup"><span data-stu-id="3bbac-113">Attributes are included in a CMC certificate request by adding them to the **TaggedAttribute** collection.</span></span> <span data-ttu-id="3bbac-114">Cada estrutura na coleção contém uma ID de inteiro, um OID (identificador de objeto) ASN. 1 e um conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="3bbac-114">Each structure in the collection contains an integer ID, an ASN.1 object identifier (OID), and a set of values.</span></span> <span data-ttu-id="3bbac-115">Os valores possíveis podem ser qualquer um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="3bbac-115">The possible values can be any of the following.</span></span>

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

## <a name="cmcaddattributes"></a><span data-ttu-id="3bbac-116">CMCAddAttributes</span><span class="sxs-lookup"><span data-stu-id="3bbac-116">CMCAddAttributes</span></span>

<span data-ttu-id="3bbac-117">Se os atributos nessa estrutura se aplicarem a uma solicitação de PKCS 10 aninhada \# , o campo **certReferences** conterá o **BodyPartID** que identifica a solicitação.</span><span class="sxs-lookup"><span data-stu-id="3bbac-117">If the attributes in this structure apply to a nested PKCS \#10 request, the **certReferences** field will contain the **BodyPartID** that identifies the request.</span></span> <span data-ttu-id="3bbac-118">Se os atributos se aplicarem a uma solicitação CMC aninhada, o campo **pkiDataReference** conterá o **BodyPartID** da solicitação.</span><span class="sxs-lookup"><span data-stu-id="3bbac-118">If the attributes apply to a nested CMC request, the **pkiDataReference** field will contain the **BodyPartID** of the request.</span></span> <span data-ttu-id="3bbac-119">Atualmente, apenas um desses campos pode ser diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="3bbac-119">Currently, only one of these fields can be nonzero.</span></span> <span data-ttu-id="3bbac-120">Os atributos que podem ser incluídos são listados no tópico [atributos com suporte](supported-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="3bbac-120">The attributes that can be included are listed in the [Supported Attributes](supported-attributes.md) topic.</span></span>

## <a name="cmcaddextensions"></a><span data-ttu-id="3bbac-121">CmcAddExtensions</span><span class="sxs-lookup"><span data-stu-id="3bbac-121">CmcAddExtensions</span></span>

<span data-ttu-id="3bbac-122">Essa estrutura pode conter extensões X. 509 versão 3 mais extensões definidas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3bbac-122">This structure can contain X.509 version 3 extensions plus extensions defined by Microsoft.</span></span> <span data-ttu-id="3bbac-123">Esse atributo é definido usando a interface [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .</span><span class="sxs-lookup"><span data-stu-id="3bbac-123">This attribute is defined by using the [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) interface.</span></span> <span data-ttu-id="3bbac-124">Se as extensões se aplicarem a uma solicitação de PKCS 10 aninhada \# , o campo **certReferences** conterá o **BodyPartID** que identifica a solicitação.</span><span class="sxs-lookup"><span data-stu-id="3bbac-124">If the extensions apply to a nested PKCS \#10 request, the **certReferences** field will contain the **BodyPartID** that identifies the request.</span></span> <span data-ttu-id="3bbac-125">Se as extensões se aplicarem a uma solicitação CMC aninhada, o campo **pkiDataReference** conterá o **BodyPartID** da solicitação.</span><span class="sxs-lookup"><span data-stu-id="3bbac-125">If the extensions apply to a nested CMC request, the **pkiDataReference** field will contain the **BodyPartID** of the request.</span></span> <span data-ttu-id="3bbac-126">Atualmente, apenas um desses campos pode ser diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="3bbac-126">Currently, only one of these fields can be nonzero.</span></span>

## <a name="sendernonce"></a><span data-ttu-id="3bbac-127">SenderNonce</span><span class="sxs-lookup"><span data-stu-id="3bbac-127">SenderNonce</span></span>

<span data-ttu-id="3bbac-128">Um nonce são dados binários aleatórios ou pseudo aleatórios que podem ser incluídos em uma solicitação de certificado e uma transação de resposta para ajudar a garantir que a resposta ou a solicitação não seja uma repetição de uma mensagem anterior.</span><span class="sxs-lookup"><span data-stu-id="3bbac-128">A nonce is random or pseudo-random binary data that can be included in a certificate request and response transaction to help ensure that the response or request is not a repeat of a previous message.</span></span> <span data-ttu-id="3bbac-129">Para obter mais informações, consulte a propriedade [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) .</span><span class="sxs-lookup"><span data-stu-id="3bbac-129">For more information, see the [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) property.</span></span>

## <a name="transactid"></a><span data-ttu-id="3bbac-130">Transactid</span><span class="sxs-lookup"><span data-stu-id="3bbac-130">TransactID</span></span>

<span data-ttu-id="3bbac-131">Uma transação de solicitação e resposta de certificado de ida e volta pode ser rastreada usando um identificador.</span><span class="sxs-lookup"><span data-stu-id="3bbac-131">A round trip certificate request and response transaction can be tracked using an identifier.</span></span> <span data-ttu-id="3bbac-132">O cliente gera uma ID de transação e a retém até que o certificado ou a autoridade de registro responda com uma mensagem que conclui a transação.</span><span class="sxs-lookup"><span data-stu-id="3bbac-132">The client generates a transaction ID and retains it until the certificate or registration authority responds with a message that completes the transaction.</span></span> <span data-ttu-id="3bbac-133">A resposta inclui o identificador.</span><span class="sxs-lookup"><span data-stu-id="3bbac-133">The response includes the identifier.</span></span> <span data-ttu-id="3bbac-134">Para obter mais informações, consulte a propriedade [**TransactionId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) .</span><span class="sxs-lookup"><span data-stu-id="3bbac-134">For more information, see the [**TransactionId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) property.</span></span>

## <a name="reginfo"></a><span data-ttu-id="3bbac-135">RegInfo</span><span class="sxs-lookup"><span data-stu-id="3bbac-135">RegInfo</span></span>

<span data-ttu-id="3bbac-136">Esse atributo pode ser usado para conter qualquer informação de registro que o cliente escolha para colocar na solicitação CMC.</span><span class="sxs-lookup"><span data-stu-id="3bbac-136">This attribute can be used to contain any registration information that the client chooses to put into the CMC request.</span></span> <span data-ttu-id="3bbac-137">O valor do atributo é uma cadeia de caracteres que contém pares de nome-valor concatenados.</span><span class="sxs-lookup"><span data-stu-id="3bbac-137">The attribute value is string that contains concatenated name-value pairs.</span></span> <span data-ttu-id="3bbac-138">Para obter mais informações, consulte a propriedade [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) .</span><span class="sxs-lookup"><span data-stu-id="3bbac-138">For more information, see the [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bbac-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3bbac-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bbac-140">Atributos com suporte</span><span class="sxs-lookup"><span data-stu-id="3bbac-140">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



