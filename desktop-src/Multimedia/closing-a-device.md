---
title: Fechando um dispositivo
description: Fechando um dispositivo
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- MCI_CLOSE comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824d156baa72ee404f29ae490d4d9816078f4d15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363700"
---
# <a name="closing-a-device"></a>Fechando um dispositivo

O comando [**fechar**](close.md) ([**MCI \_ Close**](mci-close.md)) libera o acesso a um dispositivo ou arquivo. O MCI libera um dispositivo quando todas as tarefas que usam um dispositivo o fecham. Para ajudar o MCI a gerenciar os dispositivos, seu aplicativo deve fechar cada dispositivo ou arquivo quando terminar de usá-lo.

Quando você fecha um dispositivo MCI externo que usa sua própria mídia em vez de arquivos (como áudio de CD), o driver deixa o dispositivo em seu modo atual de operação. Portanto, se você fechar um dispositivo de áudio de CD que está sendo executado, mesmo que o driver de dispositivo seja liberado da memória, o dispositivo de áudio de CD continuará a ser reproduzido até atingir o final de seu conteúdo.

> [!Note]  
> Fechar um aplicativo com dispositivos MCI abertos pode impedir que outros aplicativos usem esses dispositivos até que o Windows seja reiniciado.

 

 

 




