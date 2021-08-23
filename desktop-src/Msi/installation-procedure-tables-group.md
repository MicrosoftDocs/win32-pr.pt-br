---
description: As tabelas no grupo de procedimentos de instalação controlam tarefas executadas durante a instalação por ações padrão e ações personalizadas.
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: Grupo de tabelas de procedimento de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c66cc377fdf36969699f0e150fc30a02363ed24aa1848c4492917bffda7bc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633581"
---
# <a name="installation-procedure-tables-group"></a>Grupo de tabelas de procedimento de instalação

As tabelas no grupo de procedimentos de instalação controlam tarefas executadas durante a instalação por [ações padrão](standard-actions.md) e [ações personalizadas](custom-actions.md).

Algumas das tabelas nesse grupo controlam uma ação de alto nível, fornecendo uma sequência de ações. Cada uma das tabelas de sequência a seguir controla uma parte de uma ação de alto nível.

-   [Tabela InstallUISequence](installuisequence-table.md)
-   [Tabela InstallExecuteSequence](installexecutesequence-table.md)
-   [Tabela AdminUISequence](adminuisequence-table.md)
-   [Tabela AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabela AdvtUISequence](advtuisequence-table.md)
-   [Tabela AdvtExecuteSequence](advtexecutesequence-table.md)

Pode haver situações em que uma instalação precisa fazer algo que não é possível usando apenas [ações padrão](standard-actions.md). Para fornecer o maior grau de flexibilidade, o instalador fornece aos autores da instalação a capacidade de criar suas próprias ações personalizadas. Se você tiver ações personalizadas, deverá registrá-las com o instalador preenchendo a tabela CustomAction.

A [tabela CustomAction](customaction-table.md) fornece os meios de integrar código e dados personalizados ao processo de instalação. O código executado pode ser um fluxo contido no banco de dados, um arquivo recentemente instalado ou um executável existente.

As tabelas a seguir estendem os recursos do instalador para manipular arquivos e pastas durante a instalação.

-   A [tabela RemoveFile](removefile-table.md) contém uma lista de arquivos que são removidos durante a instalação.
-   A [tabela RemoveIniFile](removeinifile-table.md) contém as informações que um aplicativo precisa remover de .ini arquivos.
-   A [tabela RemoveRegistry](removeregistry-table.md) contém as informações que são excluídas do registro do sistema quando o componente correspondente é selecionado para ser instalado.
-   A [tabela CreateFolder](createfolder-table.md) lista as pastas que devem ser criadas durante a instalação. Embora o instalador Crie pastas conforme necessário, elas são removidas assim que estiverem vazias. A lista de pastas na tabela CreateFolder não é excluída até que o componente seja desinstalado.
-   A [tabela MoveFile](movefile-table.md) contém uma lista de arquivos a serem movidos ou copiados de um diretório de origem especificado no computador do usuário para um diretório de destino. Não é necessário usar a tabela MoveFile para descrever os arquivos associados aos componentes que você está instalando.

Para configurar as condições necessárias que devem ser atendidas para iniciar a instalação, preencha a tabela LaunchCondition.

A [tabela LaunchCondition](launchcondition-table.md) contém uma lista de condições, que devem ser satisfeitas para que a ação seja realizada com sucesso.

 

 



