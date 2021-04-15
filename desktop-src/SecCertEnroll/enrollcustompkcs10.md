---
description: Cria uma solicitação PKCS \# 10 personalizada, envia-a para uma CA (autoridade de certificação) autônoma e instala o certificado emitido no repositório de certificados.
ms.assetid: dcb69d7e-457e-457b-9eea-15676ed710aa
title: enrollCustomPKCS10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ad95f483d4bc82136865e94a70ad46e90e1c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747646"
---
# <a name="enrollcustompkcs10"></a>enrollCustomPKCS10

O exemplo enrollCustomPKCS10 cria uma solicitação PKCS \# 10 personalizada, envia-a para uma CA (autoridade de certificação) autônoma e instala o certificado emitido no repositório de certificados. Uma autoridade de certificação autônoma não requer Active Directory e não usa modelos.

## <a name="location"></a>Local

Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ enrollCustomPKCS10.

## <a name="discussion"></a>Discussão

O exemplo de enrollCustomPKCS10:

1.  Processa os argumentos de linha de comando. A linha de comando deve conter o nome da entidade do certificado X. 500, o nome do email (RFC822) e um OID (identificador de objeto) de uso avançado de chave (EKU). Por exemplo, você pode especificar os seguintes argumentos para registrar *user1@example.com* :
    -   Nome da entidade: "*CN = Usuário1, DC = exemplo, DC = com*"
    -   Nome do RFC822: *user1@example.com*
    -   OID EKU de autenticação de cliente: 1.3.6.1.5.5.7.3.2
2.  Cria um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e o inicializa para o usuário final especificando o valor **ContextUser** da enumeração [**X509CertificateEnrollmentContext**](/windows/desktop/api/CertEnroll/ne-certenroll-x509certificateenrollmentcontext) .
3.  Cria um objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , usa o objeto para codificar o nome da entidade para uma matriz de bytes e adiciona a matriz ao \# objeto de solicitação PKCS 10.
4.  Cria um objeto [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) , inicializa-o usando o OID (identificador de objeto EKU) especificado na linha de comando, cria uma coleção [**IObjectIds**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids) , adiciona o novo objeto **IObjectId** (EKU) à coleção, usa a coleção para inicializar um objeto [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) e adiciona esse objeto à solicitação.
5.  Cria um objeto [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) , inicializa-o usando o nome de RFC822 especificado na linha de comando, cria uma coleção [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) , adiciona o novo objeto **IAlternativeName** (nome rfc822) à coleção, cria um objeto [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) e adiciona esse objeto à solicitação.
6.  Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , inicializa-o usando o objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e recupera uma cadeia de caracteres que contém uma solicitação codificada em base64.
7.  Cria um objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e o usa para recuperar uma cadeia de caracteres que contém a configuração da autoridade de certificação.
8.  Cria um objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) do CryptoAPI e o usa mais as cadeias de caracteres que contêm a configuração da AC e a solicitação de certificado para enviar a solicitação para a autoridade de certificação.
9.  Verifica o status de envio e, se o registro for bem-sucedido, instala o certificado no repositório de certificados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\#Solicitação PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> </dl>

 

 
