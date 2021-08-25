---
description: As operações de backup e restauração do VSS usam um protocolo para a interação dos sistemas que usam armazenamento em massa (autores) e aqueles que fazem backup (solicitantes).
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: Usando o Serviço de Cópias de Sombra de Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ad0f07cc20da83f9401ff5194776300c5aad23a950b2fbc7f14f787fe22f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866246"
---
# <a name="using-the-volume-shadow-copy-service"></a>Usando o Serviço de Cópias de Sombra de Volume

As operações de backup e restauração do VSS usam um protocolo para a interação dos sistemas que usam armazenamento em massa (autores) e aqueles que fazem backup (solicitantes).

As operações de backup e restauração são controladas principalmente pelo solicitante, que controla o comportamento do autor e do provedor gerando eventos COM em todo o sistema para o processamento do autor. Como os métodos de geração de eventos são assíncronos, os autores têm controle limitado no estado do solicitante por meio dos manipuladores assíncronos disponíveis para VSS (consulte [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).

Essa interação requer estruturas de dados básicas que descrevem arquivos e grupos de arquivos [*(*](vssgloss-c.md)componentes ), bem como um modelo de metadados para permitir o armazenamento de informações de backup e permitir a comunicação do autor/solicitante.

-   [Compatibilidade do aplicativo VSS](usage-conventions.md)
-   [Configurando o VSS](configuring-vss.md)
-   [Metadados do VSS](vss-metadata.md)
-   [Trabalhando com seleções e caminhos lógicos](working-with-selectability-and-logical-paths.md)
-   [Visão geral do processamento de um backup no VSS](overview-of-processing-a-backup-under-vss.md)
-   [Visão geral do processamento de uma restauração no VSS](overview-of-processing-a-restore-under-vss.md)

 

 



