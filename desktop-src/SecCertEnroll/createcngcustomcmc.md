---
description: Cria um objeto de solicitação CMC com base em uma solicitação PKCS 10 aninhada interna \# .
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: createCNGCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669a52901981ea910ee3d1704ba892fb96664470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296195"
---
# <a name="createcngcustomcmc"></a>createCNGCustomCMC

O exemplo createCNGCustomCMC cria um objeto de solicitação CMC por meio de uma solicitação PKCS 10 aninhada interna \# . A solicitação interna é criada usando uma [*chave privada*](/windows/desktop/SecGloss/p-gly)assimétrica. A chave privada é criada usando o provedor criptográfico da API de criptografia: próxima geração (CNG) e o algoritmo especificado na linha de comando. Opções personalizadas, como política de exportação e nível de proteção de chave, também são definidas na chave privada.

## <a name="location"></a>Local

Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ createCNGCustomCMC.

## <a name="discussion"></a>Discussão

O exemplo de createCNGCustomCMC:

1.  Processa os seguintes argumentos de linha de comando:
    -   O nome de um [*provedor de serviços de criptografia*](/windows/desktop/SecGloss/c-gly) CNG (CSP).
    -   O nome do algoritmo usado para gerar uma chave privada assimétrica.
    -   O nome do algoritmo usado para [*aplicar o hash*](/windows/desktop/SecGloss/h-gly) à [*solicitação de certificado*](/windows/desktop/SecGloss/c-gly).
    -   Um arquivo de saída no qual salvar a solicitação de certificado.
    -   Uma cadeia de caracteres opcional (AlternateSignature) que, se presente, especifica que um algoritmo de assinatura discreto em vez de combinado seja usado. Para obter mais informações, consulte a propriedade [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) .
2.  Cria um objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) e define as seguintes propriedades:
    -   [**LegacyCsp**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [**ProviderName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [**Algoritmo**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [**Proteção contra keyprotection**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [**ExportPolicy**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  Cria uma chave privada assimétrica.
4.  Cria um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e inicializa-o usando a chave privada.
5.  Cria um objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e o inicializa usando o objeto de \# solicitação PKCS 10 criado na etapa 4.
6.  Define o sinalizador de algoritmo de assinatura alternativo como **Variant \_ true** ou **Variant \_ false** , dependendo se uma cadeia de caracteres de assinatura alternativa é especificada na linha de comando. Para obter mais informações, consulte [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).
7.  Cria um [](/windows/desktop/SecGloss/h-gly) [*identificador de objeto*](/windows/desktop/SecGloss/o-gly) de algoritmo de hash (OID) do nome do algoritmo especificado na linha de comando e define o OID no objeto de solicitação CMC.
8.  Assina a solicitação de certificado e a codifica usando [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).
9.  Recupera uma cadeia de caracteres que contém a solicitação codificada de certificado CMC e salva-a em um arquivo. A função EncodeToFileW é definida em EnrollCommon. cpp.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solicitação de CMC](cmc-request.md)
</dt> <dt>

[\#Solicitação PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
