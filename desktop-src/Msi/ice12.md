---
description: ICE12 valida as tabelas CustomAction, Directory, AdminExecuteSequence, AdminUISequence, AdvtExecuteSequence, InstallExecuteSequence e InstallUISequence do banco de dados Windows Installer.
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef427ca1567680aa9a9f2a598f5a94cb8dee545487afcf3eb1fbb8d1f350fd35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262256"
---
# <a name="ice12"></a>ICE12

ICE12 consulta as tabelas [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md)e [InstallUISequence](installuisequence-table.md) para validar o seguinte:

-   Que a [ação CostFinalize](costfinalize-action.md) ocorre em qualquer tabela de sequência que contenha ações do tipo Ação Personalizada [Tipo 35](custom-action-type-35.md) ou Tipo de Ação [Personalizada 51](custom-action-type-51.md).
-   Que cada [Tipo de Ação Personalizada 35](custom-action-type-35.md) vem após a ação [CostFinalize](costfinalize-action.md). nas tabelas de sequência.
-   Que cada Tipo de Ação [Personalizada 51](custom-action-type-51.md) que tenha uma chave estrangeira para a tabela Directory na coluna Origem da tabela CustomAction vem antes da ação [CostFinalize](costfinalize-action.md) nas tabelas de sequência.

Observe que ICE12 não valida o texto formatado na coluna Destino da tabela CustomAction.

## <a name="result"></a>Resultado

ICE12 postará uma mensagem de erro se a validação das ações personalizadas que definirem uma propriedade de diretório falhar.

## <a name="example"></a>Exemplo

ICE12 postaria três erros para o exemplo mostrado.

-   Para CA1, pasta 'MyFolder' não encontrada na tabela Diretório
-   Para CA2, a sequência '80' vem antes de CostFinalize na tabela InstallExecuteSequence. Ele deve vir depois de ( CF@100 )
-   Para CA3, a sequência '125' vem após CostFinalize na tabela InstallExecuteSequence. Ele deve vir antes de ( CF@100 )

[Tabela CustomAction](customaction-table.md) (parcial)



| Ação | Tipo | Fonte        |
|--------|------|---------------|
| CA1    | 35   | Myfolder      |
| CA2    | 35   | WindowsFolder |
| CA3    | 51   | WindowsFolder |



 

[Tabela de diretórios](directory-table.md)



| Diretório     | Pai do \_ Diretório | Defaultdir    |
|---------------|-------------------|---------------|
| Targetdir     |                   | SourceDir     |
| WindowsFolder | Targetdir         | WindowsFolder |



 

[Tabela InstallExecuteSequence](installexecutesequence-table.md) (parcial)



| Ação       | Sequência |
|--------------|----------|
| CostFinalize | 100      |
| CA2          | 80       |
| CA3          | 125      |



 

Para corrigir o erro de CA1, altere sua entrada em sua coluna Source na tabela CustomAction para uma entrada existente na tabela Directory ou adicione MyFolder à tabela Directory.

Para corrigir o erro para CA2, altere sua sequência na tabela InstallExecuteSequence de forma que ela venha após a ação CostFinalize.

Para corrigir o erro para CA3, altere sua sequência na tabela InstallExecuteSequence de forma que ela venha antes da ação CostFinalize.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



