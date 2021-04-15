---
description: As operações de backup e restauração do VSS usam um protocolo para a interação dos sistemas que usam gravadores (armazenamento em massa) e os que fazem backup (solicitantes).
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: Usando o Serviço de Cópias de Sombra de Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a1c81d79de30085f783feb02b7a7d47d5dc765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501739"
---
# <a name="using-the-volume-shadow-copy-service"></a>Usando o Serviço de Cópias de Sombra de Volume

As operações de backup e restauração do VSS usam um protocolo para a interação dos sistemas que usam gravadores (armazenamento em massa) e os que fazem backup (solicitantes).

Tanto as operações de backup quanto de restauração são direcionadas principalmente pelo solicitante, que controla o gravador e o comportamento do provedor gerando eventos COM em todo o processador para processar o gravador. Como os métodos de geração de eventos são assíncronos, os gravadores têm controle limitado no estado do solicitante por meio dos manipuladores assíncronos disponíveis para VSS (consulte [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).

Essa interação requer estruturas de dados básicas que descrevem arquivos e grupos de arquivos ([*componentes*](vssgloss-c.md)), bem como um modelo de metadados para permitir o armazenamento de informações de backup e para permitir a comunicação do gravador/solicitante.

-   [Compatibilidade do aplicativo VSS](usage-conventions.md)
-   [Configurando o VSS](configuring-vss.md)
-   [Metadados do VSS](vss-metadata.md)
-   [Trabalhando com caminhos lógicos e de seleção](working-with-selectability-and-logical-paths.md)
-   [Visão geral do processamento de um backup no VSS](overview-of-processing-a-backup-under-vss.md)
-   [Visão geral do processamento de uma restauração no VSS](overview-of-processing-a-restore-under-vss.md)

 

 



