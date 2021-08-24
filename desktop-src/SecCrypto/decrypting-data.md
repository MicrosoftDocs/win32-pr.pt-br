---
description: Apresenta as etapas para descriptografar uma mensagem criptografada.
ms.assetid: 6af7dd28-325e-431a-9cdb-109d93af6302
title: Descriptografando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 600903d7a3060c83cd7cd0a85e92f96efe4fb0cfa30c2936c5546f71138b6854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875686"
---
# <a name="decrypting-data"></a>Descriptografando dados

Esta seção apresenta as etapas para descriptografar uma mensagem criptografada.

**Para descriptografar uma mensagem criptografada**

1.  Obter um ponteiro para a mensagem enveloada digitalmente.
2.  Abra um armazenamento de certificados.
3.  Na mensagem, recupere o identificador do destinatário (Minha ID).
4.  Use o identificador de destinatário para recuperar o certificado.
5.  Obter a chave privada do certificado.
6.  Use a chave privada para descriptografar a chave simétrica (sessão).
7.  Recupere o algoritmo de criptografia da mensagem.
8.  Usando a chave de sessão descriptografada e o algoritmo de criptografia, descriptografe os dados.

[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) faz todas as tarefas para descriptografar uma mensagem; no entanto, a inicialização de estruturas e outros dados ainda é necessária.

**Para descriptografar dados usando CryptDecryptMessage**

1.  Obter um ponteiro para o BLOB criptografado.
2.  Abra um armazenamento de certificados.
3.  Crie uma matriz de armazenamento de certificados.
4.  Inicialize a [**estrutura CRYPT \_ DECRYPT MESSAGE \_ \_ PARA.**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para)
5.  Chame [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para descriptografar os dados contidos na mensagem.

[Programa C de exemplo: usar CryptEncryptMessage e CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implementa o procedimento que acabou de ser apresentado. Os comentários mostram quais elementos de código realizam cada etapa no procedimento. Para obter detalhes sobre a função, consulte [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)e, para obter detalhes sobre a estrutura de dados, consulte [**CRYPT \_ DECRYPT \_ MESSAGE \_ PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).

 

 



