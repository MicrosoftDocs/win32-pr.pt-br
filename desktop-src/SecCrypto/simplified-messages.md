---
description: Um grupo de funções de alto nível foi fornecido para simplificar e reduzir a quantidade de código necessário para realizar as tarefas de manipulação de mensagens usuais.
ms.assetid: 7c1a4d6e-9b9d-43c8-b094-3c98b9a68490
title: Mensagens simplificadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbacaac4dd8ef32b7bab1ff4e57ad04aa1263c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090626"
---
# <a name="simplified-messages"></a>Mensagens simplificadas

Um grupo de funções de alto nível foi fornecido para simplificar e reduzir a quantidade de código necessário para realizar as tarefas de manipulação de mensagens usuais. Essas funções são chamadas de "funções de mensagem simplificadas". Os nomes de todas as funções de mensagens simplificadas contêm a palavra "mensagem".

As [*funções de mensagens simplificadas*](../secgloss/s-gly.md) estão em um nível mais alto do que as funções criptográficas base ou as funções de mensagens de nível baixo. Eles encapsulam várias das funções de criptografia base, de baixo nível e de certificado em uma única função que executa uma tarefa específica de uma maneira específica, como criptografar uma mensagem PKCS \# 7 ou assinar uma mensagem. As funções de mensagens simplificadas fornecem uma maneira rápida de começar a usar o CryptoAPI, reduzindo o número de chamadas de função necessárias para realizar uma tarefa.

A tabela a seguir lista as seções que contêm descrições detalhadas de procedimento ou exemplos de programas C de como usar as funções de mensagem simplificadas.



| Seção                                                                                                                                         | Sumário                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Funções de mensagens simplificadas](cryptography-functions.md)                                                         | Lista as funções de mensagem simplificadas.                                                     |
| [Criando uma mensagem assinada](creating-a-signed-message.md)                                                                                      | Detalha o processo de criação de uma mensagem assinada.                                           |
| [Procedimento para assinar dados](procedure-for-signing-data.md)                                                                                    | Fornece um procedimento para usar as funções de mensagem simplificadas para criar uma mensagem assinada. |
| [Verificando uma mensagem assinada](verifying-a-signed-message.md)                                                                                    | Detalha um processo para verificar a assinatura em uma mensagem assinada.                          |
| [Criptografando uma mensagem](../secauthn/encrypting-a-message.md)                                                                                           | Detalha as tarefas necessárias para criptografar e descriptografar uma mensagem.                                  |
| [Descriptografando uma mensagem](../secauthn/decrypting-a-message.md)                                                                                           | Detalha as tarefas necessárias para descriptografar uma mensagem.                                              |
| [Programa C de exemplo: usando CryptEncryptMessage e CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) | Fornece um procedimento e um código de exemplo para criptografar e descriptografar uma mensagem.               |



 

 

 
