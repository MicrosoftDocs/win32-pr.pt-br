---
description: A ação InstallExecuteAgain executa um script que contém todas as operações na sequência de ação desde o início da instalação ou a última ação de InstallExecuteAgain ou a última ação de InstallExecute.
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: Ação InstallExecuteAgain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57865c3eec28afa454e440e056d1ee964528f889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920833"
---
# <a name="installexecuteagain-action"></a>Ação InstallExecuteAgain

A ação InstallExecuteAgain executa um script que contém todas as operações na sequência de ação desde o início da instalação ou a última ação de InstallExecuteAgain ou a última [ação de InstallExecute](installexecute-action.md). A ação InstallExecute atualiza o sistema sem encerrar a transação. InstallExecuteAgain executa a mesma operação que a [ação InstallExecute](installexecute-action.md) , mas só deve ser usada após InstallExecute.

InstallExecuteAgain sempre deve ser definido para que ele não seja executado durante a remoção. Para obter informações, consulte [usando propriedades em instruções condicionais](using-properties-in-conditional-statements.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação InstallExecute vem entre a [ação InstallInitialize](installinitialize-action.md) e a [ação InstallFinalize](installfinalize-action.md).

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

A ação InstallExecuteAgain faz a mesma coisa que a [ação InstallExecute](installexecute-action.md). Como as tabelas de sequência têm apenas uma chave primária, a coluna Action, a mesma ação não pode ser repetida em uma tabela de sequência específica. Existem duas ações que fazem a mesma coisa, InstallExecute e InstallExecuteAgain, para casos em que a funcionalidade de InstallExecute é necessária duas vezes na [tabela InstallExecuteSequence](installexecutesequence-table.md). Para obter mais informações, consulte [usando uma tabela de sequência](using-a-sequence-table.md).

 

 



