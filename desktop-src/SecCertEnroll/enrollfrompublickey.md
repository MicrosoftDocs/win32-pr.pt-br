---
description: Inicializa um \# objeto de solicitação de certificado PKCS 10, encapsula-o em um objeto de solicitação CMC, envia a solicitação CMC para uma AC (autoridade de certificação) corporativa e salva o certificado retornado pela autoridade de certificação em um arquivo.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: enrollFromPublicKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b336d04727f4bb4b90674bad6bb6c429465a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647456"
---
# <a name="enrollfrompublickey"></a>enrollFromPublicKey

O exemplo enrollFromPublicKey Inicializa um \# objeto de solicitação de certificado PKCS 10, o encapsula em um objeto de solicitação CMC, envia a solicitação CMC para uma AC (autoridade de certificação) corporativa e salva o certificado retornado pela autoridade de certificação em um arquivo.

## <a name="location"></a>Local

Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ enrollFromPublicKey.

## <a name="discussion"></a>Discussão

O exemplo de enrollFromPublicKey:

1.  Processa os seguintes argumentos de linha de comando:
    -   O nome de um modelo de certificado.
    -   O nome de um arquivo no qual salvar o certificado instalado como uma matriz de bytes codificada em base64.
    -   Um nome de modelo de certificado de assinatura opcional. O modelo é usado para criar um certificado de assinatura se não houver nenhum no repositório de certificados.
2.  Cria um objeto de chave privada [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) e chama o método [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) para criar uma chave privada assimétrica usando o provedor criptográfico padrão, o tamanho da chave e os valores [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) para o computador atual.
3.  Recupera a parte da chave pública do objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) .
4.  Cria um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e o inicializa usando o modelo especificado na linha de comando e a chave pública.
5.  Cria um objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e o inicializa usando o objeto de \# solicitação PKCS 10.
6.  Recupera um certificado de autenticação existente ou, se não for possível encontrar um, cria uma solicitação de certificado do modelo especificado na linha de comando e tenta registrá-lo. O findCertByKeyUsage é definido em enrollCommon. cpp.
7.  Verifica a cadeia de certificados.
8.  Cria um objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , inicializa-o usando o certificado de autenticação, recupera a coleção [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) do objeto de solicitação CMC e adiciona o objeto de certificado de autenticação à coleção.
9.  Codifica a solicitação CMC usando [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).
10. Cria um objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e o usa para recuperar uma cadeia de caracteres que contém a configuração da autoridade de certificação.
11. Cria um objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) do CryptoAPI e o usa mais as cadeias de caracteres que contêm a configuração da AC e a solicitação de certificado para enviar a solicitação para a autoridade de certificação.
12. Verifica o status do processo de registro e salva o certificado instalado em um arquivo. A função EncodeToFileW é definida em enrollCommon. cpp.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solicitação de CMC](cmc-request.md)
</dt> <dt>

[\#Solicitação PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> </dl>

 

 
