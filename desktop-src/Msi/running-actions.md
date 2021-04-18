---
description: As funções do instalador podem ser usadas para executar ações específicas ou sequências de ação.
ms.assetid: ceb4f70b-1179-416a-9030-3d87341cb956
title: Executando ações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ab566b90ec43a33f3e70b994b01446700e353b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766862"
---
# <a name="running-actions"></a>Executando ações

As funções do instalador podem ser usadas para executar ações específicas ou sequências de ação. Essas ações podem ser ações [padrão](standard-actions.md) ou [personalizadas](custom-actions.md) . O procedimento a seguir descreve como executar ações:

**Para executar uma sequência de ação**

1.  Execute uma sequência de ações definidas em uma tabela chamando a função [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) .

    O instalador consulta a tabela indicada e executa cada ação se sua expressão condicional for avaliada como TRUE.

2.  Verifique expressões condicionais chamando a função [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .
3.  Execute a ação chamando a função [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) . A ação pode ser uma ação padrão, uma ação personalizada ou uma caixa de diálogo de interface do usuário.
4.  Se ocorrer um erro durante a execução dessa ação, chame a função [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) . O instalador processará o erro.

 

 



