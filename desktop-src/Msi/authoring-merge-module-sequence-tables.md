---
description: Inclua as tabelas MergeModuleSequence no arquivo .msm se o módulo de mesclagem tiver que modificar as tabelas de sequência de ação do arquivo .msi destino. Mesclar não adiciona essas tabelas ao arquivo .msi dados. Essas tabelas ocorrem apenas em módulos de mesclagem.
ms.assetid: 9efb75d2-43f9-404c-8e7f-918d056190cf
title: Como autorar tabelas de sequência de módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45e4cf86c846030854054d7ab700e34210d4e27367cd31d606c78c24f2a9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381181"
---
# <a name="authoring-merge-module-sequence-tables"></a>Como autorar tabelas de sequência de módulo de mesclagem

Inclua as tabelas MergeModuleSequence no arquivo .msm se [](s-gly.md) o módulo de mesclagem deve modificar as tabelas de sequência de ação do arquivo .msi destino. Mesclar não adiciona essas tabelas ao arquivo .msi dados. Essas tabelas ocorrem apenas em módulos de mesclagem.

Se alguma das tabelas ModuleSequence estiver presente em um arquivo .msm, uma cópia vazia da tabela de sequência do instalador correspondente também deverá ser autor no módulo de mesclagem. Por exemplo, se um módulo de mesclagem contiver uma tabela ModuleAdminExecuteSequence, o módulo de mesclagem também deverá incluir uma tabela AdminExecuteSequence vazia. Durante uma mesclagem, essas tabelas vazias fornecem à ferramenta de mesclagem as diretrizes de esquema necessárias.

Ao usar [ações padrão em](standard-actions.md) tabelas de sequência de módulo de mesclagem, o valor na coluna Sequência deve ser o número de sequência de ação recomendado para a ação padrão. Consulte as sequências de ação sugeridas fornecidas abaixo para ver os números de sequência recomendados em cada tabela de sequência. Se o número de sequência na tabela de sequência do módulo de mesclagem for diferente do número de sequência da mesma ação no arquivo .msi, a ferramenta de mesclagem usará o número de sequência no arquivo .msi durante a mesclagem.



| Tabela MergeModuleSequence                                                    | Sequências de ação recomendadas                                             |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ModuleAdminUISequence](moduleadminuisequence-table.md)                     | [AdminUISequence sugerido](suggested-adminuisequence.md)               |
| [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)           | [AdminExecuteSequence sugerido](suggested-adminexecutesequence.md)     |
| [ModuleAdvtUISequence](moduleadvtuisequence-table.md)                       | [AdvtUISequence sugerido](suggested-advtuisequence.md)                 |
| [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)             | [AdvtExecuteSequence sugerido](suggested-advtexecutesequence.md)       |
| [ModuleInstallUISequence](moduleinstalluisequence-table.md)                 | [InstallUISequence sugerido](suggested-installuisequence.md)           |
| [Tabela ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) | [Instalação SugeridaExecuteSequence](suggested-installexecutesequence.md) |



 

Se uma [ação padrão](standard-actions.md) for usada na coluna Ação de uma tabela de sequência de módulo de mesclagem, as colunas BaseAction e After desse registro deverão ser Null.

Se uma ação personalizada ou caixa de diálogo for inserida na coluna Ação, a coluna Sequência deverá ser nula.

Se uma ação que retorna um sinalizador de encerramento for inserida na coluna Ação, a coluna Sequência deverá conter o valor negativo para esse sinalizador e as colunas BaseAction e After desse registro deverão ser Null. Os valores negativos a seguir indicam que a ação será chamada se o instalador retornar o sinalizador de encerramento.



| Sinalizador de término          | Valor | Descrição              |
|---------------------------|-------|--------------------------|
| msiDoActionStatusSuccess  | -1    | Conclusão bem-sucedida.   |
| msiDoActionStatusUserExit | -2    | O usuário encerra a instalação. |
| msiDoActionStatusFailure  | -3    | A saída fatal é encerrada.   |
| msiDoActionStatusSuspend  | -4    | A instalação está suspensa.    |



 

A coluna BaseAction pode conter uma ação padrão, uma ação personalizada especificada na tabela de ação personalizada do módulo de mesclagem ou uma caixa de diálogo especificada na tabela de diálogo do módulo. A coluna BaseAction é uma chave na coluna Ação desta tabela. Ele não pode ser uma chave estrangeira em outra tabela de mesclagem ou tabela no arquivo .msi. Isso significa que cada ação padrão, ação personalizada ou caixa de diálogo listada na coluna BaseAction também deve ser listada na coluna Ação de outro registro nesta tabela.

 

 



