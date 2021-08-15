---
description: A criptografia de chave pública depende de um par de chaves públicas e privadas para criptografar e descriptografar conteúdo.
ms.assetid: a85ec2bc-a413-41a6-b3d2-5fa81a9e7bb6
title: Certificados de chave pública X.509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1eb40e57114f4509884df3a5ac36e7ae8ea0486817ff300d58f4273d51c123
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903244"
---
# <a name="x509-public-key-certificates"></a>Certificados de chave pública X.509

A criptografia de chave pública depende de um par de chaves públicas e privadas para criptografar e descriptografar conteúdo. As chaves estão matematicamente relacionadas e o conteúdo criptografado usando uma das chaves só pode ser descriptografado usando o outro. A chave privada é mantida em segredo. A chave pública normalmente é inserida em um certificado binário e o certificado é publicado em um banco de dados que pode ser alcançado por todos os usuários autorizados.

O padrão PKI (infraestrutura de chave pública) X.509 identifica os requisitos para certificados de chave pública robustos. Um certificado é uma estrutura de dados assinada que vincula uma chave pública a uma pessoa, computador ou organização. Os certificados são emitidos por autoridades [*de certificação*](/windows/desktop/SecGloss/c-gly) (CAs). Todos os que fazem parte da segurança das comunicações que usam uma chave pública dependem da AC para verificar adequadamente as identidades das pessoas, sistemas ou entidades às quais ela emite certificados. O nível de verificação normalmente depende do nível de segurança necessário para a transação. Se a AC puder verificar a identidade do solicitante, ela assinará (criptografa), codifica e emite o certificado.

Um certificado é uma estrutura de dados assinada que vincula uma chave pública a uma entidade. A sintaxe ASN.1 [*(Abstract Syntax Notation One)*](/windows/desktop/SecGloss/a-gly) para o certificado [*X.509*](/windows/desktop/SecGloss/x-gly) versão 3 é mostrada no exemplo a seguir.

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

Desde sua criação em 1998, três versões do padrão de certificado de chave pública X.509 foram evoluindo. Conforme mostrado pela ilustração a seguir, cada versão sucessiva da estrutura de dados retido os campos que existiam nas versões anteriores e adicionou mais.

![Certificados x.509 versões 1, 2 e 3](images/x509certificateversions.png)

Os tópicos a seguir discutem os campos disponíveis mais detalhadamente:

-   [Campos básicos](about-basic-fields.md)
-   [Campos da versão 2](about-version-2-fields.md)
-   [Extensões da versão 3](about-version-3-extensions.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Infraestrutura de chave pública](public-key-infrastructure.md)
</dt> </dl>

 

 
