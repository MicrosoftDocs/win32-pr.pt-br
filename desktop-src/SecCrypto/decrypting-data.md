---
description: Apresenta as etapas para descriptografar uma mensagem criptografada.
ms.assetid: 6af7dd28-325e-431a-9cdb-109d93af6302
title: Descriptografando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970f16862bb8c6693b2ff11f519af3f7c412024b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297680"
---
# <a name="decrypting-data"></a>Descriptografando dados

Esta seção apresenta as etapas para descriptografar uma mensagem criptografada.

**Para descriptografar uma mensagem criptografada**

1.  Obtenha um ponteiro para a mensagem digitalmente envelopada.
2.  Abra um repositório de certificados.
3.  Na mensagem, recupere o identificador de destinatário (minha ID).
4.  Use o identificador de destinatário para recuperar o certificado.
5.  Obtenha a chave privada para o certificado.
6.  Use a chave privada para descriptografar a chave simétrica (sessão).
7.  Recupere o algoritmo de criptografia da mensagem.
8.  Usando a chave de sessão descriptografada e o algoritmo de criptografia, descriptografe os dados.

[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) faz todas as tarefas para descriptografar uma mensagem; no entanto, a inicialização de estruturas e outros dados ainda é necessária.

**Para descriptografar dados usando CryptDecryptMessage**

1.  Obtenha um ponteiro para o BLOB criptografado.
2.  Abra um repositório de certificados.
3.  Criar uma matriz de repositório de certificados.
4.  Inicialize a [**estrutura \_ criptografar \_ mensagem \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) .
5.  Chame [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para descriptografar os dados contidos na mensagem.

[Programa C de exemplo: usar CryptEncryptMessage e CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implementa o procedimento que acabou de ser apresentado. Os comentários mostram quais elementos de código realizam cada etapa no procedimento. Para obter detalhes sobre a função, consulte [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)e para obter detalhes sobre a estrutura de dados, consulte [**\_ \_ mensagens \_ de descriptografia cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).

 

 



