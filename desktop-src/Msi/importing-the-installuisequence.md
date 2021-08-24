---
description: A sequência de interface do usuário é importada para o banco de dados de exemplo.
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: Importando o InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c559f9c4ad2cbd766447d27c879246f0fbf6af1ff78e1e02dece17b362ad2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580655"
---
# <a name="importing-the-installuisequence"></a>Importando o InstallUISequence

A [tabela InstallUISequence](installuisequence-table.md) lista as ações executadas quando a ação [INSTALL](install-action.md) de nível superior é executada e o nível de interface do usuário interno é definido como interface do usuário completa ou interface do usuário reduzida. O instalador ignorará as ações nesta tabela se o nível de interface do usuário estiver definido como interface do usuário básica ou sem interface do usuário. Consulte [Interface do Usuário](user-interface.md) e [Interface do Usuário níveis .](user-interface-levels.md) Consulte [Grupo de tabelas de procedimento de](installation-procedure-tables-group.md)instalação , usando uma tabela de [sequência](using-a-sequence-table.md)e o exemplo detalhado da tabela de sequência [.](sequence-table-detailed-example.md)

Se na [](importing-a-blank-database.md) seção Importando um banco de dados em branco que você usou uisample.msi do SDK do Instalador do Windows, as tabelas de sequência na cópia do MNP2000.msi já contêm as sequências de ação sugeridas descritas em Usando uma tabela de sequência [.](using-a-sequence-table.md) Nenhuma alteração nessas sequências deve ser necessária para criar o pacote de Bloco de notas instalação.

Use o editor de banco de dados para MNP2000.msi e insira os dados a seguir na tabela InstallUISequence.

[Tabela InstallUISequence](installuisequence-table.md)



| Ação                | Condição                                    | Sequência |
|-----------------------|----------------------------------------------|----------|
| AppSearch             |                                              | 400      |
| CCPSearch             | NÃO instalado                                | 500      |
| CostFinalize          |                                              | 1000     |
| CostInitialize        |                                              | 800      |
| ExecuteAction         |                                              | 1300     |
| ExitDlg               |                                              | -1       |
| FatalErrorDlg         |                                              | -3       |
| FileCost              |                                              | 900      |
| LaunchConditions      |                                              | 100      |
| MaintenanceWelcomeDlg | Instalado E NÃO RETOMAR E NÃO Pré-selecionado | 1250     |
| PrepareDlg            |                                              | 140      |
| ProgressDlg           |                                              | 1280     |
| ResumeDlg             | INSTALADO E (RESUME OU Pré-selecionado)        | 1240     |
| RMCCPSearch           | NÃO instalado                                | 600      |
| UserExitDlg           |                                              | -2       |
| WelcomeDlg            | NÃO instalado                                | 1230     |
| MigrateFeatureStates  |                                              | 1200     |
| FindRelatedProducts   |                                              | 200      |



 

[Continuar](importing-the-adminexecutesequence.md)

 

 



