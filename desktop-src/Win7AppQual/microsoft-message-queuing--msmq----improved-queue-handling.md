---
description: MSMQ (Enfilagem de Mensagens da Microsoft) – Tratamento de fila aprimorado
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: MSMQ (Enfilagem de Mensagens da Microsoft) – Tratamento de fila aprimorado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4de125062dfdd705165e83e8a34d2bc0ef595eb08b6152d37aed5520e9ed39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053054"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a>MSMQ (Enfilagem de Mensagens da Microsoft) – Tratamento de fila aprimorado

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 7  
**Servidores** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

 **Gravidade –** Baixa  
**Frequência** – Baixa  





## <a name="description"></a>Descrição

O Serviço MSMQ não coloca um limite rígido no número de filas que podem ser criadas em um sistema. No entanto, o desempenho do sistema é afetado quando um grande número de filas é criado. Especificamente, quando há mais de alguns milhares de filas, o tempo de início do Serviço MSMQ aumenta exponencialmente, resultando em um impacto visível.

A Microsoft otimizou a start-up do Serviço MSMQ no Windows 7 para reduzir a sobrecarga de busca para carregar as filas na memória. Essa otimização levou a uma melhoria significativa do tempo de início do Serviço MSMQ, mesmo quando várias mil filas são criadas no sistema.

## <a name="manifestation-of-impact"></a>Manifestação de impacto

Essa melhoria de desempenho não afeta a funcionalidade de nenhum aplicativo existente.

## <a name="leveraging-the-changed-feature"></a>Aproveitando o recurso alterado

Os desenvolvedores de aplicativos que usam o MSMQ Windows 7 agora podem arquitetar suas soluções sem limitar o número de filas. Observe que o número de filas ainda afeta o desempenho geral do Servidor MSMQ, mas o impacto no desempenho agora está em uma escala linear em vez de exponencial.

## <a name="compatibility-performance-reliability-and-usability-tests"></a>Testes de compatibilidade, desempenho, confiabilidade e usabilidade

Se você usar um grande número de filas, simule o ambiente de produção em uma casa de teste, monitore o desempenho e analise o tempo de início do serviço e a produtividade da mensagem com um grande número de filas e mensagens presentes no sistema de teste.

 

 



