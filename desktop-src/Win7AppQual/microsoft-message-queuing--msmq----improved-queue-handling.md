---
description: .
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: MSMQ (enfileiramento de mensagens da Microsoft)-manipulação de fila aprimorada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffcc566c4c4ea461fdd9c4634b26ff69f239f03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921939"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a>MSMQ (enfileiramento de mensagens da Microsoft)-manipulação de fila aprimorada

## <a name="platforms"></a>Plataformas

**Clientes** -Windows 7  
**Servidores** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -baixa  
**Frequência** -baixa  





## <a name="description"></a>Descrição

O serviço MSMQ não coloca um limite rígido no número de filas que podem ser criadas em um sistema. No entanto, o desempenho do sistema é afetado quando um grande número de filas é criado. Especificamente, quando há mais de algumas mil filas, o tempo de inicialização do serviço MSMQ aumenta exponencialmente resultando em um impacto visível.

A Microsoft otimizou a inicialização do serviço MSMQ no Windows 7 para reduzir a sobrecarga de pesquisa para carregar as filas na memória. Essa otimização levou a uma melhoria drástica do tempo de inicialização do serviço MSMQ, mesmo quando várias filas de milhares são criadas no sistema.

## <a name="manifestation-of-impact"></a>Manifestação do impacto

Essa melhoria de desempenho não afeta a funcionalidade de nenhum aplicativo existente.

## <a name="leveraging-the-changed-feature"></a>Aproveitando o recurso alterado

Os desenvolvedores de aplicativos que usam o MSMQ no Windows 7 agora podem arquitetar suas soluções sem limitar o número de filas. Observe que o número de filas ainda afeta o desempenho geral do servidor MSMQ, mas o impacto no desempenho agora está em uma escala linear em vez de exponencial.

## <a name="compatibility-performance-reliability-and-usability-tests"></a>Compatibilidade, desempenho, confiabilidade e testes de usabilidade

Se você usar um grande número de filas, simule o ambiente de produção em uma base de teste, monitore o desempenho e analise o tempo de inicialização do serviço e a taxa de transferência da mensagem com um grande número de filas e mensagens presentes no sistema de teste.

 

 



