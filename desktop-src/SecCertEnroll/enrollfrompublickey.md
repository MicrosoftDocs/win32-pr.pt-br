---
description: Inicializa um objeto de solicitação de certificado PKCS 10, o envolve em um objeto de solicitação do CMC, envia a solicitação do CMC para uma AC (autoridade de certificação) corporativa e salva o certificado retornado pela AC em \# um arquivo.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: enrollFromPublicKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0346e2966dc9109ed9413022ead4eda487c37c2ac66ad9da42d2dcee2445032
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780045"
---
# <a name="enrollfrompublickey"></a>enrollFromPublicKey

O exemplo enrollFromPublicKey inicializa um objeto de solicitação de certificado PKCS 10, o envolve em um objeto de solicitação do CMC, envia a solicitação do CMC para uma AC (autoridade de certificação) corporativa e salva o certificado retornado pela AC em \# um arquivo.

## <a name="location"></a>Localização

Quando você instala o Microsoft Windows Software Development Kit (SDK), o exemplo é instalado, por padrão, na pasta *%ProgramFiles%* \\ SDKs da Microsoft Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollFromPublicKey.

## <a name="discussion"></a>Discussão

O exemplo enrollFromPublicKey:

1.  Processa os seguintes argumentos de linha de comando:
    -   O nome de um modelo de certificado.
    -   O nome de um arquivo no qual salvar o certificado instalado como uma matriz de byte codificada em base64.
    -   Um nome de modelo de certificado de assinatura opcional. O modelo será usado para criar um certificado de assinatura se nenhum existir no armazenamento de certificados.
2.  Cria um objeto de chave privada [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) e chama o método Create para criar uma chave privada assimétrica usando os valores padrão de provedor criptográfico, tamanho da chave e [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) para o computador atual. [](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create)
3.  Recupera a parte da chave pública do [**objeto IX509PrivateKey.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
4.  Cria [**um objeto IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e o inicializa usando o modelo especificado na linha de comando e na chave pública.
5.  Cria um [**objeto IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e o inicializa usando o objeto de solicitação PKCS \# 10.
6.  Recupera um certificado de assinatura existente ou, se não for possível encontrar um, cria uma solicitação de certificado do modelo especificado na linha de comando e tenta inscreveu-lo. FindCertByKeyUsage é definido em enrollCommon.cpp.
7.  Verifica a cadeia de certificados.
8.  Cria um objeto [**ISignerCertificate,**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) inicializa-o usando o certificado de assinatura, recupera a coleção [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) do objeto de solicitação do CMC e adiciona o objeto de certificado de assinatura à coleção.
9.  Codifica a solicitação do CMC usando [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).
10. Cria um [**objeto ICertConfig e**](/windows/desktop/api/certcli/nn-certcli-icertconfig) o usa para recuperar uma cadeia de caracteres que contém a configuração da AC.
11. Cria um objeto CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) e o usa mais as cadeias de caracteres que contêm a configuração da AC e a solicitação de certificado para enviar a solicitação à AC.
12. Verifica o status do processo de registro e salva o certificado instalado em um arquivo. A função EncodeToFileW é definida em enrollCommon.cpp.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solicitação do CMC](cmc-request.md)
</dt> <dt>

[Solicitação PKCS \# 10](pkcs--10-request.md)
</dt> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> </dl>

 

 
