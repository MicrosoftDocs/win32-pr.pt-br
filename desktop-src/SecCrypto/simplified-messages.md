---
description: Um grupo de funções de alto nível foi fornecido para simplificar e reduzir a quantidade de código necessário para realizar as tarefas de manipulação de mensagens usuais.
ms.assetid: 7c1a4d6e-9b9d-43c8-b094-3c98b9a68490
title: Mensagens simplificadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc274ecf876aed079e879ea1a97c000c1ddeb4c37b11e868ef8fa198103cf5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972617"
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



 

 

 
