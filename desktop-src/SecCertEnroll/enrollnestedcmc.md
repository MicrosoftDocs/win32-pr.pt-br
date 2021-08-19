---
description: Lê uma solicitação de certificado CMC existente de um arquivo, a encapsula em outra solicitação de CMC, assina essa solicitação externa, envia-a para uma autoridade de certificação (CA) e salva a resposta do certificado da autoridade de certificação em um arquivo.
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: enrollNestedCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b55c2957fc04e8bd9a088d3a07ed10c639c29d27dd1262b34709a9215c6c8b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882936"
---
# <a name="enrollnestedcmc"></a>enrollNestedCMC

O exemplo enrollNestedCMC lê uma solicitação de certificado CMC existente de um arquivo, a encapsula em outra solicitação de CMC, assina essa solicitação externa, envia-a para uma autoridade de certificação (CA) e salva a resposta do certificado da autoridade de certificação em um arquivo.

## <a name="location"></a>Localização

quando você instala o Microsoft Windows Software Development Kit (SDK), o exemplo é instalado, por padrão, na pasta *% programfiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ samples \\ X509 Certificate enrollment \\ VC \\ enrollNestedCMC.

## <a name="discussion"></a>Discussão

O exemplo de enrollNestedCMC:

1.  Processa os seguintes argumentos de linha de comando:
    -   O nome do arquivo de entrada.
    -   O nome do arquivo de saída.
    -   Um modelo de solicitação opcional.
2.  Lê uma solicitação CMC existente de um arquivo como uma matriz de bytes codificada em base63, converte a matriz de bytes em um **BSTR**, cria um objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e usa o **BSTR** para inicializar o objeto de solicitação. O objeto inicializado se torna a solicitação interna.
3.  Usa o objeto de solicitação interna criado e inicializado na etapa anterior para inicializar outra solicitação CMC.
4.  Recupera um certificado de autenticação existente ou, se não for possível encontrar um, cria uma solicitação de certificado do modelo especificado na linha de comando e tenta registrá-lo. As funções findCertByTemplate e enrollCertByTemplate são definidas em enrollCommon. cpp.
5.  Recupera a coleção [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) da solicitação CMC externa, cria um novo objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , inicializa-o usando o certificado de autenticação recuperado e o adiciona à coleção.
6.  codifica a solicitação CMC usando Distinguished Encoding Rules (DER) e recupera a solicitação como um **BSTR**.
7.  Cria um objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e o usa para recuperar uma cadeia de caracteres que contém a configuração da autoridade de certificação.
8.  Cria um objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) do CryptoAPI e o usa mais as cadeias de caracteres que contêm a configuração da AC e a solicitação de certificado para enviar a solicitação para a autoridade de certificação.
9.  Verifica o status do processo de registro e salva a resposta do certificado da autoridade de certificação em um arquivo. A função EncodeToFileW é definida em enrollCommon. cpp.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solicitação de CMC](cmc-request.md)
</dt> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> </dl>

 

 
