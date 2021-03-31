---
description: Inclua as tabelas MergeModuleSequence no arquivo. msm se o módulo de mesclagem precisar modificar as tabelas de sequência de ação do arquivo. msi de destino. A mesclagem não adiciona essas tabelas ao arquivo. msi. Essas tabelas ocorrem somente em módulos de mesclagem.
ms.assetid: 9efb75d2-43f9-404c-8e7f-918d056190cf
title: Criando tabelas de sequências do módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b21780601e626c006967cefa0dcff5700bdec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921495"
---
# <a name="authoring-merge-module-sequence-tables"></a>Criando tabelas de sequências do módulo de mesclagem

Inclua as tabelas MergeModuleSequence no arquivo. msm se o módulo de mesclagem precisar modificar as [*tabelas de sequência*](s-gly.md) de ação do arquivo. msi de destino. A mesclagem não adiciona essas tabelas ao arquivo. msi. Essas tabelas ocorrem somente em módulos de mesclagem.

Se qualquer uma das tabelas ModuleSequence estiver presente em um arquivo. msm, uma cópia vazia da tabela de sequência de instalador correspondente também deverá ser criada no módulo de mesclagem. Por exemplo, se um módulo de mesclagem contiver uma tabela ModuleAdminExecuteSequence, o módulo de mesclagem também deverá incluir uma tabela AdminExecuteSequence vazia. Durante uma mesclagem, essas tabelas vazias fornecem a ferramenta de mesclagem com as diretrizes de esquema necessárias.

Ao usar [ações padrão](standard-actions.md) em tabelas de sequências do módulo de mesclagem, o valor na coluna sequência deve ser o número de sequência de ação recomendado para a ação padrão. Consulte as sequências de ação sugeridas fornecidas abaixo para os números de sequência recomendados em cada tabela de sequência. Se o número de sequência na tabela de sequência do módulo de mesclagem for diferente do número de sequência para a mesma ação no arquivo. msi, a ferramenta de mesclagem usará o número de sequência no arquivo. msi durante a mesclagem.



| Tabela MergeModuleSequence                                                    | Sequências de ações recomendadas                                             |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ModuleAdminUISequence](moduleadminuisequence-table.md)                     | [AdminUISequence sugerido](suggested-adminuisequence.md)               |
| [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)           | [AdminExecuteSequence sugerido](suggested-adminexecutesequence.md)     |
| [ModuleAdvtUISequence](moduleadvtuisequence-table.md)                       | [AdvtUISequence sugerido](suggested-advtuisequence.md)                 |
| [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)             | [AdvtExecuteSequence sugerido](suggested-advtexecutesequence.md)       |
| [ModuleInstallUISequence](moduleinstalluisequence-table.md)                 | [InstallUISequence sugerido](suggested-installuisequence.md)           |
| [Tabela ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) | [InstallExecuteSequence sugerido](suggested-installexecutesequence.md) |



 

Se uma [ação padrão](standard-actions.md) for usada na coluna ação de uma tabela de sequência de módulo de mesclagem, as colunas baseaction e After desse registro deverão ser nulas.

Se uma ação ou caixa de diálogo personalizada for inserida na coluna ação, a coluna sequência deverá ser nula.

Se uma ação que retorna um sinalizador de encerramento for inserida na coluna de ação, a coluna de sequência deverá conter o valor negativo para esse sinalizador e as colunas Baseaction e After desse registro deverão ser nulas. Os valores negativos a seguir indicam que a ação será chamada se o instalador retornar o sinalizador de término.



| Sinalizador de término          | Valor | Descrição              |
|---------------------------|-------|--------------------------|
| msiDoActionStatusSuccess  | -1    | Conclusão bem-sucedida.   |
| msiDoActionStatusUserExit | -2    | O usuário encerra a instalação. |
| msiDoActionStatusFailure  | -3    | Encerramentos de saída fatais.   |
| msiDoActionStatusSuspend  | -4    | A instalação está suspensa.    |



 

A coluna Baseaction pode conter uma ação padrão, uma ação personalizada especificada na tabela de ação personalizada do módulo de mesclagem ou uma caixa de diálogo especificada na tabela de diálogo do módulo. A coluna Baseaction é uma chave na coluna ação desta tabela. Ele não pode ser uma chave estrangeira em outra tabela ou tabela de mesclagem no arquivo. msi. Isso significa que cada ação padrão, ação personalizada ou caixa de diálogo listada na coluna Baseaction também deve ser listada na coluna ação de outro registro nesta tabela.

 

 



