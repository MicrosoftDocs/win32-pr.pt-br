---
description: Sincronizando o VMR com a taxa de atualização do monitor
ms.assetid: 73e73821-fb08-488a-956e-ef33f6651a26
title: Sincronizando o VMR com a taxa de atualização do monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a9550e96e6a2e35c196048d38dd5b6e5b536d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171698"
---
# <a name="synchronizing-the-vmr-to-the-monitors-refresh-rate"></a>Sincronizando o VMR com a taxa de atualização do monitor

Em cenários raros, talvez você queira sincronizar precisamente a renderização de vídeo com a taxa de atualização do monitor para que exatamente um novo quadro seja apresentado sempre que o monitor for atualizado. A maneira mais confiável de fazer isso é criar um apresentador de alocador personalizado que usa uma operação de inversão em vez de uma operação blit para gravar os bits de vídeo na superfície primária. "Flip" é chamado cada vez que o monitor é atualizado, portanto, se o fluxo de vídeo não contiver carimbos de data/hora, o VMR renderizará o mais rápido possível para a superfície primária, mas a superfície bloqueará o fluxo até que a operação de inversão seja concluída. Isso significa que, desde que a CPU não seja sobrecarregada, o próximo quadro sempre estará aguardando na superfície principal cada vez que o monitor for atualizado. No entanto, se algum outro processo de uso intensivo de CPU estiver em execução, poderá possivelmente ficar sem o thread de streaming do DirectShow para que ele não possa entregar quadros de vídeo rápido o suficiente para a superfície primária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modo de reprodução do VMR (alocador personalizado-apresentadores)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



