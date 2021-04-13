---
description: O mecanismo de iluminação Direct3D pode usar dados de cor por vértice ao executar a iluminação se você informar ao tempo de execução que os dados estão presentes.
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: Estado de cor de Per-Vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0104b427753fa3d7b7cf5a0a5a10cfeb5d10f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370051"
---
# <a name="per-vertex-color-state-direct3d-9"></a>Estado de cor de Per-Vertex (Direct3D 9)

O mecanismo de iluminação Direct3D pode usar dados de cor por vértice ao executar a iluminação se você informar ao tempo de execução que os dados estão presentes. Isso é feito ativando o seguinte estado de renderização:


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



Se a cor por vértice estiver habilitada, os aplicativos poderão configurar a origem da qual o sistema recupera informações de cores para um vértice. Os \_ Estados de RENDERIZAÇÃO D3DRS AMBIENTMATERIALSOURCE, D3DRS \_ DiffuseMaterialSource, D3DRS \_ EMISSIVEMATERIALSOURCE e D3DRS \_ SPECULARMATERIALSOURCE controlam as fontes de componente de cor ambiente, difuso, emissiva e especular, respectivamente. Cada Estado pode ser definido como membros do tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) , que define constantes que instruem o sistema a usar o material atual, a cor difusa ou a cor especular como a origem do componente de cor especificado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processar Estados](render-states.md)
</dt> </dl>

 

 
