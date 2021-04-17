---
description: A ação LaunchConditions consulta a tabela LaunchCondition e avalia cada instrução condicional gravada lá. Se qualquer uma dessas instruções condicionais falhar, uma mensagem de erro será exibida para o usuário e a instalação será encerrada.
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: Ação LaunchConditions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6bb3eaf2a98c630bb9cacd18ff449083eb9c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789777"
---
# <a name="launchconditions-action"></a>Ação LaunchConditions

A ação LaunchConditions consulta a [tabela LaunchCondition](launchcondition-table.md) e avalia cada instrução condicional gravada lá. Se qualquer uma dessas instruções condicionais falhar, uma mensagem de erro será exibida para o usuário e a instalação será encerrada.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação LaunchConditions é opcional. Essa ação é normalmente a primeira na sequência, mas a [ação AppSearch](appsearch-action.md) pode ser sequenciada antes da ação LaunchConditions. Se houver condições de inicialização que não se aplicam a todos os modos de instalação, a propriedade de modo de instalação apropriada deverá ser usada em uma expressão condicional na tabela de sequência apropriada.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

 

 



