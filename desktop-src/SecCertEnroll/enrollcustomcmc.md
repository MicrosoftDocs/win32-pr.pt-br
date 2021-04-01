---
description: Cria uma solicitação de certificado CMC e registra um computador em uma hierarquia de certificado.
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: enrollCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2910e6a6ca784aaeb9ca97dc8de106932bd64c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647458"
---
# <a name="enrollcustomcmc"></a>enrollCustomCMC

O exemplo enrollCustomCMC cria uma solicitação de certificado CMC e registra um computador em uma hierarquia de certificado.

## <a name="location"></a>Local

Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ enrollCustomCMC.

## <a name="discussion"></a>Discussão

O exemplo de enrollCustomCMC:

1.  Processa os seguintes argumentos de linha de comando:
    -   Um par de nome/valor personalizado para adicionar à solicitação de certificado.
    -   Um nome de entidade alternativo.
    -   Um OID (identificador de objeto) para a extensão EKU (uso avançado de chave).
2.  Cria um objeto de solicitação [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e inicializa-o usando o contexto do computador.
3.  Usa a \# solicitação PKCS 10 para inicializar um objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .
4.  Cria um objeto [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) usando o OID especificado na linha de comando e o adiciona à coleção de extensões para a solicitação CMC.
5.  Cria o objeto [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) usando o nome especificado na linha de comando, adiciona-o à coleção [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) , usa a coleção para inicializar uma extensão [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) e a adiciona à coleção de extensões para a solicitação CMC.
6.  Cria um objeto [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) usando o nome e o valor especificados na linha de comando e adiciona-o à coleção [**IX509NAMEVALUEPAIRS**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) na solicitação CMC.
7.  Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , inicializa-o usando o objeto de solicitação CMC e recupera uma cadeia de caracteres que contém uma solicitação codificada em base64.
8.  Cria um objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e o usa para recuperar uma cadeia de caracteres que contém a configuração da autoridade de certificação.
9.  Cria um objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) do CryptoAPI e o usa mais as cadeias de caracteres que contêm a configuração da AC e a solicitação de certificado para enviar a solicitação para a autoridade de certificação.
10. Verifica o status de envio e, se for bem-sucedido, instala o certificado no repositório de certificados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solicitação de CMC](cmc-request.md)
</dt> <dt>

[\#Solicitação PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> </dl>

 

 
