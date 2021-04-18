---
description: Descreve as tarefas necessárias para codificar uma mensagem com hash.
ms.assetid: c1a65452-c634-4cc6-9afe-d6bf11d999d1
title: Codificando e decodificando uma mensagem com hash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91d165634c1ae00a59f2c77b1fc5a36b53dbd96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766827"
---
# <a name="encoding-and-decoding-a-hashed-message"></a>Codificando e decodificando uma mensagem com hash

Os dados com hash consistem em conteúdo de qualquer tipo e [*hash*](../secgloss/h-gly.md) do conteúdo. Ele pode ser usado quando for necessário apenas confirmar que o conteúdo da mensagem não foi modificado desde que o hash foi criado.

Ao criar uma mensagem com hash, pode haver vários algoritmos de hash e vários hashes. A ilustração a seguir ilustra as tarefas necessárias para codificar uma mensagem com hash. O procedimento é descrito no texto que segue a ilustração.

![Criando uma mensagem com hash](images/hashmsg.png)

**Para criar uma mensagem com hash**

1.  Obtenha um ponteiro para os dados a serem codificados em hash.
2.  Selecione o algoritmo de hash a ser usado.
3.  Coloque os dados por meio de uma função de hash usando o algoritmo de hash.
4.  Inclua os dados originais para serem codificados em hash, os algoritmos de hash e os hashes na mensagem codificada.

Para usar funções de mensagens de nível baixo para realizar as tarefas que acabaram de ser descritas, use o procedimento a seguir.

**Para aplicar o hash e codificar uma mensagem usando funções de mensagens de nível baixo**

1.  Crie ou recupere o conteúdo a ser transformado em hash.
2.  Obter um provedor criptográfico.
3.  Inicialize a estrutura de [**informações de codificação com hash de CMSG \_ \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) .
4.  Chame [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) para obter o tamanho do blob de mensagens codificadas. Aloque memória para ele.
5.  Chame [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), passando CMSG \_ com hash para o parâmetro *dwMsgType* e um ponteiro para [**CMSG \_ \_ \_ informações de codificação com hash**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) para o parâmetro *pvMsgEncodeInfo* . Como resultado dessa chamada, você obtém um identificador para a mensagem aberta.
6.  Chame [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), passando o identificador recuperado na etapa 5 e um ponteiro para os dados que serão codificados em hash e codificado. Essa função pode ser chamada quantas vezes forem necessárias para concluir o processo de codificação.
7.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando o identificador recuperado na etapa 5 e os tipos de parâmetro apropriados para acessar os dados desejados e codificados. Por exemplo, passe \_ o parâmetro de conteúdo CMSG \_ para obter um ponteiro para toda a mensagem [*PKCS \# 7*](../secgloss/p-gly.md) .

    Se o resultado dessa codificação for ser usado como os [*dados internos*](../secgloss/i-gly.md) de outra mensagem codificada, como uma mensagem envelopada, o \_ parâmetro CMSG Bare \_ Content \_ deverá ser passado. Para ver um exemplo que mostra isso, consulte [código alternativo para codificar uma mensagem envelopada](alternate-code-for-encoding-an-enveloped-message.md).

8.  Feche a mensagem chamando [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

O resultado desse procedimento é uma mensagem codificada que contém os dados originais, os algoritmos de hash e o [*hash*](../secgloss/h-gly.md) desses dados. Um ponteiro para o [*blob*](../secgloss/b-gly.md) de mensagens codificadas é obtido na etapa 7.

Os dois procedimentos a seguir decodificam e, em seguida, verificam os dados com hash.

**Para decodificar dados com hash**

1.  Obtenha um ponteiro para o BLOB codificado.
2.  Chame [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passando os argumentos necessários.
3.  Chame [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) uma vez, passando o identificador recuperado na etapa 2 e um ponteiro para os dados que serão decodificados. Isso faz com que as ações apropriadas sejam executadas na mensagem, dependendo do tipo de mensagem.
4.  Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando o identificador recuperado na etapa 2 e os tipos de parâmetro apropriados para acessar os dados decodificados desejados. Por exemplo, passe \_ o parâmetro de conteúdo CMSG \_ para obter um ponteiro para o conteúdo decodificado.

**Para verificar o hash**

1.  Chame [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passando CMSG \_ Ctrl \_ Verify \_ hash para verificar os hashes.
2.  Chame [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para fechar a mensagem.

Para um programa de exemplo, consulte [exemplo C programa: codificando e decodificando uma mensagem com hash](example-c-program-encoding-and-decoding-a-hashed-message.md).

 

 
