---
description: A ação LaunchConditions consulta a tabela LaunchCondition e avalia cada instrução condicional registrada lá. Se qualquer uma dessas instruções condicionais falhar, uma mensagem de erro será exibida para o usuário e a instalação será encerrada.
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: Ação LaunchConditions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a973e6e1de81091039de12e07e8edb890c860e5be54e942f00406e39e62e229
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086026"
---
# <a name="launchconditions-action"></a>Ação LaunchConditions

A ação LaunchConditions consulta a [tabela LaunchCondition](launchcondition-table.md) e avalia cada instrução condicional registrada lá. Se qualquer uma dessas instruções condicionais falhar, uma mensagem de erro será exibida para o usuário e a instalação será encerrada.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação LaunchConditions é opcional. Essa ação normalmente é a primeira na sequência, mas [a Ação appSearch](appsearch-action.md) pode ser sequenciada antes da ação LaunchConditions. Se houver condições de lançamento que não se aplicam a todos os modos de instalação, a propriedade de modo de instalação apropriada deverá ser usada em uma expressão condicional na tabela de sequência apropriada.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há mensagens ActionData.

 

 



