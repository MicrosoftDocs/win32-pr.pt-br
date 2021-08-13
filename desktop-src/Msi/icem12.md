---
description: ICEM12 verifica se, em uma tabela ModuleSequence, as ações padrão têm números de sequência e ações personalizadas têm valores BaseAction e After.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53e6f83b9ffccf6595719815ec4bd44cc8ff3774b989b682751dd9be1bbe5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634939"
---
# <a name="icem12"></a>ICEM12

ICEM12 verifica se, em uma tabela ModuleSequence, as ações padrão têm números de sequência e ações personalizadas têm valores BaseAction e After.

Esse ICEM está disponível no arquivo Mergemod.file fornecido no SDK do Windows Installer 2.0 e posterior. Para obter detalhes, consulte [Windows SDK components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Result

ICEM12 posta um erro nos seguintes casos:

-   Ele localiza que o módulo contém [uma ação padrão](standard-actions.md) sem um número de sequência.
-   Ele descobre que uma ação padrão tem valores inseridos nos campos BaseAction ou After da tabela [ModuleAdminUISequence](moduleadminuisequence-table.md), a tabela [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), a tabela [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), a tabela [ModuleInstallUISequence](moduleinstalluisequence-table.md)ou a tabela [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).
-   Ele localiza que [](custom-actions.md) o módulo contém uma ação personalizada sem valores inseridos nos campos Sequence, BaseAction ou After da tabela [ModuleAdminUISequence](moduleadminuisequence-table.md), [moduleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md)table ou [ModuleInstallExecuteSequence table](moduleinstallexecutesequence-table.md).

ICEM12 posta um aviso se encontrar uma ação personalizada que tenha um Número de sequência especificado, mas nenhum valor nos campos BaseAction ou After.

Observe que todas as ações encontradas na [tabela CustomAction são](customaction-table.md) consideradas ações personalizadas. Todas as outras ações são consideradas ações padrão.

## <a name="example"></a>Exemplo

O ICEM12 posta as seguintes mensagens de erro e aviso para um módulo que contém as entradas de banco de dados mostradas abaixo:

``` syntax
Error. Custom actions should use the BaseAction and After fields and not use the 
Sequence field in the Module Sequence tables. The custom action 'Action1' uses the Sequence field 
and does not use the BaseAction and After fields in the ModuleInstallExecuteSequence table. 
    
Error. Custom actions should not leave the Sequence, BaseAction, and After fields 
of the Module Sequence tables all empty. The custom action 'Action3' leaves the Sequence, 
BaseAction, and After fields empty in the ModuleAdminExecuteSequence table.

Error. Standard actions should not use the BaseAction and After fields in Module 
Sequence tables. The standard action 'Action2' has a values entered in the BaseAction 
or After fields of the ModuleAdminExecuteSequence table.

Error. Standard actions must have a entry in the Sequence field of Module Sequence 
tables. The standard action 'Action2' does not have a Sequence value in the 
ModuleExecuteSequence table.
```

[CustomAction](customaction-table.md)



| Ação  | Type | Fonte  | Destino  |
|---------|------|---------|---------|
| Action1 | 30   | source1 | target1 |
| Action3 | 30   | source3 | target3 |



 

[ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)



| Ação  | Sequência | BaseAction | Depois | Condição |
|---------|----------|------------|-------|-----------|
| Action2 |          | Action1    | 1     | true      |
| Action3 |          |            |       | true      |



 

[ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Ação  | Sequência | BaseAction | Depois | Condição |
|---------|----------|------------|-------|-----------|
| Action1 | 1        |            |       | true      |



 

Para corrigir esses erros, tente o seguinte:

-   Remova o número de sequência para a ação personalizada Action1 e use os campos BaseAction e After.
-   Insira valores nos campos Sequence, BaseAction ou After para a ação personalizada Action3. Deixe os campos BaseAction e After vazios para a ação padrão Action2.
-   Não deixe o campo Sequência vazio para a ação padrão Action2.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência ice do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



