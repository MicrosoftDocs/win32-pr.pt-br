---
description: A ação InstallExecute executa um script que contém todas as operações na sequência de ação desde o início da instalação ou a última ação InstallExecute ou ação de InstallExecuteAgain.
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: Ação InstallExecute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 249a83f283b3abee97fbddf99d755b158678726fbb36c066791e3f87ae718f46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946124"
---
# <a name="installexecute-action"></a>Ação InstallExecute

A ação InstallExecute executa um script que contém todas as operações na sequência de ação desde o início da instalação ou a última ação InstallExecute ou ação de [InstallExecuteAgain](installexecuteagain-action.md). A ação InstallExecute atualiza o sistema sem encerrar a transação.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação InstallExecute vem entre a [ação InstallInitialize](installinitialize-action.md) e a [ação InstallFinalize](installfinalize-action.md).

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

A [ação InstallExecuteAgain](installexecuteagain-action.md) faz a mesma coisa que a ação InstallExecute. Como as tabelas de sequência têm apenas uma chave primária, a coluna Action, a mesma ação não pode ser repetida em uma tabela de sequência específica. Existem duas ações que fazem a mesma coisa, InstallExecute e InstallExecuteAgain, para casos em que a funcionalidade de InstallExecute é necessária duas vezes na [tabela InstallExecuteSequence](installexecutesequence-table.md). Para obter mais informações, consulte [usando uma tabela de sequência](using-a-sequence-table.md).

 

 



