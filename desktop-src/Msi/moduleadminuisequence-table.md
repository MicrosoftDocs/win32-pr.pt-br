---
description: Uma ferramenta de mesclagem avalia a tabela ModuleAdminUISequence e, em seguida, insere as ações calculadas na tabela AdminUISequence com um número de sequência correto.
ms.assetid: c71477e7-22bc-420a-9902-39bbf98b4ee5
title: Tabela ModuleAdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e128aebd6481c077827f4d1ba2b487eafe6132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747539"
---
# <a name="moduleadminuisequence-table"></a>Tabela ModuleAdminUISequence

Uma ferramenta de mesclagem avalia a tabela ModuleAdminUISequence e, em seguida, insere as ações calculadas na [tabela AdminUISequence](adminuisequence-table.md) com um número de sequência correto.

A tabela ModuleAdminUISequence tem as colunas a seguir.



| Coluna     | Tipo                         | Chave | Nullable |
|------------|------------------------------|-----|----------|
| Ação     | [Identificador](identifier.md) | S   | N        |
| Sequência   | [Inteiro](integer.md)       |     | S        |
| Baseaction | [Identificador](identifier.md) |     | S        |
| After (após)      | [Inteiro](integer.md)       |     | S        |
| Condição  | [Condição](condition.md)   |     | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action
</dt> <dd>

Ação a ser inserida em sequência. Refere-se a uma das [ações padrão](standard-actions.md)do instalador ou a uma entrada na tabela [CustomAction](customaction-table.md) ou na [tabela de diálogo](dialog-table.md)do módulo de mesclagem.

Se uma [ação padrão](standard-actions.md) for usada na coluna ação de uma tabela de sequência de módulo de mesclagem, as colunas baseaction e After desse registro deverão ser nulas.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem
</dt> <dd>

O número de sequência de uma ação padrão. Se uma ação ou caixa de diálogo personalizada for inserida na coluna ação dessa linha, esse campo deverá ser definido como nulo.

Ao usar [ações padrão](standard-actions.md) em tabelas de sequências do módulo de mesclagem, o valor na coluna sequência deve ser o número de sequência de ação recomendado. Se o número de sequência no módulo de mesclagem for diferente daquele para a mesma ação na tabela de sequência de arquivos. msi, a ferramenta de mesclagem usará o número de sequência do arquivo. msi. Consulte as sequências sugeridas em [usando uma tabela de sequência](using-a-sequence-table.md) para os números de sequência recomendados de ações padrão.

</dd> <dt>

<span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>Baseaction
</dt> <dd>

A coluna Baseaction pode conter uma ação padrão, uma ação personalizada especificada na tabela de ação personalizada do módulo de mesclagem ou uma caixa de diálogo especificada na tabela de diálogo do módulo. A coluna Baseaction é uma chave na coluna ação desta tabela. Ele não pode ser uma chave estrangeira em outra tabela ou tabela de mesclagem no arquivo. msi. Isso significa que cada ação padrão, ação personalizada ou caixa de diálogo listada na coluna Baseaction também deve ser listada na coluna ação de outro registro nesta tabela.

</dd> <dt>

<span id="After"></span><span id="after"></span><span id="AFTER"></span>Após
</dt> <dd>

Booliano para se a ação vier antes ou depois de Baseaction.



| Valor | Significado                          |
|-------|----------------------------------|
| 0     | Ação a ser executada antes de Baseaction |
| 1     | Ação a ser executada após Baseaction  |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema
</dt> <dd>

Uma instrução condicional que indica se a ação é executada. NULL é avaliado como true.

</dd> </dl>

## <a name="remarks"></a>Comentários

<dl> <dt>

<span id="If_this_table_is_present_the__AdminUISequence_Table_must_also_be_present_in_the_merge_module."></span><span id="if_this_table_is_present_the__adminuisequence_table_must_also_be_present_in_the_merge_module."></span><span id="IF_THIS_TABLE_IS_PRESENT_THE__ADMINUISEQUENCE_TABLE_MUST_ALSO_BE_PRESENT_IN_THE_MERGE_MODULE."></span>Se essa tabela estiver presente, a [tabela AdminUISequence](adminuisequence-table.md) também deverá estar presente no módulo de mesclagem.
</dt> <dd></dd> </dl>

 

 



