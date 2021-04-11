---
description: O ICE75 verifica se todo o tipo de ação personalizada 17 (DLL), tipo de ação personalizada 18 (EXE), tipo de ação personalizada 21 (JScript) e ações personalizadas de tipo de ação personalizada 22 (VBScript) são sequenciadas após a ação CostFinalize.
ms.assetid: 831de042-bea6-42da-90a0-3847bb447414
title: ICE75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d708552b3ed2d397e29d37abdf0ceed01093fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297120"
---
# <a name="ice75"></a>ICE75

O ICE75 verifica se todo o [tipo de ação personalizada 17](custom-action-type-17.md) (DLL), [tipo de ação personalizada 18](custom-action-type-18.md) (exe), [tipo de ação personalizada 21](custom-action-type-21.md) (JScript) e ações personalizadas de [tipo de ação personalizada 22](custom-action-type-22.md) (VBScript) são sequenciadas após a [ação CostFinalize](costfinalize-action.md). Esses tipos de ação personalizada usam um arquivo instalado como sua origem. ICE75 verifica a tabela [InstallUISequence](installuisequence-table.md), a [tabela InstallExecuteSequence](installexecutesequence-table.md), a tabela [AdminUISequence](adminuisequence-table.md)e a [tabela AdminExecuteSequence](adminexecutesequence-table.md). Observe que a ação CostFinalize é necessária nessas tabelas de sequência.

## <a name="result"></a>Resultado

ICE75 posta um erro se encontrar uma ação personalizada usando um arquivo instalado como um arquivo de origem que não é sequenciado após a ação CostFinalize.

## <a name="example"></a>Exemplo

ICE75 relata os seguintes erros para o exemplo mostrado:

``` syntax
CostFinalize is missing from 'AdminUISequence'. CA_FileExe is a custom
 action whose source is an installed file. It must be sequenced after 
the CostFinalize action.
 
CA_FileDLL is a custom action whose source is an installed file.  It 
must be sequenced after the CostFinalize action in the 
AdminExecuteSequence table
```

[Tabela CustomAction](customaction-table.md) (parcial)



| Ação      | Tipo | Fonte  |
|-------------|------|---------|
| \_FILEEXE CA | 18   | FileExe |
| \_FILEDLL CA | 17   | FileDLL |



 

[Tabela AdminUISequence](adminuisequence-table.md) (parcial)



| Ação      | Sequência |
|-------------|----------|
| \_FILEEXE CA | 1100     |



 

[Tabela AdminExecuteSequence](adminexecutesequence-table.md) (parcial)



| Ação       | Sequência |
|--------------|----------|
| \_FILEDLL CA  | 800      |
| CostFinalize | 1000     |



 

Para corrigir os erros, sequenciar as ações personalizadas após a ação CostFinalize.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



