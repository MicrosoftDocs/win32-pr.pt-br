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
# <a name="x509-public-key-certificates"></a>Certificados de chave pública X. 509

A criptografia de chave pública depende de um par de chaves pública e privada para criptografar e descriptografar o conteúdo. As chaves estão matematicamente relacionadas, e o conteúdo criptografado usando uma das chaves só pode ser descriptografado usando o outro. A chave privada é mantida em segredo. A chave pública normalmente é inserida em um certificado binário e o certificado é publicado em um banco de dados que pode ser acessado por todos os usuários autorizados.

O padrão PKI (infraestrutura de chave pública) X. 509 identifica os requisitos para certificados de chave pública robustos. Um certificado é uma estrutura de dados assinada que associa uma chave pública a uma pessoa, computador ou organização. Os certificados são emitidos por CAS ( [*autoridades de certificação*](/windows/desktop/SecGloss/c-gly) ). Todas as pessoas que fazem parte para proteger as comunicações que usam uma chave pública contam com a autoridade de certificação para verificar adequadamente as identidades de indivíduos, sistemas ou entidades para as quais ele emite certificados. O nível de verificação normalmente depende do nível de segurança necessário para a transação. Se a AC puder verificar adequadamente a identidade do solicitante, ela assinará (criptografa), codificará e emitirá o certificado.

Um certificado é uma estrutura de dados assinada que associa uma chave pública a uma entidade. A sintaxe de uma (ASN. 1) de [*notação de sintaxe abstrata*](/windows/desktop/SecGloss/a-gly) para o certificado da versão 3 [*X. 509*](/windows/desktop/SecGloss/x-gly) é mostrada no exemplo a seguir.

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

Desde sua concepção em 1998, foram evoluídas três versões do padrão de certificado de chave pública X. 509. Conforme mostrado na ilustração a seguir, cada versão sucessiva da estrutura de dados manteve os campos que existiam nas versões anteriores e adicionavam mais.

![certificados x. 509 versões 1, 2 e 3](images/x509certificateversions.png)

Os tópicos a seguir discutem os campos disponíveis mais detalhadamente:

-   [Campos básicos](about-basic-fields.md)
-   [Campos da versão 2](about-version-2-fields.md)
-   [Extensões da versão 3](about-version-3-extensions.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Infraestrutura de chave pública](public-key-infrastructure.md)
</dt> </dl>

 

 
