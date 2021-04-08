---
description: ICEM12 verifica que, em uma tabela ModuleSequence, as ações padrão têm números de sequência e as ações personalizadas têm os valores Baseaction e After.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37cbff2e29a85dd50ef1f044a43fdb8e48ffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010630"
---
# <a name="icem12"></a>ICEM12

ICEM12 verifica que, em uma tabela ModuleSequence, as ações padrão têm números de sequência e as ações personalizadas têm os valores Baseaction e After.

Esse ICEM está disponível no arquivo Mergemod. Cub fornecido no SDK do Windows Installer 2,0 e posterior. Para obter detalhes, consulte [SDK do Windows components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Resultado

ICEM12 posta um erro nos seguintes casos:

-   Ele descobre que o módulo contém uma [ação padrão](standard-actions.md) sem um número de sequência.
-   Ele descobre que uma ação padrão tem valores inseridos nos campos Baseaction ou After da [tabela ModuleAdminUISequence](moduleadminuisequence-table.md), [tabela ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), tabela [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), tabela [ModuleInstallUISequence](moduleinstalluisequence-table.md)ou [tabela ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).
-   Ele descobre que o módulo contém uma [ação personalizada](custom-actions.md) sem quaisquer valores inseridos nos campos Sequence, baseaction ou After da [tabela ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), tabela [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), tabela [ModuleInstallUISequence](moduleinstalluisequence-table.md)ou [tabela ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).

ICEM12 lançará um aviso se encontrar uma ação personalizada que tenha um número de sequência especificado, mas nenhum valor nos campos Baseaction ou After.

Observe que todas as ações encontradas na [tabela CustomAction](customaction-table.md) são consideradas ações personalizadas. Todas as outras ações são consideradas ações padrão.

## <a name="example"></a>Exemplo

ICEM12 posta as mensagens de erro e de aviso a seguir para um módulo que contém as entradas de banco de dados mostradas abaixo:

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



| Ação  | Tipo | Fonte  | Destino  |
|---------|------|---------|---------|
| Action1 | 30   | origem1 | target1 |
| Action3 | 30   | source3 | target3 |



 

[ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)



| Ação  | Sequência | Baseaction | After (após) | Condição |
|---------|----------|------------|-------|-----------|
| Action2 |          | Action1    | 1     | true      |
| Action3 |          |            |       | true      |



 

[ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Ação  | Sequência | Baseaction | After (após) | Condição |
|---------|----------|------------|-------|-----------|
| Action1 | 1        |            |       | true      |



 

Para corrigir esses erros, tente o seguinte:

-   Remova o número de sequência para a ação personalizada Action1 e use os campos Baseaction e After em vez disso.
-   Insira valores nos campos Sequence, Baseaction ou After para a ação personalizada Action3. Deixe os campos Baseaction e After vazios para a ação padrão Action2.
-   Não deixe o campo de sequência Vazio para a ação padrão Action2.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



