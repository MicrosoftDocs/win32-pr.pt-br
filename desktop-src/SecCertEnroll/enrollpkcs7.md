---
description: Cria uma \# solicitação PKCS 7 de um certificado existente herdando as chaves pública e privada e o modelo de certificado.
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34bc7f9d7b7d5ae9fa88db0dd70c177c3aa69da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646779"
---
# <a name="enrollpkcs7"></a>enrollPKCS7

O exemplo enrollPKCS7 cria uma \# solicitação PKCS 7 de um certificado existente herdando as chaves pública e privada e o modelo de certificado. O certificado existente é usado para assinar a solicitação. Este exemplo registra o usuário em uma hierarquia de certificado e instala a resposta do certificado. O exemplo usa um certificado existente para registrar e instalar um novo. Para obter mais informações sobre como renovar um certificado existente, consulte [enrollRenewalPKCS7](enrollrenewalpkcs7.md).

## <a name="location"></a>Localização

Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ enrollPKCS7.

## <a name="discussion"></a>Discussão

O exemplo de enrollPKCS7:

1.  Processa os argumentos de linha de comando. A linha de comando deve conter o nome do modelo de certificado usado para localizar um certificado existente.
2.  Recupera um certificado existente usando o nome do modelo especificado na linha de comando ou, se um certificado não puder ser encontrado, tentará registrar um novo criado usando o modelo. As funções findCertByTemplate e enrollCertByTemplate são definidas em enrollCommon. cpp.
3.  Verifica a cadeia de certificados e converte o certificado em um **BSTR**.
4.  Cria um objeto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) e o inicializa usando o certificado existente. O novo \# objeto de solicitação PKCS 7 herda as chaves pública e privada e o modelo do certificado existente.
5.  Cria um objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , inicializa-o usando o certificado existente e o adiciona ao \# objeto de solicitação PKCS 7.
6.  Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , inicializa-o usando o \# objeto de solicitação PKCS 7, tenta registrá-lo com a AC e monitora o status do processo de registro. A função checkEnrollStatus é definida em enrollCommon. cpp.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solicitação de CMC](cmc-request.md)
</dt> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> </dl>

 

 



