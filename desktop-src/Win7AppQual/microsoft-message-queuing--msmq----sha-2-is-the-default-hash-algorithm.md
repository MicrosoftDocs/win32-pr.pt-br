---
description: .
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: MSMQ (enfileiramento de mensagens da Microsoft)-o SHA 2 é o algoritmo de hash padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb62f55f07565e76cefb5463a095d11ae789f379
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314959"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a>MSMQ (enfileiramento de mensagens da Microsoft)-o SHA 2 é o algoritmo de hash padrão

## <a name="affected-platforms"></a>Plataformas afetadas

 **Clientes** -Windows XP, Windows Vista, Windows 7  
**Servidores** -windows Server 2003, windows Server 2008, windows Server 2008 R2  










## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -baixa  
**Frequência** -baixa  





## <a name="description"></a>Descrição

No Windows 7, o MSMQ usa o SHA-2 como padrão ao assinar uma mensagem de saída. Além disso, todas as mensagens de entrada devem ser assinadas com SHA-2. Você pode habilitar o suporte para um algoritmo de criptografia inferior por meio de uma chave do registro acessível pelo administrador.

## <a name="manifestation-of-impact"></a>Manifestação do impacto

-   O MSMQ no Windows 2003 ou inferior não aceitará mensagens assinadas provenientes do MSMQ no Windows 7
-   O MSMQ no Windows 7 não aceitará mensagens assinadas provenientes do Windows 2008 ou abaixo

## <a name="mitigation"></a>Atenuação

Os usuários devem considerar a atualização para o Windows 7 para aproveitar o algoritmo de assinatura mais forte. Para habilitar a troca direta de mensagens assinadas entre o Windows 7 e qualquer sistema operacional de nível inferior, o administrador deve adicionar as exceções apropriadas nas máquinas MSMQ.

 

 



