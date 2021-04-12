---
title: Estratégias de desenho multithread OpenGL
description: O GDI não dá suporte a vários threads.
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- OpenGL no Windows, desenho multithread
- multithread OpenGL Drawing OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bccb08d48bd8ccb62584f15911a1eb65080c4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292065"
---
# <a name="multithread-opengl-drawing-strategies"></a>Estratégias de desenho multithread OpenGL

O GDI não dá suporte a vários threads. Você deve usar um contexto de dispositivo distinto e um contexto de renderização distinto para cada thread. Isso tende a limitar as vantagens de desempenho do uso de vários threads com sistemas de processador único executando aplicativos OpenGL. No entanto, há maneiras de usar threads com um sistema de processador único para aumentar significativamente o desempenho. Por exemplo, você pode usar um thread separado para passar chamadas de renderização OpenGL para hardware 3D dedicado.

Os sistemas SMP (multiprocessamento simétrico) podem se beneficiar muito do uso de vários threads. Uma estratégia óbvia é usar um thread separado para cada processador para lidar com a renderização de OpenGL em janelas separadas. Por exemplo, em um aplicativo de simulação de voo, você poderia usar processadores e threads separados para renderizar os modos de exibição frontal, voltar e lateral.

Um thread pode ter apenas um contexto de renderização ativo atual. Ao usar vários threads e vários contextos de renderização, você deve ter cuidado para sincronizar seu uso. Por exemplo, use um thread somente para chamar [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) depois que todos os threads terminarem de desenhar.

 

 




