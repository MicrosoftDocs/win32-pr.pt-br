---
description: O valor lógico de uma propriedade que foi definida é True.
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: Usando propriedades em instruções condicionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5dcee5c2d657b8014ac98c0d4d1ce5b56f0f3614a597cd63611ae965e30720
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499206"
---
# <a name="using-properties-in-conditional-statements"></a>Usando propriedades em instruções condicionais

O valor lógico de uma propriedade que foi definida é True. Para determinar se uma propriedade é definida sem realmente obter seu valor, teste a expressão lógica "MyProperty" ou "Not MyProperty". Quando a propriedade MyProperty é definida, a primeira é avaliada como True e a última como False.

Uma ou mais propriedades podem ser combinadas com operadores para formar expressões lógicas usadas em instruções condicionais. Para obter mais informações sobre os operadores que podem ser usados em instruções condicionais, consulte [Sintaxe de instrução condicional](conditional-statement-syntax.md).

Uma instrução condicional que usa propriedades pode ser inserida na coluna Condição da tabela [Condição](condition-table.md) para modificar o estado de seleção de qualquer entrada na [tabela Recurso](feature-table.md).

Instruções condicionais com uma ou mais propriedades são comumente usadas na coluna Condição das tabelas de banco de dados.

As tabelas a seguir têm uma coluna para expressões condicionais:

-   [Tabela de condição](condition-table.md)
-   [Tabela ControlEvent](controlevent-table.md)
-   [Tabela LaunchCondition](launchcondition-table.md)
-   [Tabela InstallUISequence](installuisequence-table.md)
-   [Tabela InstallExecuteSequence](installexecutesequence-table.md)
-   [Tabela ControlCondition](controlcondition-table.md)
-   [Tabela AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabela AdvtExecuteSequence](advtexecutesequence-table.md)
-   [Tabela AdminUISequence](adminuisequence-table.md)

Observe que as seis tabelas de sequência de ação têm campos para uma condição. Se a expressão condicional nesse campo for avaliada como False, o instalador ignorará essa ação.

Se você definir [uma](private-properties.md) propriedade privada na sequência de interface do usuário ao criar uma ação personalizada em uma das tabelas de sequência de interface do usuário, essa propriedade não será definida na sequência de execução. Para definir a propriedade na sequência de execução, você também deve colocar uma ação personalizada em uma tabela de sequência de execução. Como alternativa, você pode tornar a propriedade uma [propriedade pública](public-properties.md) e incluí-la na [**propriedade SecureCustomProperties.**](securecustomproperties.md)

Para obter mais informações, consulte [Usando uma tabela de sequência ou](using-a-sequence-table.md) Usando [propriedades](using-properties.md).

 

 



