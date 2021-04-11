---
description: Adicione um registro à tabela CustomAction para a ação personalizada de inicialização.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Adicionando inicialização às tabelas CustomAction e binary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbcd1b483505d7d33981d695ed0d29c3b72a3f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091549"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a>Adicionando inicialização às tabelas CustomAction e binary

Adicione um registro à [tabela CustomAction](customaction-table.md) para a ação personalizada de inicialização. Insira o nome da ação personalizada na coluna ação da tabela CustomAction. Insira o tipo numérico total para inicialização, 65, na coluna tipo da tabela ação personalizada. A coluna Source da tabela CustomAction especifica uma chave para o registro da [tabela binária](binary-table.md) que contém os dados binários da dll. Insira Tutorial.dll na coluna de origem da tabela CustomAction. O ponto de entrada especificado no campo de destino da tabela CustomAction deve corresponder ao exportado da DLL. Insira LaunchTutorial na coluna de destino da tabela CustomAction.

[Tabela CustomAction](customaction-table.md)



| Ação | Tipo | Fonte       | Destino         |
|--------|------|--------------|----------------|
| Inicializar | 65   | Tutorial.dll | LaunchTutorial |



 

Adicione o Tutorial.dll criado no tutorial. cpp como um fluxo binário à tabela binária.

[Tabela binária](binary-table.md)



| Nome         | Dados                          |
|--------------|-------------------------------|
| Tutorial.dll | {*dados binários adicionados para dll*} |



 

Continue a [Adicionar um evento de controle no final da instalação para executar a inicialização](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).

 

 



