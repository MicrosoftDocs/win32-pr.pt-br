---
description: A criptografia de chave pública depende de um par de chaves pública e privada para criptografar e descriptografar o conteúdo.
ms.assetid: a85ec2bc-a413-41a6-b3d2-5fa81a9e7bb6
title: Certificados de chave pública X. 509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acd602e9b47cb7825f6d75df0fb74399b914db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555226"
---
# <a name="x509-public-key-certificates"></a><span data-ttu-id="2b083-103">Certificados de chave pública X. 509</span><span class="sxs-lookup"><span data-stu-id="2b083-103">X.509 Public Key Certificates</span></span>

<span data-ttu-id="2b083-104">A criptografia de chave pública depende de um par de chaves pública e privada para criptografar e descriptografar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2b083-104">Public key cryptography relies on a public and private key pair to encrypt and decrypt content.</span></span> <span data-ttu-id="2b083-105">As chaves estão matematicamente relacionadas, e o conteúdo criptografado usando uma das chaves só pode ser descriptografado usando o outro.</span><span class="sxs-lookup"><span data-stu-id="2b083-105">The keys are mathematically related, and content encrypted by using one of the keys can only be decrypted by using the other.</span></span> <span data-ttu-id="2b083-106">A chave privada é mantida em segredo.</span><span class="sxs-lookup"><span data-stu-id="2b083-106">The private key is kept secret.</span></span> <span data-ttu-id="2b083-107">A chave pública normalmente é inserida em um certificado binário e o certificado é publicado em um banco de dados que pode ser acessado por todos os usuários autorizados.</span><span class="sxs-lookup"><span data-stu-id="2b083-107">The public key is typically embedded in a binary certificate, and the certificate is published to a database that can be reached by all authorized users.</span></span>

<span data-ttu-id="2b083-108">O padrão PKI (infraestrutura de chave pública) X. 509 identifica os requisitos para certificados de chave pública robustos.</span><span class="sxs-lookup"><span data-stu-id="2b083-108">The X.509 public key infrastructure (PKI) standard identifies the requirements for robust public key certificates.</span></span> <span data-ttu-id="2b083-109">Um certificado é uma estrutura de dados assinada que associa uma chave pública a uma pessoa, computador ou organização.</span><span class="sxs-lookup"><span data-stu-id="2b083-109">A certificate is a signed data structure that binds a public key to a person, computer, or organization.</span></span> <span data-ttu-id="2b083-110">Os certificados são emitidos por CAS ( [*autoridades de certificação*](/windows/desktop/SecGloss/c-gly) ).</span><span class="sxs-lookup"><span data-stu-id="2b083-110">Certificates are issued by [*certification authorities*](/windows/desktop/SecGloss/c-gly) (CAs).</span></span> <span data-ttu-id="2b083-111">Todas as pessoas que fazem parte para proteger as comunicações que usam uma chave pública contam com a autoridade de certificação para verificar adequadamente as identidades de indivíduos, sistemas ou entidades para as quais ele emite certificados.</span><span class="sxs-lookup"><span data-stu-id="2b083-111">All who are party to secure communications that make use of a public key rely on the CA to adequately verify the identities of the individuals, systems, or entities to which it issues certificates.</span></span> <span data-ttu-id="2b083-112">O nível de verificação normalmente depende do nível de segurança necessário para a transação.</span><span class="sxs-lookup"><span data-stu-id="2b083-112">The level of verification typically depends on the level of security required for the transaction.</span></span> <span data-ttu-id="2b083-113">Se a AC puder verificar adequadamente a identidade do solicitante, ela assinará (criptografa), codificará e emitirá o certificado.</span><span class="sxs-lookup"><span data-stu-id="2b083-113">If the CA can suitably verify the identity of the requester, it signs (encrypts), encodes, and issues the certificate.</span></span>

<span data-ttu-id="2b083-114">Um certificado é uma estrutura de dados assinada que associa uma chave pública a uma entidade.</span><span class="sxs-lookup"><span data-stu-id="2b083-114">A certificate is a signed data structure that binds a public key to an entity.</span></span> <span data-ttu-id="2b083-115">A sintaxe de uma (ASN. 1) de [*notação de sintaxe abstrata*](/windows/desktop/SecGloss/a-gly) para o certificado da versão 3 [*X. 509*](/windows/desktop/SecGloss/x-gly) é mostrada no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="2b083-115">The [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) syntax for the version 3 [*X.509*](/windows/desktop/SecGloss/x-gly) certificate is shown in the following example.</span></span>

``` syntax
-- X.509 signed certificate 

SignedContent ::= SEQUENCE 
{
  certificate         CertificateToBeSigned,
  algorithm           Object Identifier,
  signature           BITSTRING
}
 
-- X.509 certificate to be signed

CertificateToBeSigned ::= SEQUENCE 
{
  version                 [0] CertificateVersion DEFAULT v1,
  serialNumber            CertificateSerialNumber,
  signature               AlgorithmIdentifier,
  issuer                  Name
  validity                Validity,
  subject                 Name
  subjectPublicKeyInfo    SubjectPublicKeyInfo,
  issuerUniqueIdentifier  [1] IMPLICIT UniqueIdentifier OPTIONAL,
  subjectUniqueIdentifier [2] IMPLICIT UniqueIdentifier OPTIONAL,
  extensions              [3] Extensions OPTIONAL
}
```

<span data-ttu-id="2b083-116">Desde sua concepção em 1998, foram evoluídas três versões do padrão de certificado de chave pública X. 509.</span><span class="sxs-lookup"><span data-stu-id="2b083-116">Since its inception in 1998, three versions of the X.509 public key certificate standard have evolved.</span></span> <span data-ttu-id="2b083-117">Conforme mostrado na ilustração a seguir, cada versão sucessiva da estrutura de dados manteve os campos que existiam nas versões anteriores e adicionavam mais.</span><span class="sxs-lookup"><span data-stu-id="2b083-117">As shown by the following illustration, each successive version of the data structure has retained the fields that existed in the previous versions and added more.</span></span>

![certificados x. 509 versões 1, 2 e 3](images/x509certificateversions.png)

<span data-ttu-id="2b083-119">Os tópicos a seguir discutem os campos disponíveis mais detalhadamente:</span><span class="sxs-lookup"><span data-stu-id="2b083-119">The following topics discuss the available fields in more detail:</span></span>

-   [<span data-ttu-id="2b083-120">Campos básicos</span><span class="sxs-lookup"><span data-stu-id="2b083-120">Basic Fields</span></span>](about-basic-fields.md)
-   [<span data-ttu-id="2b083-121">Campos da versão 2</span><span class="sxs-lookup"><span data-stu-id="2b083-121">Version 2 Fields</span></span>](about-version-2-fields.md)
-   [<span data-ttu-id="2b083-122">Extensões da versão 3</span><span class="sxs-lookup"><span data-stu-id="2b083-122">Version 3 Extensions</span></span>](about-version-3-extensions.md)

## <a name="related-topics"></a><span data-ttu-id="2b083-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b083-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b083-124">Infraestrutura de chave pública</span><span class="sxs-lookup"><span data-stu-id="2b083-124">Public Key Infrastructure</span></span>](public-key-infrastructure.md)
</dt> </dl>

 

 
