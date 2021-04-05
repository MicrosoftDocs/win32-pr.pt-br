---
description: A tabela AdvtExecuteSequence lista ações que o instalador chama quando executa a ação de anúncio de nível superior. Confira o grupo tabelas de procedimentos de instalação, usando uma tabela de sequência e o exemplo de tabela de sequência detalhado.
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: Importando o AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4d7622670973a622b1376456ecfef445684cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662594"
---
# <a name="importing-the-advtexecutesequence"></a>Importando o AdvtExecuteSequence

A [tabela AdvtExecuteSequence](advtexecutesequence-table.md) lista ações que o instalador chama quando executa a [ação de anúncio](advertise-action.md)de nível superior. Confira o [grupo tabelas de procedimentos de instalação](installation-procedure-tables-group.md), [usando uma tabela de sequência](using-a-sequence-table.md)e o exemplo de tabela de [sequência detalhado](sequence-table-detailed-example.md).

Se na seção [importando um banco de dados em branco](importing-a-blank-database.md) usado uisample.msi do SDK do Windows Installer, as tabelas de sequência em sua cópia do MNP2000.msi já contêm as sequências de ações sugeridas descritas em [usando uma tabela de sequência](using-a-sequence-table.md). Nenhuma alteração nessas sequências deve ser necessária para criar o pacote de instalação de exemplo do bloco de notas.

Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na [tabela AdvtExecuteSequence](advtexecutesequence-table.md).

[Tabela AdvtExecuteSequence](advtexecutesequence-table.md)



| Ação                | Condição | Sequência |
|-----------------------|-----------|----------|
| CostFinalize          |           | 1000     |
| CostInitialize        |           | 800      |
| Createatalhos       |           | 4500     |
| InstallFinalize       |           | 6600     |
| InstallInitialize     |           | 1500     |
| InstallValidate       |           | 1.400     |
| PublishComponents     |           | 6200     |
| PublishFeatures       |           | 6300     |
| PublishProduct        |           | 6400     |
| RegisterClassInfo     |           | 4600     |
| RegisterExtensionInfo |           | 4700     |
| RegisterMIMEInfo      |           | 4900     |
| RegisterProgIdInfo    |           | 4800     |



 

A [tabela AdvtUISequence](advtuisequence-table.md) não é usada pelo instalador. Essa tabela não deve existir ou deixada vazia no banco de dados de instalação.

[Continuar](adding-summary-information.md)

 

 



