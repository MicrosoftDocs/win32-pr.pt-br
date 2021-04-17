---
description: ICE12 valida as tabelas CustomAction, Directory, AdminExecuteSequence, AdminUISequence, AdvtExecuteSequence, InstallExecuteSequence e InstallUISequence do banco de dados Windows Installer.
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d02756bd357c6e85f60b0c41b72a4a66965fedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769319"
---
# <a name="ice12"></a>ICE12

ICE12 consulta as tabelas [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md)e [InstallUISequence](installuisequence-table.md) para validar o seguinte:

-   A [ação CostFinalize](costfinalize-action.md) ocorre em qualquer tabela de sequência que contenha ações do tipo tipo de [ação personalizada 35](custom-action-type-35.md) ou [tipo de ação personalizada 51](custom-action-type-51.md).
-   Cada [tipo de ação personalizada 35](custom-action-type-35.md) vem após a [ação CostFinalize](costfinalize-action.md). nas tabelas de sequência.
-   Cada [ação personalizada tipo 51](custom-action-type-51.md) que tem uma chave estrangeira para a tabela de diretório na coluna de origem da tabela CustomAction vem antes da [ação CostFinalize](costfinalize-action.md) nas tabelas de sequência.

Observe que o ICE12 não valida o texto formatado na coluna de destino da tabela CustomAction.

## <a name="result"></a>Resultado

ICE12 posta uma mensagem de erro se a validação das ações personalizadas que definem uma propriedade de diretório falhar.

## <a name="example"></a>Exemplo

ICE12 iria postar três erros para o exemplo mostrado.

-   Para CA1, pasta ' MyFolder ' não encontrada na tabela de diretórios
-   Para CA2, a sequência ' 80 ' vem antes de CostFinalize na tabela InstallExecuteSequence. Ele deve vir após ( CF@100 )
-   Para CA3, a sequência ' 125 ' vem após CostFinalize na tabela InstallExecuteSequence. Ele deve vir antes de ( CF@100 )

[Tabela CustomAction](customaction-table.md) (parcial)



| Ação | Tipo | Fonte        |
|--------|------|---------------|
| CA1    | 35   | MyFolder      |
| CA2    | 35   | WindowsFolder |
| CA3    | 51   | WindowsFolder |



 

[Tabela de diretórios](directory-table.md)



| Diretório     | Pai do diretório \_ | DefaultDir    |
|---------------|-------------------|---------------|
| TARGETDIR     |                   | SourceDir     |
| WindowsFolder | TARGETDIR         | WindowsFolder |



 

[Tabela InstallExecuteSequence](installexecutesequence-table.md) (parcial)



| Ação       | Sequência |
|--------------|----------|
| CostFinalize | 100      |
| CA2          | 80       |
| CA3          | 125      |



 

Para corrigir o erro de CA1, altere sua entrada em sua coluna de origem na tabela CustomAction para uma entrada existente na tabela de diretório ou adicione MyFolder à tabela de diretórios.

Para corrigir o erro para CA2, altere sua sequência na tabela InstallExecuteSequence de modo que ela venha após a ação CostFinalize.

Para corrigir o erro para CA3, altere sua sequência na tabela InstallExecuteSequence de tal forma que ela venha antes da ação CostFinalize.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



