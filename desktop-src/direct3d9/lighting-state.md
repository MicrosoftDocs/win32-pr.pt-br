---
description: Se você não acender com um sombreador de vértice ou um sombreador de pixel, poderá optar por usar o mecanismo de iluminação no tempo de execução.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: Estado de iluminação (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5935590c46776c621535968f4d457f3738d83d02342ffddf832cbf0278bbd9ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674266"
---
# <a name="lighting-state-direct3d-9"></a>Estado de iluminação (Direct3D 9)

Se você não acender com um sombreador de vértice ou um sombreador de pixel, poderá optar por usar o mecanismo de iluminação no tempo de execução. O mecanismo de iluminação requer que os dados de vértice contenham normalidades por vértice; os vértices sem dados normais gerarão um produto de ponto zero em todos os cálculos de iluminação. Os cálculos de iluminação são abordados em mais detalhes na [matemática de iluminação (Direct3D 9)](mathematics-of-lighting.md).

Para habilitar o mecanismo de iluminação, use:


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processar Estados](render-states.md)
</dt> </dl>

 

 



