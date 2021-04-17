---
description: O ICEM03 verifica se todas as ações no módulo são ações básicas ou derivam de uma ação base válida.
ms.assetid: 8e2b5921-32cf-45e8-9906-30002574a712
title: ICEM03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f368fa50a71153c41eebaa9ee5084449cf824993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748592"
---
# <a name="icem03"></a>ICEM03

O ICEM03 verifica se todas as ações no módulo são ações básicas ou derivam de uma ação base válida.

O módulo de mesclagem ICEs é armazenado em um arquivo. Cub do módulo de mesclagem chamado Mergemod. Cub e não no arquivo. Cub que contém a ICEs usada para a validação do pacote.

## <a name="result"></a>Resultado

ICEM03 posta as mensagens de erro para um módulo que contém ações em uma tabela de sequência que não é uma ação base ou derivada de uma ação base válida.

## <a name="example"></a>Exemplo

ICEM03 posta as seguintes mensagens de erro para um módulo que contém as entradas de banco de dados mostradas abaixo.

``` syntax
The action 'Action1' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
The action 'Action2' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
```

[Tabela ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Ação  | Sequência | Baseaction | After (após) | Condição |
|---------|----------|------------|-------|-----------|
| Action1 |          | Action2    | 0     |           |
| Action2 |          | Action1    | 0     |           |



 

ICEM03 posta erros para essas duas ações porque elas se referem umas às outras como ações básicas na tabela ModuleInstallExecuteSequence. Todas as ações nas tabelas [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), [ModuleAdvtUISequence](moduleadvtuisequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md)e [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) devem ser ações base ou derivar sua posição da combinação de outra ação e um sinalizador de antes e depois.

Para corrigir esse erro, determine as ações básicas para as duas ações. Adicione um registro para as ações de base com um número de sequência padrão. Para Action1 e Action2, insira os nomes de ação base na coluna Baseaction e 0 ou 1 na coluna After.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



