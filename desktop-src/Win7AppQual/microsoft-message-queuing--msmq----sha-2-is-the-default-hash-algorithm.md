---
description: MSMQ (Enquete de Mensagens da Microsoft) – SHA 2 é o algoritmo de hash padrão
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: MSMQ (Enquete de Mensagens da Microsoft) – SHA 2 é o algoritmo de hash padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3c54832d953e50f3b912fdf36374faa8ff9ed0466587f7ac3fed2572eb3b85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053034"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a>MSMQ (Enquete de Mensagens da Microsoft) – SHA 2 é o algoritmo de hash padrão

## <a name="affected-platforms"></a>Plataformas afetadas

 **Clientes** – Windows XP, Windows Vista, Windows 7  
**Servidores** – Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










## <a name="feature-impact"></a>Impacto do recurso

 **Gravidade –** Baixa  
**Frequência** – Baixa  





## <a name="description"></a>Descrição

No Windows 7, o MSMQ usa SHA-2 como o padrão ao assinar uma mensagem de saída. Além disso, todas as mensagens de entrada devem ser assinadas com SHA-2. Você pode habilitar o suporte para um algoritmo de criptografia inferior por meio de uma chave do Registro acessível pelo administrador.

## <a name="manifestation-of-impact"></a>Manifestação de impacto

-   O MSMQ Windows 2003 ou inferior não aceitará mensagens assinadas provenientes do MSMQ no Windows 7
-   O MSMQ Windows 7 não aceitará mensagens assinadas provenientes do Windows 2008 ou inferior

## <a name="mitigation"></a>Atenuação

Os usuários devem considerar atualizar para o Windows 7 para aproveitar o algoritmo de assinatura mais forte. Para habilitar a troca contínua de mensagens assinadas entre o Windows 7 e qualquer sistema operacional de nível inferior, o Administrador deve adicionar exceções apropriadas nos máquinas MSMQ.

 

 



