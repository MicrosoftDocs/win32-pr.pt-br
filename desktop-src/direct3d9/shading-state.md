---
description: O Direct3D dá suporte a sombreamento simples e Gouraud. O padrão é sombreamento Gouraud. Para controlar o modo de sombreamento atual, seu aplicativo C++ especifica um membro do tipo enumerado D3DSHADEMODE para o \_ estado de RENDERIZAÇÃO D3DRS shadmode.
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: Estado de sombreamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebac826704fee0e1903c1aa2a2348bff4a089c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105802065"
---
# <a name="shading-state-direct3d-9"></a>Estado de sombreamento (Direct3D 9)

O Direct3D dá suporte a sombreamento simples e Gouraud. O padrão é sombreamento Gouraud. Para controlar o modo de sombreamento atual, seu aplicativo C++ especifica um membro do tipo enumerado [**D3DSHADEMODE**](./d3dshademode.md) para o \_ estado de renderização D3DRS shadmode.

O exemplo de código C++ a seguir demonstra o processo de definir o estado de sombreamento para o modo de sombreamento simples.


```
// This code example assumes that d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface.
// Set the shading state.
d3dDevice->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processar Estados](render-states.md)
</dt> </dl>

 

 
