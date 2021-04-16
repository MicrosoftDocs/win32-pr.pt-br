---
description: O valor lógico de uma propriedade que foi definida é true.
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: Usando propriedades em instruções condicionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73596c465c4bcc0864caf8512e97c92d68f05fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787058"
---
# <a name="using-properties-in-conditional-statements"></a>Usando propriedades em instruções condicionais

O valor lógico de uma propriedade que foi definida é true. Para determinar se uma propriedade está definida sem realmente obter seu valor, teste a expressão lógica "MyProperty" ou "not MyProperty". Quando a propriedade MyProperty é definida, a anterior é avaliada como true e a última como false.

Uma ou mais propriedades podem ser combinadas com operadores para formar expressões lógicas usadas em instruções condicionais. Para obter mais informações sobre os operadores que podem ser usados em instruções condicionais, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).

Uma instrução condicional que usa propriedades pode ser inserida na coluna condição da [tabela condição](condition-table.md) para modificar o estado de seleção de qualquer entrada na [tabela de recursos](feature-table.md).

Instruções condicionais com uma ou mais propriedades são geralmente usadas na coluna condição de tabelas de banco de dados.

As tabelas a seguir têm uma coluna para expressões condicionais:

-   [Tabela de condição](condition-table.md)
-   [Tabela ControlEvent,](controlevent-table.md)
-   [Tabela LaunchCondition](launchcondition-table.md)
-   [Tabela InstallUISequence](installuisequence-table.md)
-   [Tabela InstallExecuteSequence](installexecutesequence-table.md)
-   [Tabela ControlCondition](controlcondition-table.md)
-   [Tabela AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabela AdvtExecuteSequence](advtexecutesequence-table.md)
-   [Tabela AdminUISequence](adminuisequence-table.md)

Observe que as seis tabelas de sequência de ação têm campos para uma condição. Se a expressão condicional nesse campo for avaliada como false, o instalador ignorará essa ação.

Se você definir uma [propriedade privada](private-properties.md) na sequência da interface do usuário criando uma ação personalizada em uma das tabelas de sequência da interface do usuário, essa propriedade não será definida na sequência de execução. Para definir a propriedade na sequência de execução, você também deve colocar uma ação personalizada em uma tabela de sequência de execução. Como alternativa, você pode tornar a propriedade uma [propriedade pública](public-properties.md) e incluí-la na propriedade [**SecureCustomProperties**](securecustomproperties.md) .

Para obter mais informações, consulte [usando uma tabela de sequência](using-a-sequence-table.md) ou [usando Propriedades](using-properties.md).

 

 



