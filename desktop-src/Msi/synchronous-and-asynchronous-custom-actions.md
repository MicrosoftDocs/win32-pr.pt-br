---
description: O Windows instalador processa ações personalizadas como um thread separado da instalação principal.
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: Ações personalizadas síncronas e assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ffa9de75d81cfe0c824bab0580f0e6565567a187f768d99687169b47543a41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893606"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a>Ações personalizadas síncronas e assíncronas

O Windows instalador processa ações personalizadas como um thread separado da instalação principal. Durante a execução síncrona de uma ação personalizada, o instalador aguarda a conclusão do thread da ação personalizada antes de continuar a instalação principal. Durante a execução assíncrona, o instalador executa a ação personalizada simultaneamente à medida que a instalação atual continua. Portanto, os autores de ações personalizadas devem estar cientes de qualquer thread assíncrono que possa estar fazendo alterações no banco de dados de instalação entre chamadas de função.

Em particular, as chamadas para [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) e [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) devem ser evitadas em ações personalizadas assíncronas. Em vez disso, [**use MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) para obter um caminho de destino. Operações de banco de dados em massa, como operações de importação, exportação e transformação, devem ser evitadas em qualquer tipo de ação personalizada.

Os sinalizadores de opção podem ser definidos no campo Tipo da tabela [CustomAction](customaction-table.md) para especificar que os threads de ação principal e personalizados sejam executados de forma síncrona ou assíncrona. Consulte [Opções de processamento de retorno de ação personalizada.](custom-action-return-processing-options.md)

O instalador só pode executar [Ações Personalizadas](rollback-custom-actions.md) de Reback e [Ações de Instalação](concurrent-installations.md) Simultânea como ações personalizadas síncronas.

 

 



