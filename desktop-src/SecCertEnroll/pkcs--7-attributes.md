---
description: O PKCS \# 7 é um padrão de sintaxe de mensagem criptográfica.
ms.assetid: fd4e2a13-f257-4ba9-a11d-35f49c5a6c00
title: Atributos PKCS \# 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24436a918afe2d9bd85d7c28ae330b8c022bd4e3d34d30e58aae7b9c57c4963a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774581"
---
# <a name="pkcs-7-attributes"></a>Atributos PKCS \# 7

O PKCS \# 7 é um padrão de sintaxe de mensagem criptográfica. Uma mensagem PKCS 7 não constitui, por si só, uma solicitação de certificado, mas pode encapsular uma solicitação PKCS 10 ou CMC em uma estrutura \# \# **ContentInfo** ASN.1 usando um dos tipos de conteúdo a seguir. O encapsulamento permite que você adicione funcionalidades extras, como várias assinaturas, que não estão disponíveis de outra forma.

-   **Dados**
-   **SignedData**
-   **EnvelopedData**
-   **SignedAndEnvelopedData**
-   **DigestedData**
-   **Encrypteddata**

Atributos podem ser adicionados aos campos **authenticatedAttributes** e **unauthenticatedAttributes** do tipo de conteúdo **SignedData.**

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

O processo necessário para arquivar a chave privada de um cliente em uma AC (autoridade de certificação) fornece um exemplo abrangente de como os atributos autenticados (assinados) e os atributos não autenticados podem ser usados:

-   O cliente cria um [**objeto IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e adiciona dados apropriados para o tipo de certificado que está sendo solicitado.
-   O cliente usa a solicitação PKCS 10 para inicializar um \# [**objeto IX509CertificateRequestCmc.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) A solicitação PKCS \# 10 é colocada na estrutura **TaggedRequest** na solicitação do CMC. Para obter mais informações, consulte [Atributos do CMC](cmc-attributes.md).
-   O cliente criptografa uma chave privada e a usa para inicializar um [**objeto IX509AttributeArchiveKey.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) O novo **atributo ArchiveKey** é encapsulado em uma **estrutura EnvelopedData.**

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

-   O cliente cria um hash SHA-1 da chave criptografada e o usa para inicializar um objeto [**IX509AttributeArchiveKeyHash.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   O cliente recupera a [**coleção CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) da solicitação do CMC e adiciona os atributos **ArchiveKey** e **ArchiveKeyHash** a ela. Os atributos são colocados na estrutura **TaggedAttributes** da solicitação do CMC.
-   O cliente usa a solicitação do CMC para inicializar um [**objeto IX509CertificateRequestPkcs7.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) Isso coloca a solicitação do CMC no **campo contentInfo** da estrutura SignedData do PKCS \#  7.
-   O **atributo ArchiveKeyHash** é assinado e colocado na sequência **authenticatedAttributes** da **estrutura SignerInfo.**
-   O atributo **ArchiveKey** é colocado na sequência **unauthenticatedAttributes** da estrutura **SignerInfo** associada ao signerador primário da mensagem PKCS \# 7.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos com suporte](supported-attributes.md)
</dt> </dl>

 

 



