---
description: Polígonos que são coplanar em seu espaço 3D podem ser feitos para aparecer como se não fossem coplanar adicionando um Bias z a cada um.
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: Tendência de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce605ea1df161e5ebfed95c214c3dd180ab7ee6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456585"
---
# <a name="depth-bias-direct3d-9"></a>Tendência de profundidade (Direct3D 9)

Polígonos que são coplanar em seu espaço 3D podem ser feitos para aparecer como se não fossem coplanar adicionando um Bias z a cada um. Essa é uma técnica comumente usada para garantir que as sombras em uma cena sejam exibidas corretamente. Por exemplo, uma sombra em uma parede provavelmente terá o mesmo valor de profundidade que a parede. Se você renderizar o mural primeiro e, em seguida, a sombra, a sombra pode não estar visível ou os artefatos de profundidade podem estar visíveis. Você pode reverter a ordem na qual você renderiza os objetos Coplanar em espera de reversão do efeito, mas os artefatos de profundidade ainda são prováveis.

Um aplicativo pode ajudar a garantir que polígonos coplanar sejam renderizados corretamente adicionando uma tendência aos valores z que o sistema usa ao renderizar os conjuntos de polígonos coplanar. Para adicionar um Bias z a um conjunto de polígonos, chame o método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) antes de processá-los, definindo o parâmetro *State* como D3DRS \_ DEPTHBIAS e o parâmetro *Value* para um valor float adequado (por exemplo, um valor adequado pode ser de-1,0 a 1,0); para passar esse valor para **setprocessstate**, você também deve converter o valor em um **DWORD**. Um valor de tendência de z maior aumenta a probabilidade de que os polígonos processados sejam visíveis quando exibidos com outros polígonos coplanar.


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



onde m é a inclinação de profundidade máxima do triângulo que está sendo renderizado.


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



As unidades dos Estados de \_ RENDERIZAÇÃO D3DRS DEPTHBIAS e D3DRS \_ SLOPESCALEDEPTHBIAS dependem de se o buffer z ou o w-buffer está habilitado. O aplicativo deve fornecer valores adequados.

A tendência não é aplicada a nenhum primitivo de linha e ponto. No entanto, essa tendência precisa ser aplicada a triângulos desenhados no modo de wireframe.


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

[Pipeline de pixel](pixel-pipeline.md)
</dt> </dl>

 

 
