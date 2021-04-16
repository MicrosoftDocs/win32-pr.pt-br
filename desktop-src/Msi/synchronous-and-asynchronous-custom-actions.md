---
description: O Windows Installer processa ações personalizadas como um thread separado da instalação principal.
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: Ações personalizadas síncronas e assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067c5b40840269f3a0393faee8fe670f5e522c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768717"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a>Ações personalizadas síncronas e assíncronas

O Windows Installer processa ações personalizadas como um thread separado da instalação principal. Durante a execução síncrona de uma ação personalizada, o instalador aguarda que o thread da ação personalizada seja concluído antes de continuar a instalação principal. Durante a execução assíncrona, o instalador executa a ação personalizada simultaneamente à medida que a instalação atual continua. Os autores de ações personalizadas devem, portanto, estar cientes de quaisquer threads assíncronos que possam estar fazendo alterações no banco de dados de instalação entre chamadas de função.

Em particular, as chamadas para [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) e [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) devem ser evitadas em ações personalizadas assíncronas. Em vez disso, use [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) para obter um caminho de destino. Operações de banco de dados em massa, como operações de importação, exportação e transformação, devem ser evitadas em qualquer tipo de ação personalizada.

Os sinalizadores de opção podem ser definidos no campo tipo da [tabela CustomAction](customaction-table.md) para especificar que os threads de ação principal e personalizada sejam executados de forma síncrona ou assíncrona. Consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).

O instalador só pode executar ações [personalizadas de reversão](rollback-custom-actions.md) e ações de [instalação simultânea](concurrent-installations.md) como ações personalizadas síncronas.

 

 



