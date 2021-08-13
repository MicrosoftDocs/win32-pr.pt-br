---
description: Uma ferramenta de mesclagem avalia a tabela ModuleAdminExecuteSequence e insere as ações calculadas na tabela AdminExecuteSequence com um número de sequência correto.
ms.assetid: 26cc5e15-8dfd-4bf5-8830-225164302278
title: Tabela ModuleAdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e820c721fbbaa7d8925b07ee584cbb0b97fee66eac05fd7b8dafbe38f3f319d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628712"
---
# <a name="moduleadminexecutesequence-table"></a>Tabela ModuleAdminExecuteSequence

Uma ferramenta de mesclagem avalia a tabela ModuleAdminExecuteSequence e insere as ações calculadas na [tabela AdminExecuteSequence](adminexecutesequence-table.md) com um número de sequência correto.

A tabela ModuleAdminExecuteSequence tem as seguintes colunas.



| Coluna     | Tipo                         | Chave | Nullable |
|------------|------------------------------|-----|----------|
| Ação     | [Identificador](identifier.md) | Y   | N        |
| Sequência   | [Inteiro](integer.md)       |     | Y        |
| BaseAction | [Identificador](identifier.md) |     | Y        |
| Depois      | [Inteiro](integer.md)       |     | Y        |
| Condição  | [Condição](condition.md)   |     | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Ação
</dt> <dd>

Ação a ser inserida na sequência. Refere-se a uma das ações [padrão](standard-actions.md)do instalador ou uma entrada na tabela [CustomAction](customaction-table.md) do módulo de mesclagem ou na [tabela Dialog](dialog-table.md).

Se uma [ação padrão](standard-actions.md) for usada na coluna Ação de uma tabela de sequência de módulo de mesclagem, as colunas BaseAction e After desse registro deverão ser Null.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Seqüência
</dt> <dd>

O número de sequência de uma ação padrão. Se uma ação personalizada ou caixa de diálogo for inserida na coluna Ação desta linha, esse campo deverá ser definido como Nulo.

Ao usar [ações padrão em](standard-actions.md) tabelas de sequência de módulo de mesclagem, o valor na coluna Sequência deve ser o número de sequência de ação recomendado. Se o número de sequência no módulo de mesclagem for diferente desse para a mesma ação na tabela de sequência de arquivos .msi, a ferramenta de mesclagem usará o número de sequência do arquivo .msi. Consulte as sequências sugeridas em [Usando uma tabela de sequência](using-a-sequence-table.md) para ver os números de sequência recomendados de ações padrão.

</dd> <dt>

<span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction
</dt> <dd>

A coluna BaseAction pode conter uma ação padrão, uma ação personalizada especificada na tabela de ação personalizada do módulo de mesclagem ou uma caixa de diálogo especificada na tabela de diálogo do módulo. A coluna BaseAction é uma chave na coluna Ação desta tabela. Ele não pode ser uma chave estrangeira em outra tabela de mesclagem ou tabela no arquivo .msi dados. Isso significa que cada ação padrão, ação personalizada ou caixa de diálogo listada na coluna BaseAction também deve ser listada na coluna Ação de outro registro nesta tabela.

</dd> <dt>

<span id="After"></span><span id="after"></span><span id="AFTER"></span>Depois
</dt> <dd>

Booliana para saber se Action vem antes ou depois de BaseAction.



| Valor | Significado                          |
|-------|----------------------------------|
| 0     | Ação a ser tomada antes de BaseAction |
| 1     | Ação a ser tomada após BaseAction  |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condição
</dt> <dd>

Uma instrução condicional que indica se a ação é executada. Null é avaliada como true.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se esta tabela estiver presente, a [tabela AdminExecuteSequence](adminexecutesequence-table.md) também deverá estar presente no módulo de mesclagem.

 

 



