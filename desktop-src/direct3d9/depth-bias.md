---
description: Polígonos que são coplanares em seu espaço 3D podem ser feitos para aparecer como se não fosse coplanar adicionando um desvio z a cada um.
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: Desvio de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc99d606a561fd6f4eec412774ce53d9b5dd5e62c7f50b118a4e90a88664a2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523803"
---
# <a name="depth-bias-direct3d-9"></a>Desvio de profundidade (Direct3D 9)

Polígonos que são coplanares em seu espaço 3D podem ser feitos para aparecer como se não fosse coplanar adicionando um desvio z a cada um. Essa é uma técnica comumente usada para garantir que as sombras em uma cena sejam exibidas corretamente. Por exemplo, uma sombra em uma parede provavelmente terá o mesmo valor de profundidade que a parede. Se você renderizar a parede primeiro e, em seguida, a sombra, a sombra poderá não estar visível ou os artefatos de profundidade poderão estar visíveis. Você pode reverter a ordem na qual renderiza os objetos coplanar na expectativa de reverter o efeito, mas os artefatos de profundidade ainda são prováveis.

Um aplicativo pode ajudar a garantir que os polígonos coplanar sejam renderizados corretamente adicionando um desvio aos valores z que o sistema usa ao renderizar os conjuntos de polígonos coplanar. Para adicionar um desvio z a um conjunto de polígonos, chame o método [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) logo antes de renderizar, definindo o parâmetro *State* como D3DRS DEPTHBIAS e o parâmetro Value para um valor float adequado (por exemplo, um valor adequado pode ser de \_ -1,0 a 1,0); para passar esse valor para **SetRenderState,** você também deve castrar o valor para um **DWORD**.  Um valor de desvio z maior aumenta a probabilidade de que os polígonos renderizado sejam visíveis quando exibidos com outros polígonos coplanares.


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



em que m é a inclinação de profundidade máxima do triângulo que está sendo renderizado.


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



As unidades para os estados de renderização D3DRS \_ DEPTHBIAS e D3DRS \_ SLOPESCALEDEPTHBIAS dependem se o buffer z ou w-buffering está habilitado. O aplicativo deve fornecer valores adequados.

O desvio não é aplicado a nenhum primitivo de linha e ponto. No entanto, esse desvio precisa ser aplicado a triângulos desenhados no modo wireframe.


```
// RenderStates
D3DRS_SLOPESCALEDEPTHBIAS, // Defaults to zero
D3DRS_DEPTHBIAS,           // Defaults to zero
```




```
// Caps
D3DPRASTERCAPS_DEPTHBIAS           
D3DPRASTERCAPS_SLOPESCALEDEPTHBIAS 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pixel Pipeline](pixel-pipeline.md)
</dt> </dl>

 

 
