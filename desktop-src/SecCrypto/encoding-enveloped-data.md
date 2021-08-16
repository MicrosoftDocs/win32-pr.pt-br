---
description: A sintaxe da mensagem criptográfica pode ser usada para codificar mensagens envelopadas.
ms.assetid: f35aacda-6827-42e9-b7ac-58dc007fc697
title: Codificando dados Envelopos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3517a956311373d067072899ee71bcdf742990877c7d569bfe4e5ef7f2757e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766752"
---
# <a name="encoding-enveloped-data"></a>Codificando dados Envelopos

Os dados de envelope consistem no conteúdo criptografado de qualquer tipo e chaves de sessão de criptografia de conteúdo criptografado para um ou mais destinatários. As mensagens envelopadas mantêm o conteúdo do segredo da mensagem e permitem que apenas pessoas ou entidades especificadas recuperem o conteúdo.

A sintaxe de mensagem de criptografia (CMS) pode ser usada para codificar mensagens envelopadas. O CMS dá suporte a três técnicas de gerenciamento de chaves: transporte de chave, contrato de chave e chaves de criptografia de chave simétrica distribuídas anteriormente (KEK). Os KEK simétricos distribuídos anteriormente também são conhecidos como distribuição de chaves de lista de endereçamento.

Em cada uma dessas três técnicas, uma única chave de sessão é gerada para criptografar a mensagem envelopada. Os problemas de gerenciamento de chaves lidam com o modo como a chave de sessão é criptografada pelo remetente e descriptografada por um receptor. Uma única mensagem criptografada pode ser distribuída para muitos destinatários usando uma combinação das técnicas de gerenciamento de chaves.

O gerenciamento de chaves de transporte de chave usa a chave pública do destinatário pretendido para criptografar a chave de sessão. O destinatário descriptografa a chave de sessão usando a chave privada associada à chave pública que foi usada para criptografar. Em seguida, o receptor usa a chave de sessão descriptografada para descriptografar os dados de envelope. Quando o transporte de chave é usado, o receptor não confirmou informações sobre a identidade do remetente.

No gerenciamento de contrato de chave, uma chave privada temporária, efêmera Diffie-Hellman é gerada e usada para criptografar a chave de sessão. A chave pública correspondente à chave privada efêmera é incluída como parte das informações de destinatário da mensagem. O destinatário descriptografa a chave de sessão usando a chave efêmera recebida e usa essa chave de sessão descriptografada para descriptografar a mensagem envelopada. Usando o contrato de chave efêmera em conjunto com a chave privada do receptor, o receptor da mensagem confirmava informações sobre a identidade do remetente.

Para o gerenciamento de chaves usando [*chaves simétricas*](../secgloss/s-gly.md)distribuídas anteriormente, cada mensagem inclui a chave de criptografia de conteúdo que foi criptografada com uma chave de criptografia de chave distribuída anteriormente. Os receptores usam a chave de criptografia de chave distribuída anteriormente para descriptografar a chave de criptografia de conteúdo e, em seguida, usam a chave de criptografia de conteúdo descriptografada para descriptografar a mensagem envelopada.

Uma sequência de eventos típica de CMS para codificação de dados envelopes, é mostrada na ilustração a seguir.

![codificando dados envelopos](images/envelmsg.png)

-   Um ponteiro para a mensagem de [*texto não criptografado*](../secgloss/p-gly.md) é recuperado.
-   Uma chave simétrica ([*sessão*](../secgloss/s-gly.md)) é gerada.
-   A [*chave simétrica*](../secgloss/s-gly.md) e o algoritmo de criptografia especificado são usados para criptografar os dados da mensagem.
-   Um [*repositório de certificados*](../secgloss/c-gly.md) é aberto.
-   O certificado do destinatário é recuperado do repositório.
-   A [*chave pública*](../secgloss/p-gly.md) é recuperada do certificado do destinatário.
-   Usando a chave pública do destinatário, a chave simétrica é criptografada.
-   Do certificado do destinatário, a ID do destinatário é recuperada.
-   As informações a seguir estão incluídas na mensagem digitalmente envelopada: o algoritmo de criptografia de dados, os dados criptografados, a chave simétrica criptografada e a estrutura de informações do destinatário.

Para usar funções de mensagens de nível baixo para realizar as tarefas típicas listadas, use o procedimento a seguir.

**Para codificar uma mensagem envelopada**

1.  Crie ou recupere o conteúdo.
2.  Obter um provedor criptográfico.
3.  Obter um certificado de destinatário.
4.  Inicialize a estrutura de [**\_ \_ \_ informações de codificação envelopada do CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) .
5.  Chame [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) para obter o tamanho do blob de mensagens codificadas. Aloque memória para ele.
6.  Chame [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), passando CMSG \_ envelopeed para *dwMsgType* e um ponteiro para [**CMSG \_ \_ \_ informações de codificação envelopadas**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) para *pvMsgEncodeInfo*. Como resultado dessa chamada, você receberá um identificador para a mensagem aberta.
7.  Chame [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), passando o identificador recuperado na etapa 6 e um ponteiro para os dados que serão criptografados, envelopos e codificados. Essa função pode ser chamada quantas vezes forem necessárias para concluir o processo de codificação.
8.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando o identificador recuperado na etapa 6 e os tipos de parâmetro apropriados para acessar os dados desejados e codificados. Por exemplo, passe \_ o parâmetro de conteúdo CMSG \_ para obter um ponteiro para toda a \# mensagem PKCS 7.

    Se o resultado dessa codificação for ser usado como os [*dados internos*](../secgloss/i-gly.md) para outra mensagem codificada, como uma mensagem envelopada, o \_ parâmetro CMSG Bare \_ Content \_ param deverá ser passado. Para obter um exemplo, consulte [código alternativo para codificar uma mensagem envelopada](alternate-code-for-encoding-an-enveloped-message.md).

9.  Feche a mensagem chamando [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

O resultado desse procedimento é uma mensagem codificada que contém os dados criptografados, a [*chave simétrica*](../secgloss/s-gly.md) que é criptografada com as chaves públicas do destinatário e as estruturas de dados de informações de destinatário. A combinação de conteúdo criptografado e uma chave simétrica criptografada para um destinatário é um [*envelope digital*](../secgloss/d-gly.md) para esse destinatário. Qualquer tipo de conteúdo pode ser envelopado para vários destinatários.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Programa C de exemplo: codificando uma mensagem envelopada e assinada](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
