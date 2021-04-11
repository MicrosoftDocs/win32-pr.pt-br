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
# <a name="cmc-extensions"></a><span data-ttu-id="5fcd5-104">Extensões CMC</span><span class="sxs-lookup"><span data-stu-id="5fcd5-104">CMC Extensions</span></span>

<span data-ttu-id="5fcd5-105">As extensões são incluídas em uma solicitação CMC adicionando-as à estrutura **marcadoattributes** mostrada no seguinte exemplo de sintaxe ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="5fcd5-105">Extensions are included in a CMC request by adding them to the **TaggedAttributes** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="5fcd5-106">Para obter mais informações, consulte o tópico [atributos](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="5fcd5-106">For more information, see the [Attributes](attributes.md) topic.</span></span>

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

<span data-ttu-id="5fcd5-107">Cada estrutura na coleção **taggedattributes** contém uma ID de inteiro, um OID (identificador de objeto) ASN. 1 e um conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="5fcd5-107">Each structure in the **TaggedAttributes** collection contains an integer ID, an ASN.1 object identifier (OID), and a set of values.</span></span> <span data-ttu-id="5fcd5-108">As extensões são incorporadas a uma solicitação adicionando uma estrutura **CmcAddExtensions** ao campo **valores** .</span><span class="sxs-lookup"><span data-stu-id="5fcd5-108">Extensions are incorporated into a request by adding a **CmcAddExtensions** structure to the **values** field.</span></span> <span data-ttu-id="5fcd5-109">A sintaxe de estrutura ASN. 1 é mostrada no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="5fcd5-109">The ASN.1 structure syntax is shown in the following example.</span></span> <span data-ttu-id="5fcd5-110">O identificador de objeto é **XCN \_ OID \_ CMC \_ Add \_ Extensions** (1.3.6.1.5.5.7.7.8).</span><span class="sxs-lookup"><span data-stu-id="5fcd5-110">The object identifier is **XCN\_OID\_CMC\_ADD\_EXTENSIONS** (1.3.6.1.5.5.7.7.8).</span></span>

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

<span data-ttu-id="5fcd5-111">O procedimento a seguir discute como usar a API de registro de certificado para adicionar extensões a uma solicitação de certificado CMC.</span><span class="sxs-lookup"><span data-stu-id="5fcd5-111">The following procedure discusses how to use the Certificate Enrollment API to add extensions to a CMC certificate request.</span></span>

<span data-ttu-id="5fcd5-112">**Para usar a API de registro de certificado para adicionar extensões a uma solicitação de certificado CMC**</span><span class="sxs-lookup"><span data-stu-id="5fcd5-112">**To use the Certificate Enrollment API to add extensions to a CMC certificate request**</span></span>

1.  <span data-ttu-id="5fcd5-113">Crie uma extensão usando qualquer uma das interfaces disponíveis que derivam da interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) ou use o objeto **IX509Extension** diretamente para criar extensões personalizadas.</span><span class="sxs-lookup"><span data-stu-id="5fcd5-113">Create an extension by using any of the available interfaces that derive from the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface or use the **IX509Extension** object directly to create custom extensions.</span></span>
2.  <span data-ttu-id="5fcd5-114">Chame a propriedade [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) no objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) para recuperar uma coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .</span><span class="sxs-lookup"><span data-stu-id="5fcd5-114">Call the [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) property on the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object to retrieve an [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection.</span></span>
3.  <span data-ttu-id="5fcd5-115">Adicione as extensões criadas na etapa 1 à coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .</span><span class="sxs-lookup"><span data-stu-id="5fcd5-115">Add the extensions created in step 1 to the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection.</span></span>
4.  <span data-ttu-id="5fcd5-116">Chame o [**registro**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) para executar automaticamente as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="5fcd5-116">Call [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) to automatically perform the following actions:</span></span>
    -   <span data-ttu-id="5fcd5-117">Recupere um objeto [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) do objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="5fcd5-117">Retrieve an [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) object from the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
    -   <span data-ttu-id="5fcd5-118">Crie e inicialize um objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) usando a coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) recuperada na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="5fcd5-118">Create and initialize an [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object by using the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection retrieved in step 2.</span></span>
    -   <span data-ttu-id="5fcd5-119">Crie uma coleção [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) e adicione o objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) a ela.</span><span class="sxs-lookup"><span data-stu-id="5fcd5-119">Create an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection and add the [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object to it.</span></span>
    -   <span data-ttu-id="5fcd5-120">Use a coleção [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) para inicializar um objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .</span><span class="sxs-lookup"><span data-stu-id="5fcd5-120">Use the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection to initialize an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object.</span></span>
    -   <span data-ttu-id="5fcd5-121">Adicione o objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) à coleção [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) .</span><span class="sxs-lookup"><span data-stu-id="5fcd5-121">Add the [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object to the [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fcd5-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5fcd5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fcd5-123">Atributos</span><span class="sxs-lookup"><span data-stu-id="5fcd5-123">Attributes</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="5fcd5-124">Arquitetura de atributo</span><span class="sxs-lookup"><span data-stu-id="5fcd5-124">Attribute Architecture</span></span>](attribute-architecture.md)
</dt> <dt>

[<span data-ttu-id="5fcd5-125">Atributos CMC</span><span class="sxs-lookup"><span data-stu-id="5fcd5-125">CMC Attributes</span></span>](cmc-attributes.md)
</dt> <dt>

[<span data-ttu-id="5fcd5-126">Extensões</span><span class="sxs-lookup"><span data-stu-id="5fcd5-126">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



