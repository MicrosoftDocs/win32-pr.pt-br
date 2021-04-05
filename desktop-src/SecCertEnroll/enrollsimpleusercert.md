---
description: Registra um usuário final com uma autoridade de certificação (CA) usando um modelo, o nome da entidade e o comprimento, em bits, da chave.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: enrollSimpleUserCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0956455afa814af54cc86661f2d7733a6d16dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011246"
---
# <a name="enrollsimpleusercert"></a>enrollSimpleUserCert

O exemplo enrollSimpleUserCert registra um usuário final com uma autoridade de certificação (CA) usando um modelo, o nome da entidade e o comprimento, em bits, da chave.

## <a name="location"></a>Local

Quando você instala o SDK (Software Development Kit) do Microsoft Windows, uma versão em C++ do exemplo é instalada, por padrão, na pasta *% ProgramFiles%%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ enrollSimpleUserCert. Uma versão do C# é instalada na pasta *% ProgramFiles%%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ X509 Certificate Enroll \\ \\ EnrollSimpleUserCert.

## <a name="discussion"></a>Discussão

O exemplo de enrollSimpleUserCert:

1.  Processa os argumentos de linha de comando. A linha de comando deve conter o nome do modelo, o nome da entidade e o comprimento da chave.
2.  Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e o inicializa usando o modelo.
3.  Recupera o objeto de solicitação de certificado interno do objeto de registro e o consulta para o objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) . A solicitação mais interna é sempre uma \# solicitação PKCS 10.
4.  Recupera o objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) da solicitação PKCS \# 10 e define o comprimento da chave especificado na linha de comando.
5.  Cria um objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , usa-o para codificar o nome da entidade X. 500 e adiciona o nome à \# solicitação PKCS 10.
6.  Tenta registrar o usuário final com a AC e monitora o progresso do processo de registro. A função checkEnrollStatus é definida em enrollCommon. cpp.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\#Solicitação PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> </dl>

 

 



