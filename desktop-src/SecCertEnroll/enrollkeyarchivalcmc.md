---
description: Cria uma solicitação de certificado CMC para arquivar uma chave privada em uma autoridade de certificação (CA).
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: enrollKeyArchivalCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 144f5f063834c156da5058fbc34f66ebdb76eb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758170"
---
# <a name="enrollkeyarchivalcmc"></a>enrollKeyArchivalCMC

O exemplo enrollKeyArchivalCMC cria uma solicitação de certificado CMC para arquivar uma chave privada em uma autoridade de certificação (CA). Para obter mais informações, consulte [solicitação de arquivamento de chave CMC](cmc-key-archival-request.md).

## <a name="location"></a>Local

Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ enrollKeyArchivalCMC.

## <a name="discussion"></a>Discussão

O exemplo de enrollKeyArchivalCMC:

1.  Processa os argumentos de linha de comando. A linha de comando deve conter o nome do modelo de certificado a ser usado para o registro.
2.  Cria um objeto de solicitação de certificado [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e o inicializa para um contexto de usuário final usando o nome do modelo.
3.  Define a propriedade [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) na solicitação CMC.
4.  Cria um objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e o usa para recuperar uma cadeia de caracteres que contém a configuração da autoridade de certificação.
5.  Cria um objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) do CryptoAPI e o usa para recuperar o certificado do Exchange para a autoridade de certificação.
6.  Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , inicializa-o usando a solicitação CMC, cria uma cadeia de caracteres codificada em base64 que contém a solicitação de arquivamento de chave e a envia para a autoridade de certificação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solicitação de arquivamento de chave CMC](cmc-key-archival-request.md)
</dt> <dt>

[Solicitação de CMC](cmc-request.md)
</dt> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> </dl>

 

 
