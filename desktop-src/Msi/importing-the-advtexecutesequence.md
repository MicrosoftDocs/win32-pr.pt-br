---
description: A tabela AdvtExecuteSequence lista as ações que o instalador chama quando executa a ação ADVERTISE de nível superior. Consulte Grupo de tabelas de procedimento de instalação, usando uma tabela de sequência e o exemplo detalhado da tabela de sequência.
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: Importando o AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518adfa315b5705806ba65caf09691316894ab664c32485dd3f4b6ce894be1a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043666"
---
# <a name="importing-the-advtexecutesequence"></a>Importando o AdvtExecuteSequence

A [tabela AdvtExecuteSequence](advtexecutesequence-table.md) lista as ações que o instalador chama quando executa a ação [ADVERTISE](advertise-action.md)de nível superior . Consulte [Grupo de tabelas de procedimento de](installation-procedure-tables-group.md)instalação , usando uma tabela de [sequência](using-a-sequence-table.md)e o exemplo detalhado da tabela de sequência [.](sequence-table-detailed-example.md)

Se na [](importing-a-blank-database.md) seção Importando um banco de dados em branco que você usou uisample.msi do SDK do Instalador do Windows, as tabelas de sequência em sua cópia do MNP2000.msi já contêm as sequências de ação sugeridas descritas em Usando uma tabela de sequência [.](using-a-sequence-table.md) Nenhuma alteração nessas sequências deve ser necessária para criar o Bloco de notas de instalação de exemplo.

Use o editor de banco de dados para MNP2000.msi e insira os dados a seguir na [tabela AdvtExecuteSequence](advtexecutesequence-table.md).

[Tabela AdvtExecuteSequence](advtexecutesequence-table.md)



| Ação                | Condição | Sequência |
|-----------------------|-----------|----------|
| CostFinalize          |           | 1000     |
| CostInitialize        |           | 800      |
| CreateShortcuts       |           | 4500     |
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



 

A [tabela AdvtUISequence](advtuisequence-table.md) não é usada pelo instalador. Essa tabela não deve existir ou ser deixada vazia no banco de dados de instalação.

[Continuar](adding-summary-information.md)

 

 



