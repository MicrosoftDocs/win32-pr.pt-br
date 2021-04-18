---
description: PKCS \# 7 é um padrão de sintaxe de mensagem criptográfica.
ms.assetid: fd4e2a13-f257-4ba9-a11d-35f49c5a6c00
title: '\#Atributos PKCS 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0c7bc9b991a6625cae36ae9857275a9d86786a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811064"
---
# <a name="pkcs-7-attributes"></a><span data-ttu-id="d4d2c-103">\#Atributos PKCS 7</span><span class="sxs-lookup"><span data-stu-id="d4d2c-103">PKCS \#7 Attributes</span></span>

<span data-ttu-id="d4d2c-104">PKCS \# 7 é um padrão de sintaxe de mensagem criptográfica.</span><span class="sxs-lookup"><span data-stu-id="d4d2c-104">PKCS \#7 is a cryptographic message syntax standard.</span></span> <span data-ttu-id="d4d2c-105">Uma \# mensagem PKCS 7 não faz, por si só, constituir uma solicitação de certificado, mas pode encapsular uma \# solicitação PKCS 10 ou CMC em uma estrutura **ContentInfo** ASN. 1 usando um dos seguintes tipos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d4d2c-105">A PKCS \#7 message does not, by itself, constitute a certificate request, but it can encapsulate a PKCS \#10 or CMC request in a **ContentInfo** ASN.1 structure by using one of the following content types.</span></span> <span data-ttu-id="d4d2c-106">O encapsulamento permite que você adicione funcionalidades extras, como várias assinaturas, que não estão disponíveis de outra forma.</span><span class="sxs-lookup"><span data-stu-id="d4d2c-106">Encapsulation enables you to add extra functionality, such as multiple signatures, that is not otherwise available.</span></span>

-   <span data-ttu-id="d4d2c-107">**Dados**</span><span class="sxs-lookup"><span data-stu-id="d4d2c-107">**Data**</span></span>
-   <span data-ttu-id="d4d2c-108">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="d4d2c-108">**SignedData**</span></span>
-   <span data-ttu-id="d4d2c-109">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="d4d2c-109">**EnvelopedData**</span></span>
-   <span data-ttu-id="d4d2c-110">**SignedAndEnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="d4d2c-110">**SignedAndEnvelopedData**</span></span>
-   <span data-ttu-id="d4d2c-111">**DigestedData**</span><span class="sxs-lookup"><span data-stu-id="d4d2c-111">**DigestedData**</span></span>
-   <span data-ttu-id="d4d2c-112">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="d4d2c-112">**EncryptedData**</span></span>

<span data-ttu-id="d4d2c-113">Os atributos podem ser adicionados aos campos **authenticatedAttributes** e **unauthenticatedAttributes** do tipo de conteúdo **SignedData** .</span><span class="sxs-lookup"><span data-stu-id="d4d2c-113">Attributes can be added to the **authenticatedAttributes** and **unauthenticatedAttributes** fields of the **SignedData** content type.</span></span>

``` syntax
SignedData ::= SEQUENCE 
{
   version             INTEGER,
   digestAlgorithms    DigestAlgorithmIdentifiers,
   contentInfo         ContentInfo,
   certificates        [0] IMPLICIT Certificates OPTIONAL,
   crls                [1] IMPLICIT CertificateRevocationLists OPTIONAL,
   signerInfos         SignerInfos
}

SignerInfos ::= SET OF SignerInfo

SignerInfo ::= SEQUENCE 
{
    version                     INTEGER,
    sid                         CertIdentifier,
    digestAlgorithm             DigestAlgorithmIdentifier,
    authenticatedAttributes     [0] IMPLICIT Attributes OPTIONAL,
    digestEncryptionAlgorithm   DigestEncryptionAlgId,
    encryptedDigest             EncryptedDigest,
    unauthenticatedAttributes   [1] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

<span data-ttu-id="d4d2c-114">O processo necessário para arquivar a chave privada de um cliente em uma autoridade de certificação (CA) fornece um exemplo abrangente de como os atributos autenticados (assinados) e os atributos não autenticados podem ser usados:</span><span class="sxs-lookup"><span data-stu-id="d4d2c-114">The process required to archive a client's private key on a certification authority (CA) provides a comprehensive example of how authenticated (signed) attributes and the unauthenticated attributes can be used:</span></span>

-   <span data-ttu-id="d4d2c-115">O cliente cria um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e adiciona os dados apropriados para o tipo de certificado que está sendo solicitado.</span><span class="sxs-lookup"><span data-stu-id="d4d2c-115">The client creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and adds appropriate data for the type of certificate being requested.</span></span>
-   <span data-ttu-id="d4d2c-116">O cliente usa a \# solicitação PKCS 10 para inicializar um objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="d4d2c-116">The client uses the PKCS \#10 request to initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span> <span data-ttu-id="d4d2c-117">A \# solicitação PKCS 10 é colocada na estrutura **TaggedRequest** na solicitação CMC.</span><span class="sxs-lookup"><span data-stu-id="d4d2c-117">The PKCS \#10 request is placed into the **TaggedRequest** structure in the CMC request.</span></span> <span data-ttu-id="d4d2c-118">Para obter mais informações, consulte [atributos CMC](cmc-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="d4d2c-118">For more information, see [CMC Attributes](cmc-attributes.md).</span></span>
-   <span data-ttu-id="d4d2c-119">O cliente criptografa uma chave privada e a usa para inicializar um objeto [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) .</span><span class="sxs-lookup"><span data-stu-id="d4d2c-119">The client encrypts a private key and uses it to initialize an [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) object.</span></span> <span data-ttu-id="d4d2c-120">O novo atributo **ArchiveKey** é encapsulado em uma estrutura **EnvelopedData** .</span><span class="sxs-lookup"><span data-stu-id="d4d2c-120">The new **ArchiveKey** attribute is encapsulated in an **EnvelopedData** structure.</span></span>

    ``` syntax
    EnvelopedData ::= SEQUENCE 
    {
        version                 INTEGER,
        recipientInfos          RecipientInfos,
        encryptedContentInfo    EncryptedContentInfo
    } 

    RecipientInfos ::= SET OF RecipientInfo

    EncryptedContentInfo ::= SEQUENCE 
    {
        contentType                 ContentType,
        contentEncryptionAlgorithm  ContentEncryptionAlgId,
        encryptedContent            [0] IMPLICIT EncryptedContent OPTIONAL
    } 

    EncryptedContent ::= OCTET STRING

    RecipientInfo ::= SEQUENCE 
    {
        version                 INTEGER,
        issuerAndSerialNumber   IssuerAndSerialNumber,
        keyEncryptionAlgorithm  KeyEncryptionAlgId,
        encryptedKey            EncryptedKey
    } 
    ```

-   <span data-ttu-id="d4d2c-121">O cliente cria um hash SHA-1 da chave criptografada e a usa para inicializar um objeto [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) .</span><span class="sxs-lookup"><span data-stu-id="d4d2c-121">The client creates a SHA-1 hash of the encrypted key and uses it to initialize an [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) object.</span></span>
-   <span data-ttu-id="d4d2c-122">O cliente recupera a coleção [**criptattributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) da solicitação CMC e adiciona os atributos **ArchiveKey** e **ArchiveKeyHash** a ela.</span><span class="sxs-lookup"><span data-stu-id="d4d2c-122">The client retrieves the [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) collection from the CMC request and adds the **ArchiveKey** and the **ArchiveKeyHash** attributes to it.</span></span> <span data-ttu-id="d4d2c-123">Os atributos são colocados na estrutura **marcadoattributes** da solicitação CMC.</span><span class="sxs-lookup"><span data-stu-id="d4d2c-123">The attributes are placed into the **TaggedAttributes** structure of the CMC request.</span></span>
-   <span data-ttu-id="d4d2c-124">O cliente usa a solicitação CMC para inicializar um objeto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) .</span><span class="sxs-lookup"><span data-stu-id="d4d2c-124">The client uses the CMC request to initialize an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object.</span></span> <span data-ttu-id="d4d2c-125">Isso coloca a solicitação CMC no campo **contentInfo** da \# estrutura **SignedData** do PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="d4d2c-125">This places the CMC request into the **contentInfo** field of the PKCS \#7 **SignedData** structure.</span></span>
-   <span data-ttu-id="d4d2c-126">O atributo **ArchiveKeyHash** é assinado e colocado na sequência **AuthenticatedAttributes** da estrutura **SignerInfo** .</span><span class="sxs-lookup"><span data-stu-id="d4d2c-126">The **ArchiveKeyHash** attribute is signed and placed in the **authenticatedAttributes** sequence of the **SignerInfo** structure.</span></span>
-   <span data-ttu-id="d4d2c-127">O atributo **ArchiveKey** é colocado na sequência **UnauthenticatedAttributes** da estrutura **SignerInfo** associada ao signatário principal da \# mensagem PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="d4d2c-127">The **ArchiveKey** attribute is placed in the **unauthenticatedAttributes** sequence of the **SignerInfo** structure associated with the primary signer of the PKCS \#7 message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4d2c-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4d2c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4d2c-129">Atributos com suporte</span><span class="sxs-lookup"><span data-stu-id="d4d2c-129">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



