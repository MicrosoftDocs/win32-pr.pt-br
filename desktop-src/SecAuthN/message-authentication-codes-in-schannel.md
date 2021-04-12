---
description: Um Message Authentication Code (MAC) é usado para detectar violação e falsificação de mensagens.
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Códigos de autenticação de mensagens no Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93939c0c4b4550ad0c24f8e6ef0e0b8bf9f1b07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170812"
---
# <a name="message-authentication-codes-in-schannel"></a>Códigos de autenticação de mensagens no Schannel

Um [*Message Authentication Code*](../secgloss/m-gly.md) (Mac) é usado para detectar violação e falsificação de mensagens. O remetente de uma mensagem cria um MAC criptografando um [*hash*](../secgloss/h-gly.md) unidirecional do corpo da mensagem usando uma [*chave de sessão*](../secgloss/s-gly.md) compartilhada pelo remetente e pelo destinatário. O MAC é anexado à mensagem que é enviada ao destinatário. O destinatário da mensagem gera o MAC novamente, usando a chave de sessão compartilhada e o corpo da mensagem e compara o MAC gerado com o MAC recebido do remetente. Se os dois forem idênticos, o remetente deverá ter a chave de sessão compartilhada e a mensagem não foi alterada em trânsito.

Em protocolos Schannel, o algoritmo usado para gerar o MAC é determinado pelo [conjunto de codificação](cipher-suites-in-schannel.md) em uso pelo remetente e pelo destinatário.

 

 
