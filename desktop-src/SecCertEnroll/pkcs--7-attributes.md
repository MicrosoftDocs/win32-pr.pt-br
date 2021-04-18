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
# <a name="pkcs-7-attributes"></a>\#Atributos PKCS 7

PKCS \# 7 é um padrão de sintaxe de mensagem criptográfica. Uma \# mensagem PKCS 7 não faz, por si só, constituir uma solicitação de certificado, mas pode encapsular uma \# solicitação PKCS 10 ou CMC em uma estrutura **ContentInfo** ASN. 1 usando um dos seguintes tipos de conteúdo. O encapsulamento permite que você adicione funcionalidades extras, como várias assinaturas, que não estão disponíveis de outra forma.

-   **Dados**
-   **SignedData**
-   **EnvelopedData**
-   **SignedAndEnvelopedData**
-   **DigestedData**
-   **EncryptedData**

Os atributos podem ser adicionados aos campos **authenticatedAttributes** e **unauthenticatedAttributes** do tipo de conteúdo **SignedData** .

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

O processo necessário para arquivar a chave privada de um cliente em uma autoridade de certificação (CA) fornece um exemplo abrangente de como os atributos autenticados (assinados) e os atributos não autenticados podem ser usados:

-   O cliente cria um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e adiciona os dados apropriados para o tipo de certificado que está sendo solicitado.
-   O cliente usa a \# solicitação PKCS 10 para inicializar um objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) . A \# solicitação PKCS 10 é colocada na estrutura **TaggedRequest** na solicitação CMC. Para obter mais informações, consulte [atributos CMC](cmc-attributes.md).
-   O cliente criptografa uma chave privada e a usa para inicializar um objeto [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) . O novo atributo **ArchiveKey** é encapsulado em uma estrutura **EnvelopedData** .

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

-   O cliente cria um hash SHA-1 da chave criptografada e a usa para inicializar um objeto [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) .
-   O cliente recupera a coleção [**criptattributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) da solicitação CMC e adiciona os atributos **ArchiveKey** e **ArchiveKeyHash** a ela. Os atributos são colocados na estrutura **marcadoattributes** da solicitação CMC.
-   O cliente usa a solicitação CMC para inicializar um objeto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) . Isso coloca a solicitação CMC no campo **contentInfo** da \# estrutura **SignedData** do PKCS 7.
-   O atributo **ArchiveKeyHash** é assinado e colocado na sequência **AuthenticatedAttributes** da estrutura **SignerInfo** .
-   O atributo **ArchiveKey** é colocado na sequência **UnauthenticatedAttributes** da estrutura **SignerInfo** associada ao signatário principal da \# mensagem PKCS 7.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos com suporte](supported-attributes.md)
</dt> </dl>

 

 



