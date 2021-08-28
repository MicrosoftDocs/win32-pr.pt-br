---
description: Processo para decodificar dados assinados.
ms.assetid: 803220d0-7963-4fc4-8451-a979e54a9cc3
title: Decodificação de dados assinados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3466736f6c8aab36184c02b918625a609a83c78c6f0142d3201d4c264d67441
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875676"
---
# <a name="decoding-signed-data"></a>Decodificação de dados assinados

O processo geral a seguir decodifica um [*tipo de dados assinado.*](../secgloss/s-gly.md)

**Para decodificar uma mensagem assinada**

1.  Obter um ponteiro para o BLOB codificado.
2.  Chame [**CryptMsgOpenToDecode,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)passando os argumentos necessários.
3.  Chame [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) uma vez, passando o handle recuperado na etapa 2 e um ponteiro para os dados que devem ser decodificados. Isso faz com que as ações apropriadas sejam tomadas na mensagem, dependendo do tipo de mensagem.
4.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando o handle recuperado na etapa 2 e os tipos de parâmetro apropriados para acessar os dados decodificados. Por exemplo, passe o CMSG \_ CONTENT \_ PARAM para obter um ponteiro para o conteúdo decodificado.

O processo geral a seguir verifica a assinatura de uma mensagem assinada decodificada.

**Para verificar a assinatura de uma mensagem decodificada assinada**

1.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando o handle de mensagem e o PARAM DE INFORMAÇÕES DO CERTIFICADO DO SIGNER DO CMSG para obter as INFORMAÇÕES DE CERTIFICADO do \_ signante da \_ \_ \_ mensagem. [**\_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)
2.  Chame [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) para abrir um repositório temporário inicializado com os certificados da mensagem.
3.  Chame [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) para obter as INFORMAÇÕES de [**CERTIFICADO \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) do signante dos certificados incluídos na mensagem.
4.  Chame [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passando CTRL VERIFY SIGNATURE do CMSG \_ para verificar as \_ \_ assinaturas.
5.  Chame [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para fechar a mensagem.

O resultado desses procedimentos é que a assinatura é verificada e um ponteiro é recuperado para o conteúdo de mensagem decodificado obtido na etapa 4 do procedimento para decodificar uma mensagem assinada.

Para obter detalhes de codificação em C, consulte Programa C de [exemplo: assinatura, codificação,](example-c-program-signing-encoding-decoding-and-verifying-a-message.md)decodificação e verificação de uma mensagem .

 

 
