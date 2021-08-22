---
description: Adicione um registro à tabela CustomAction para a ação personalizada de inicialização.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Adicionando inicialização às tabelas CustomAction e binary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b362259f2ee336a540f396dc05f7745cbc3fde8fb44b8a1c06dabbd6247ba05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145959"
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

 

 



