---
description: A inversão de prioridade ocorre quando dois ou mais threads com prioridades diferentes estão em contenção a ser agendada.
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: Inversão de prioridade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a0f4c9d57000e9e81429ee882e70dc14f63ae4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296740"
---
# <a name="priority-inversion"></a>Inversão de prioridade

A inversão de prioridade ocorre quando dois ou mais threads com prioridades diferentes estão em contenção a ser agendada. Considere um caso simples com três threads: thread 1, thread 2 e thread 3. O thread 1 é de alta prioridade e fica pronto para ser agendado. O thread 2, um thread de baixa prioridade, está executando o código em uma seção crítica. O thread 1, o thread de alta prioridade, começa a aguardar um recurso compartilhado do thread 2. O thread 3 tem prioridade média. O thread 3 recebe todo o tempo do processador, pois o thread de alta prioridade (thread 1) está aguardando recursos compartilhados do thread de baixa prioridade (thread 2). O thread 2 não deixará a seção crítica, pois não tem a prioridade mais alta e não será agendado.

O Agendador resolve esse problema, aumentando aleatoriamente a prioridade dos threads prontos (nesse caso, os bloqueios de baixa prioridade). Os threads de baixa prioridade são executados por tempo suficiente para sair da seção crítica e o thread de alta prioridade pode inserir a seção crítica. Se o thread de baixa prioridade não obtiver tempo de CPU suficiente para sair da seção crítica pela primeira vez, ele receberá outra chance durante a próxima rodada de agendamento.

 

 



