---
description: Tarefas gerais necessárias para decodificar uma mensagem envelopada.
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: Decodificando dados envelopado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1a0ba12e967f5a0cd56347c0839ce9fca40f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563039"
---
# <a name="decoding-enveloped-data"></a>Decodificando dados envelopado

As tarefas gerais necessárias para decodificar uma mensagem envelopada são descritas na ilustração a seguir e descritas na lista que a segue.

![decodificando dados envelopado](images/decemsg.png)

A sequência de eventos para decodificar dados envelopos usando o gerenciamento de chaves de transporte de chaves, conforme descrito na ilustração anterior, é a seguinte:

-   Um ponteiro para a mensagem [*digitalmente envelopada*](../secgloss/d-gly.md) é recuperado.
-   Um [*repositório de certificados*](../secgloss/c-gly.md) é aberto.
-   A partir da mensagem, a ID do destinatário (My ID) é recuperada.
-   A ID do destinatário é usada para recuperar o certificado.
-   A [*chave privada*](../secgloss/p-gly.md) associada a esse certificado é recuperada.
-   A chave privada é usada para descriptografar a chave [*simétrica*](../secgloss/s-gly.md) ([*sessão*](../secgloss/s-gly.md)).
-   O algoritmo de criptografia é recuperado da mensagem.
-   Usando a chave privada e o algoritmo de criptografia, os dados são descriptografados.

O procedimento a seguir usa funções de mensagem de nível baixo para realizar as tarefas que você acabou de listar.

**Para decodificar uma mensagem envelopada**

1.  Obtenha um ponteiro para o BLOB codificado.
2.  Chame [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passando os argumentos necessários.
3.  Chame [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) uma vez, passando o identificador recuperado na etapa 2 e um ponteiro para os dados que serão decodificados. Isso faz com que as ações apropriadas sejam executadas na mensagem, dependendo do tipo de mensagem.
4.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando o identificador recuperado na etapa 2 e CMSG \_ tipo \_ param para verificar se a mensagem é do tipo de dados Envelopado.
5.  Novamente, chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando \_ o parâmetro de tipo de conteúdo interno CMSG \_ \_ \_ para obter o tipo de dados do [*conteúdo interno*](../secgloss/i-gly.md).
6.  Se o tipo de dados de conteúdo interno for **dado**, continue a descriptografar e decodificar o conteúdo. Caso contrário, execute um procedimento de decodificação apropriado para o tipo de dados Content.
7.  Supondo que o tipo de conteúdo interno seja "data", inicialize a estrutura [**CMSG \_ Ctrl \_ Decrypt \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) dados e chame [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passando CMSG \_ Ctrl \_ Decrypt e o endereço da estrutura. O conteúdo será descriptografado.
8.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando no \_ parâmetro de conteúdo CMSG \_ para obter um ponteiro para o blob de dados de conteúdo decodificado (cadeia de caracteres de **byte** ).
9.  Chame [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para fechar a mensagem.

O resultado desse procedimento é que a mensagem é decodificada e descriptografada e um ponteiro é recuperado para o BLOB de dados de conteúdo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Programa C de exemplo: codificando uma mensagem envelopada e assinada](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
