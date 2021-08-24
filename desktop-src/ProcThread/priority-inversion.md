---
description: A inversão de prioridade ocorre quando dois ou mais threads com prioridades diferentes estão em contenção a ser agendada.
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: Inversão de prioridade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a891655196b8f7e81c118d39fb8516a244411f1f4f6d9505e2fb40818d71f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031926"
---
# <a name="priority-inversion"></a>Inversão de prioridade

A inversão de prioridade ocorre quando dois ou mais threads com prioridades diferentes estão em contenção a ser agendada. Considere um caso simples com três threads: thread 1, thread 2 e thread 3. O thread 1 é de alta prioridade e fica pronto para ser agendado. O thread 2, um thread de baixa prioridade, está executando o código em uma seção crítica. O thread 1, o thread de alta prioridade, começa a aguardar um recurso compartilhado do thread 2. O Thread 3 tem prioridade média. O Thread 3 recebe todo o tempo do processador, pois o thread de alta prioridade (thread 1) está aguardando recursos compartilhados do thread de baixa prioridade (thread 2). O Thread 2 não deixará a seção crítica, pois ele não tem a prioridade mais alta e não será agendado.

O agendador resolve esse problema aumentando aleatoriamente a prioridade dos threads prontos (nesse caso, os titulares de bloqueio de baixa prioridade). Os threads de baixa prioridade são executados por tempo suficiente para sair da seção crítica e o thread de alta prioridade pode entrar na seção crítica. Se o thread de baixa prioridade não tiver tempo de CPU suficiente para sair da seção crítica pela primeira vez, ele terá outra chance durante a próxima rodada de agendamento.

 

 



