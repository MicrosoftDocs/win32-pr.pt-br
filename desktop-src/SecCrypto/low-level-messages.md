---
description: As funções de mensagem de baixo nível codificam dados para transmissão e decodificar dados que foram recebidos. As funções de mensagem de baixo nível também descriptografam e verificam as assinaturas das mensagens recebidas.
ms.assetid: 42c19920-c7f7-4a4d-9de3-3de9a34fbe0c
title: Funções de mensagem de baixo nível
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ee5aaf91fe52a727404ecd3417922e239642c6d445a6674044cc95ebd286a5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408396"
---
# <a name="low-level-message-functions"></a>Funções de mensagem de baixo nível

As [*funções de mensagem de baixo nível codificam*](../secgloss/l-gly.md) dados para transmissão e decodificar dados que foram recebidos. As funções de mensagem de baixo nível também descriptografam e verificam as assinaturas das mensagens recebidas.

Quando uma mensagem é aberta usando uma função aberta de mensagem de baixo nível, ela permanece aberta e disponível (mantém seu estado [*)*](../secgloss/s-gly.md)até que seja fechada. Isso permite que uma mensagem seja construída por peça usando várias chamadas para a [**função CryptMsgUpdate.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)

O uso de funções de mensagem de baixo nível requer mais chamadas de função do que o uso de funções de mensagem simplificadas (consulte [Mensagens simplificadas](simplified-messages.md)). Se as funções de mensagem simplificadas são usadas, mais do trabalho é feito dentro das funções da API.

O uso de funções de mensagem de baixo nível envolve o trabalho adicional de fazer chamadas para outros certificados ou funções criptográficas. Por exemplo, dados de chamadas para funções de certificado podem ser necessários para inicializar estruturas usadas por essas funções de mensagem de baixo nível. As funções de mensagem simplificadas inicializam muitas dessas estruturas internamente.

A tabela a seguir lista seções com descrições de procedimento e exemplos de código C do uso das funções de mensagem de baixo nível.



| Seção                                                                               | Sumário                                           |
|---------------------------------------------------------------------------------------|----------------------------------------------------|
| [Funções de mensagem de baixo nível](cryptography-functions.md) | Lista as funções de mensagem de baixo nível.             |
| [Assinatura de dados](signing-data.md)                                                      | Detalha as tarefas necessárias para assinar dados.             |
| [Codificando dados envelhados](encoding-enveloped-data.md)                                | Detalha as tarefas necessárias para codificar dados envelhados. |
| [Decodificação de dados envelhados](decoding-enveloped-data.md)                                | Detalha as tarefas necessárias para decodificar dados envelhados. |



 

 

 
