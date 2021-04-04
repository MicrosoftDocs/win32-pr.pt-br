---
description: A tabela AdminExecuteSequence lista as ações que o instalador executa ao chamar a ação de administrador de nível superior. Confira o grupo tabelas de procedimentos de instalação, usando uma tabela de sequência e o exemplo de tabela de sequência detalhado.
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: Importando o AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cfef89ada780d9ce647f45667fdc34cc5b01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647470"
---
# <a name="importing-the-adminexecutesequence"></a>Importando o AdminExecuteSequence

A [tabela AdminExecuteSequence](adminexecutesequence-table.md) lista as ações que o instalador executa ao chamar a [ação de administrador](admin-action.md)de nível superior. Confira o [grupo tabelas de procedimentos de instalação](installation-procedure-tables-group.md), [usando uma tabela de sequência](using-a-sequence-table.md)e o exemplo de tabela de [sequência detalhado](sequence-table-detailed-example.md).

Se na seção [importando um banco de dados em branco](importing-a-blank-database.md) usado uisample.msi do SDK do Windows Installer, as tabelas de sequência em sua cópia do MNP2000.msi já contêm as sequências de ações sugeridas descritas em [usando uma tabela de sequência](using-a-sequence-table.md). Nenhuma alteração nessas sequências deve ser necessária para criar o pacote de instalação de exemplo do bloco de notas.

Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na tabela AdminExecuteSequence.

[Tabela AdminExecuteSequence](adminexecutesequence-table.md)



| Ação              | Condição | Sequência |
|---------------------|-----------|----------|
| CostFinalize        |           | 1000     |
| CostInitialize      |           | 800      |
| Custo de            |           | 900      |
| InstallAdminPackage |           | 3900     |
| InstallFiles        |           | 4000     |
| InstallFinalize     |           | 6600     |
| InstallInitialize   |           | 1500     |
| InstallValidate     |           | 1.400     |



 

[Continuar](importing-the-adminuisequence.md)

 

 



