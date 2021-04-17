---
description: Processo para decodificar dados assinados.
ms.assetid: 803220d0-7963-4fc4-8451-a979e54a9cc3
title: Decodificando dados assinados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfd327746c5d0ba8e7089e1c273817b76c16370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754948"
---
# <a name="decoding-signed-data"></a>Decodificando dados assinados

O processo geral a seguir Decodifica um tipo de [*dados assinado*](../secgloss/s-gly.md) .

**Para decodificar uma mensagem assinada**

1.  Obtenha um ponteiro para o BLOB codificado.
2.  Chame [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passando os argumentos necessários.
3.  Chame [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) uma vez, passando o identificador recuperado na etapa 2 e um ponteiro para os dados que serão decodificados. Isso faz com que as ações apropriadas sejam executadas na mensagem, dependendo do tipo de mensagem.
4.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando o identificador recuperado na etapa 2 e os tipos de parâmetro apropriados para acessar os dados decodificados. Por exemplo, passe \_ o parâmetro de conteúdo CMSG \_ para obter um ponteiro para o conteúdo decodificado.

O processo geral a seguir verifica a assinatura de uma mensagem decodificada e assinada.

**Para verificar a assinatura de uma mensagem decodificada e assinada**

1.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando o identificador de mensagem e o \_ parâmetro de informações de certificado do assinante CMSG \_ \_ \_ para obter as [**\_ informações de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) do assinante da mensagem.
2.  Chame [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) para abrir um repositório temporário que é inicializado com os certificados da mensagem.
3.  Chame [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) para obter as informações de [**certificado \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) do assinante dos certificados incluídos na mensagem.
4.  Chame [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passando na CMSG \_ Ctrl de \_ verificação de \_ assinatura para verificar as assinaturas.
5.  Chame [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para fechar a mensagem.

O resultado desses procedimentos é que a assinatura é verificada e um ponteiro é recuperado para o conteúdo da mensagem decodificada obtido na etapa 4 do procedimento para decodificar uma mensagem assinada.

Para obter detalhes de codificação C, consulte [exemplo c programa: assinatura, codificação, decodificação e verificação de uma mensagem](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

 

 
