---
description: A restauração de arquivo em um sistema em execução pode ser problemática. É importante que a execução de aplicativos (autores) indique o que fazer quando surgirem dificuldades durante as restaurações, por exemplo, se o arquivo que está sendo restaurado estiver em uso no momento.
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: Configurações de restauração do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48b3486128c6a91f601a89d697a4db9d8ab27fe9d3ac4cbef28dc870928d37d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344190"
---
# <a name="vss-restore-configurations"></a>Configurações de restauração do VSS

A restauração de arquivo em um sistema em execução pode ser problemática. É importante que a execução de aplicativos (autores) indique o que fazer quando surgirem dificuldades durante as restaurações, por exemplo, se o arquivo que está sendo restaurado estiver em uso no momento.

No VSS, os autores têm duas maneiras complementares de gerenciar restaurações:[*métodos de restauração*](vssgloss-r.md) e [*destinos de restauração.*](vssgloss-r.md)

Além disso, os solicitantes podem optar por restaurar arquivos para locais não especificados anteriormente e notificar os autores (consulte [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).

O método de restauração (também chamar o destino de restauração original) é especificado por um autor em um momento de backup e define uma definição de todo o autor do método a ser usado para restaurar todos os seus componentes no futuro. Todos os arquivos e componentes gerenciados por um autor compartilham o mesmo método de restauração.

Os destinos de restauração permitem que os autores alterem a maneira como os componentes específicos devem ser restaurados no momento da restauração. Ao contrário dos métodos de restauração, os destinos de restauração são definidos para um conjunto de componentes.

Uma discussão detalhada sobre o uso de métodos de restauração e destinos de restauração é encontrada nos tópicos listados abaixo:

-   [Estado de restauração do VSS](vss-restore-state.md)
-   [Definição de métodos de restauração do VSS](setting-vss-restore-methods.md)
-   [Definindo destinos de restauração do VSS](setting-vss-restore-targets.md)
-   [Definindo opções de restauração do VSS](setting-vss-restore-options.md)

(Para obter informações sobre restaurações que não usam esses mecanismos, consulte [Restaurações sem participação do autor](restores-without-writer-participation.md).)

 

 



