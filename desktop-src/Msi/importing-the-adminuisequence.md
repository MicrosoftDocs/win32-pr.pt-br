---
description: A tabela AdminUISequence lista as ações que o instalador chama quando executa a ação de administrador de nível superior e o nível da interface do usuário interna é definido como interface de usuários completa ou interface reduzida.
ms.assetid: f23bd5c2-1d7f-485f-a22b-99436dfab6bf
title: Importando o AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f1b9d2a91a350097ac043c186478e4933f6e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751441"
---
# <a name="importing-the-adminuisequence"></a>Importando o AdminUISequence

A [tabela AdminUISequence](adminuisequence-table.md) lista as ações que o instalador chama quando executa a [ação de administrador](admin-action.md) de nível superior e o nível da interface do usuário interna é definido como interface de usuários completa ou interface reduzida. O instalador ignorará as ações nesta tabela se o nível da interface do usuário estiver definido como interface básica ou não. Consulte [interface do usuário](user-interface.md) e [níveis de interface do usuário](user-interface-levels.md). Confira o [grupo tabelas de procedimentos de instalação](installation-procedure-tables-group.md), [usando uma tabela de sequência](using-a-sequence-table.md)e o exemplo de tabela de [sequência detalhado](sequence-table-detailed-example.md).

Se na seção [importando um banco de dados em branco](importing-a-blank-database.md) usado uisample.msi do SDK do Windows Installer, as tabelas de sequência em sua cópia do MNP2000.msi já contêm as sequências de ações sugeridas descritas em [usando uma tabela de sequência](using-a-sequence-table.md). Nenhuma alteração nessas sequências deve ser necessária para instalar o exemplo do bloco de notas.

Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na tabela AdminExecuteSequence.

[Tabela AdminUISequence](adminuisequence-table.md)



| Ação          | Condição | Sequência |
|-----------------|-----------|----------|
| AdminWelcomeDlg |           | 1230     |
| CostFinalize    |           | 1000     |
| CostInitialize  |           | 800      |
| ExecuteAction   |           | 1300     |
| ExitDlg         |           | -1       |
| FatalErrorDlg   |           | -3       |
| Custo de        |           | 900      |
| PrepareDlg      |           | 140      |
| ProgressDlg     |           | 1280     |
| UserExitDlg     |           | -2       |



 

[Continuar](importing-the-advtexecutesequence.md)

 

 



