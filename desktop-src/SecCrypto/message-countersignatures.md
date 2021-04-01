---
description: Às vezes, uma mensagem assinada requer uma referenda.
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: Referendas de mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8dff2920217dd9a79f917f7b625da3919747d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647306"
---
# <a name="message-countersignatures"></a>Referendas de mensagem

Às vezes, uma mensagem assinada requer uma [*referenda*](../secgloss/c-gly.md). Por exemplo, o usuário A pode enviar uma mensagem de dados assinados para o usuário B, esperando que B confirme o contrato com os termos contidos no documento. O usuário B decodifica a mensagem, lê os termos e, se estiver no contrato, faz a assinatura da mensagem. A mensagem de assinatura é enviada de volta para o usuário A. o usuário A agora sabe, e pode provar que o usuário B concordou com os termos.

A tabela a seguir lista as seções que contêm descrições de procedimento ou exemplos de programa C de assinatura de mensagem.



| Seção                                                                                                                                 | Sumário                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Funções de mensagem](cryptography-functions.md)                                                                       | Lista as funções de assinatura do contador.                             |
| [Como assinar uma mensagem](countersigning-a-message.md)                                                                                | Detalha o processo de assinatura de contador de uma mensagem.                  |
| [Verificando uma referenda](verifying-a-countersignature.md)                                                                        | Detalha o procedimento para verificar uma assinatura de contador.           |
| [Verificando uma mensagem assinada](verifying-a-signed-message.md)                                                                            | Detalha um processo para verificar a assinatura em uma mensagem assinada. |
| [Programa C de exemplo: codificando e decodificando uma mensagem de assinatura](example-c-program-encoding-and-decoding-a-countersigned-message.md) | Programa C de exemplo que codifica e decodifica uma mensagem de assinatura. |



 

 

 
