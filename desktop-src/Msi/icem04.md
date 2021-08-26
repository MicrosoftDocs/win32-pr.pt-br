---
description: ICEM04 verifica se as tabelas vazias necessárias do módulo de mesclagem estão vazias. Falha ao corrigir um erro que os relatórios ICEM04 podem resultar em mesclagem incorreta do módulo de mesclagem.
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8388cbccd576b89a70716dd7c2ca6c82ac49fb30c8c39776904753de00b68dba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050156"
---
# <a name="icem04"></a>ICEM04

ICEM04 verifica se as tabelas vazias necessárias do módulo de mesclagem estão vazias. Falha ao corrigir um erro que os relatórios ICEM04 podem resultar em mesclagem incorreta do módulo de mesclagem.

## <a name="result"></a>Resultado

ICEM04 posta um erro quando as tabelas vazias necessárias do módulo de mesclagem não estão vazias.

## <a name="example"></a>Exemplo

ICEM04 posta as seguintes mensagens de erro para um módulo que contém as entradas de banco de dados mostradas.

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

A tabela a seguir mostra uma [Tabela AdvtExecuteSequence parcial.](advtexecutesequence-table.md)



| Ação         | Sequência |
|----------------|----------|
| CostInitialize | 1        |



 

A lista a seguir mostra o conteúdo parcial de MergeModule:

-   ModuleInstallExecuteSequence
-   ModuleAdvtExecuteSequence
-   InstallUISequence

O exemplo a seguir mostra outro erro possível.

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

Se um módulo de mesclagem contiver uma tabela de sequência de módulos, ele deverá conter a tabela de sequência vazia correspondente, independentemente de a tabela de sequência de módulo estar vazia ou não. Por exemplo, se o módulo de mesclagem contiver a tabela [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), ele também deverá conter uma tabela AdminExecuteSequence vazia.

A [Tabela FeatureComponents é](featurecomponents-table.md) necessária em todos os módulos de mesclagem e deve estar vazia.

O procedimento a seguir mostra como corrigir erros.

**Para corrigir erros**

1.  Adicione uma Tabela [FeatureComponents vazia](featurecomponents-table.md) ao módulo de mesclagem.
2.  Adicione uma Tabela [InstallExecuteSequence vazia](installexecutesequence-table.md) ao módulo de mesclagem.
3.  Remova a ação 'CostInitialize' da [tabela AdvtExecuteSequence](advtexecutesequence-table.md).
    > [!Note]  
    > Essa tabela deve estar vazia em um módulo de mesclagem. As ações só devem aparecer na tabela ModuleAdvtExecuteSequence.

     

## <a name="tables-used-during-execution"></a>Tabelas usadas durante a execução

A lista a seguir identifica as tabelas usadas durante a execução:

-   [Tabela FeatureComponents](featurecomponents-table.md)
-   Tabelas \* de sequência de módulos e \* tabelas de sequência correspondentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre módulos de mesclagem](about-merge-modules.md)
</dt> <dt>

[Referência ice do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



