---
description: As funções de mensagem de nível baixo codificam dados para transmissão e decodificação de dados recebidos. Funções de mensagem de nível baixo também descriptografam e verificam as assinaturas de mensagens recebidas.
ms.assetid: 42c19920-c7f7-4a4d-9de3-3de9a34fbe0c
title: Funções de mensagem de nível baixo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22654f19dfe5178dfb98006c17c2d0536f78cd46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647307"
---
# <a name="low-level-message-functions"></a>Funções de mensagem de nível baixo

As [*funções de mensagem de nível baixo*](../secgloss/l-gly.md) codificam dados para transmissão e decodificação de dados recebidos. Funções de mensagem de nível baixo também descriptografam e verificam as assinaturas de mensagens recebidas.

Quando uma mensagem é aberta usando uma função Open de baixo nível, ela permanece aberta e disponível (mantém seu [*estado*](../secgloss/s-gly.md)) até que seja fechada. Isso permite que uma mensagem seja construída gradativamente usando várias chamadas para a função [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) .

O uso de funções de mensagens de nível baixo requer mais chamadas de função do que o uso de funções de mensagens simplificadas (consulte [mensagens simplificadas](simplified-messages.md)). Se as funções de mensagem simplificadas forem usadas, mais trabalho será feito dentro das funções da API.

O uso de funções de mensagens de nível baixo envolve o trabalho adicional de fazer chamadas para outras funções de certificado ou de criptografia. Por exemplo, os dados de chamadas para funções de certificado podem ser necessários para inicializar estruturas usadas por essas funções de mensagens de nível baixo. As funções de mensagens simplificadas inicializam muitas dessas estruturas internamente.

A tabela a seguir lista seções com descrições de procedimento e exemplos de código C de como usar as funções de mensagens de nível baixo.



| Seção                                                                               | Sumário                                           |
|---------------------------------------------------------------------------------------|----------------------------------------------------|
| [Funções de mensagem de nível baixo](cryptography-functions.md) | Lista as funções de mensagem de nível baixo.             |
| [Dados de assinatura](signing-data.md)                                                      | Detalha as tarefas necessárias para assinar dados.             |
| [Codificando dados Envelopos](encoding-enveloped-data.md)                                | Detalha as tarefas necessárias para codificar dados de envelope. |
| [Decodificando dados envelopado](decoding-enveloped-data.md)                                | Detalha as tarefas necessárias para decodificar dados de envelope. |



 

 

 
