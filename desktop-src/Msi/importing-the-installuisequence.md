---
description: A sequência da interface do usuário é importada para o banco de dados de exemplo.
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: Importando o InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f20de59a752da6d24a5f3e7fed94e00aa4f0048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170425"
---
# <a name="importing-the-installuisequence"></a>Importando o InstallUISequence

A [tabela InstallUISequence](installuisequence-table.md) lista as ações que são executadas quando a ação de [instalação](install-action.md) de nível superior é executada e o nível de interface do usuário interno é definido como interface de usuários completa ou interface reduzida. O instalador ignorará as ações nesta tabela se o nível da interface do usuário estiver definido como interface básica ou como sem interface. Consulte [interface do usuário](user-interface.md) e [níveis de interface do usuário](user-interface-levels.md). Confira o [grupo tabelas de procedimentos de instalação](installation-procedure-tables-group.md), [usando uma tabela de sequência](using-a-sequence-table.md)e o exemplo de tabela de [sequência detalhado](sequence-table-detailed-example.md).

Se na seção [importando um banco de dados em branco](importing-a-blank-database.md) usado uisample.msi do SDK do Windows Installer, as tabelas de sequência em sua cópia do MNP2000.msi já contêm as sequências de ações sugeridas descritas em [usando uma tabela de sequência](using-a-sequence-table.md). Nenhuma alteração nessas sequências deve ser necessária para criar o pacote de instalação do bloco de notas.

Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na tabela InstallUISequence.

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
| Custo de              |                                              | 900      |
| LaunchConditions      |                                              | 100      |
| MaintenanceWelcomeDlg | Instalado e não retomado e não selecionado | 1250     |
| PrepareDlg            |                                              | 140      |
| ProgressDlg           |                                              | 1280     |
| ResumeDlg             | Instalado e (retomado ou preselecionado)        | 1240     |
| RMCCPSearch           | NÃO instalado                                | 600      |
| UserExitDlg           |                                              | -2       |
| WelcomeDlg            | NÃO instalado                                | 1230     |
| MigrateFeatureStates  |                                              | 1200     |
| FindRelatedProducts   |                                              | 200      |



 

[Continuar](importing-the-adminexecutesequence.md)

 

 



