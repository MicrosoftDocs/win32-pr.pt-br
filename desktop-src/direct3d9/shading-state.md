---
description: O Direct3D dá suporte a sombreamento simples e Gouraud. O padrão é sombreamento Gouraud. Para controlar o modo de sombreamento atual, seu aplicativo C++ especifica um membro do tipo enumerado D3DSHADEMODE para o \_ estado de RENDERIZAÇÃO D3DRS shadmode.
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: Estado de sombreamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f28514fefbf39e75bd84a0ae56324fd859f0fd85fa4a25449e349ce592ab3b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727596"
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

 

 
