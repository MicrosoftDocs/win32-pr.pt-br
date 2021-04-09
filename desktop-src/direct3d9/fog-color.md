---
description: A cor de neblina para sombra de pixel e Vertex é definida por meio do \_ estado de RENDERIZAÇÃO D3DRS FOGCOLOR. Os valores do estado de renderização podem ser qualquer cor RGB, especificada como uma cor RGBA. O componente alfa é ignorado.
ms.assetid: 76366496-553d-4dbf-868d-d58b5377d36a
title: Cor da neblina (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c9ae217a26ab38be5e3f232fb9dfcd4c2977f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009873"
---
# <a name="fog-color-direct3d-9"></a>Cor da neblina (Direct3D 9)

A cor de neblina para sombra de pixel e Vertex é definida por meio do \_ estado de RENDERIZAÇÃO D3DRS FOGCOLOR. Os valores do estado de renderização podem ser qualquer cor RGB, especificada como uma cor RGBA. O componente alfa é ignorado.

O exemplo de C++ a seguir define a cor de neblina como branco.


```
/* For this example, the d3dDevice variable is
* a valid pointer to an IDirect3DDevice9 interface.
*/
HRESULT hr;
hr = d3dDevice->SetRenderState(
                    D3DRS_FOGCOLOR,
                    0x00FFFFFF); // Highest 8 bits are not used.
if(FAILED(hr))
    return hr;
```



A neblina é aplicada de forma diferente pelo pipeline de função fixa e pelo pipeline programável.

1.  Se o driver oferecer suporte a D3DPMISCCAPS \_ FOGANDSPECULARALPHA:
    -   Se o pipeline de função fixa for usado e D3DRS \_ FOGCOLOR for definido, v1. w (no sombreador de pixel) será igual ao valor definido em neblina RenderState.
    -   Se o pipeline programável for usado, v1. w (no sombreador de pixels) é igual a 0, mesmo que oD1. w seja explicitamente escrito em um sombreador de vértice.
2.  Se o driver não oferecer suporte a D3DPMISCCAPS \_ FOGANDSPECULARALPHA:
    -   Se o pipeline de função fixa for usado e D3DRS \_ FOGCOLOR for definido, então v1. w (no sombreador de pixel) é igual ao valor definido em neblina renderingstate.
    -   Se oFog for explicitamente gravado em um sombreador de vértice, v1. w (no sombreador de pixel) é igual a oFog, clamped entre 0 e 1.
    -   Se nenhum dos dois casos acima se aplicar, v1. w (no sombreador de pixels) é igual a 0, mesmo se oD1. w for explicitamente escrito em um sombreador de vértice.

Para obter mais informações, consulte [D3DPMISCCAPS](d3dpmisccaps.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de neblina](fog-types.md)
</dt> </dl>

 

 



