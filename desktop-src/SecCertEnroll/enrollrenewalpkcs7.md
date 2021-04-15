---
description: Cria um \# objeto de solicitação PKCS 7 para renovar um certificado existente. O objeto de solicitação usa um novo par de chaves, mas retém o provedor criptográfico associado ao certificado que está sendo renovado.
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8795758a2744dcee07a100f87eb1db0a1af49eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505973"
---
# <a name="enrollrenewalpkcs7"></a>enrollRenewalPKCS7

O exemplo enrollRenewalPKCS7 cria um \# objeto de solicitação PKCS 7 para renovar um certificado existente. O objeto de solicitação usa um novo par de chaves, mas retém o provedor criptográfico associado ao certificado que está sendo renovado.

## <a name="location"></a>Local

Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ enrollRenewalPKCS7.

## <a name="discussion"></a>Discussão

O exemplo de enrollRenewalPKCS7:

1.  Processa os argumentos de linha de comando. A linha de comando deve conter o nome do modelo usado para criar a solicitação de certificado.
2.  Recupera um certificado existente usando o nome do modelo especificado na linha de comando ou, se um certificado não puder ser encontrado, tentará registrá-lo usando o modelo. As funções findCertByTemplate e enrollCertByTemplate são definidas em enrollCommon. cpp.
3.  Verifica a cadeia de certificados e converte o certificado em um **BSTR**.
4.  Cria um objeto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) e o inicializa usando o certificado existente. Como o parâmetro *inheritoptions* é definido como InheritDefault, um novo par de chaves é criado para a solicitação, mas o provedor criptográfico no certificado existente é usado. Para obter mais informações, consulte o método [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) .
5.  Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , inicializa-o usando o \# objeto de solicitação PKCS 7, tenta registrá-lo com a AC e monitora o status do processo de registro. A função checkEnrollStatus é definida em enrollCommon. cpp.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solicitação de CMC](cmc-request.md)
</dt> <dt>

[\#Solicitação de renovação PKCS 7](pkcs--7--renewal-request.md)
</dt> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> </dl>

 

 



