---
description: A restauração de arquivos em um sistema em execução pode ser problemática. É importante que a execução de aplicativos (gravadores) indique o que fazer quando surgirem dificuldades durante restaurações, por exemplo, se o arquivo que está sendo restaurado estiver em uso no momento.
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: Configurações de restauração do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13acfc59f250a859e9c62f2df2e1b1b982608ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090443"
---
# <a name="vss-restore-configurations"></a>Configurações de restauração do VSS

A restauração de arquivos em um sistema em execução pode ser problemática. É importante que a execução de aplicativos (gravadores) indique o que fazer quando surgirem dificuldades durante restaurações, por exemplo, se o arquivo que está sendo restaurado estiver em uso no momento.

No VSS, os gravadores têm duas maneiras complementares de gerenciar restaurações —[*métodos de restauração*](vssgloss-r.md) e [*destinos de restauração*](vssgloss-r.md).

Além disso, os solicitantes podem optar por restaurar os arquivos para os locais não especificados anteriormente e notificar os gravadores (consulte [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).

O método Restore (também chama o destino de restauração original) é especificado por um gravador em um horário de backup e define uma definição de todo o gravador do método a ser usado para restaurar todos os seus componentes no futuro. Todos os arquivos e componentes gerenciados por um gravador compartilham o mesmo método de restauração.

Os destinos de restauração permitem que os gravadores alterem como os componentes específicos devem ser restaurados no momento da restauração. Ao contrário dos métodos de restauração, os destinos de restauração são definidos para um conjunto de componentes.

Uma discussão detalhada sobre o uso de métodos de restauração e destinos de restauração é encontrada nos tópicos listados abaixo:

-   [Estado de restauração do VSS](vss-restore-state.md)
-   [Definição de métodos de restauração do VSS](setting-vss-restore-methods.md)
-   [Definindo destinos de restauração do VSS](setting-vss-restore-targets.md)
-   [Definindo opções de restauração do VSS](setting-vss-restore-options.md)

(Para obter informações sobre restaurações que não usam esses mecanismos, consulte [restaurações sem participação no gravador](restores-without-writer-participation.md).)

 

 



