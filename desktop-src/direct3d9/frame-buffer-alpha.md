---
description: A combinação alfa do buffer de quadro é um pouco diferente do alfa do vértice, alfa do material e alfa de textura.
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: Buffer de quadro alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec091e8cc42d6b21142d3b9372f6d2931ba25d1dfe12aa7717e0b09acf0b0718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297491"
---
# <a name="frame-buffer-alpha-direct3d-9"></a>Buffer de quadro alfa (Direct3D 9)

A combinação alfa do buffer de quadro é um pouco diferente do alfa do vértice, alfa do material e alfa de textura. Valores de transparência de conjunto alfa de vértice, material e textura que são usados apenas para o primitivo atual e, por si só, não têm nenhum efeito em outros primitivos. A combinação alfa do buffer de quadros controla como o primitivo atual é combinado com pixels existentes no buffer de quadro para produzir uma cor de pixel final.

Ao executar a combinação alfa, duas cores estão sendo combinadas: uma cor de origem e uma cor de destino. A cor de origem é do objeto transparente, a cor de destino é a cor que já está no local do pixel. A cor de destino é o resultado da renderização de algum outro objeto que está atrás do objeto transparente, ou seja, o objeto que ficará visível por meio do objeto transparente. A combinação alfa usa uma fórmula para controlar a proporção entre os objetos de origem e de destino.


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



ObjectColor é a contribuição do primitivo que está sendo renderizado no local do pixel atual. PixelColor é a contribuição do buffer de quadro no local do pixel atual.

O conjunto de fatores de combinação alfa que pode ser usado está listado abaixo.



| Fator do modo Blend         | Descrição                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DBLEND \_ ZERO            | (0, 0, 0, 0)                                                                                                                                                                             |
| D3DBLEND \_ ONE             | (1, 1, 1, 1)                                                                                                                                                                             |
| D3DBLEND \_ SRCCOLOR        | (Rs, Gs, Bs, As)                                                                                                                                                                         |
| D3DBLEND \_ INVSRCCOLOR     | (1-Rs, 1-Gs, 1-Bs, 1-As)                                                                                                                                                                 |
| D3DBLEND \_ SRCALPHA        | (As, As, As, As)                                                                                                                                                                         |
| D3DBLEND \_ INVSRCALPHA     | (1-As, 1-As, 1-As, 1-As)                                                                                                                                                                 |
| D3DBLEND \_ DESTALPHA       | (Ad, Ad, Ad, Ad)                                                                                                                                                                         |
| D3DBLEND \_ INVDESTALPHA    | (1-Ad, 1-Ad, 1-Ad, 1-Ad)                                                                                                                                                                 |
| D3DBLEND \_ DESTCOLOR       | (Rd, Gd, Bd, Ad)                                                                                                                                                                         |
| D3DBLEND \_ INVDESTCOLOR    | (1-Rd, 1-Gd, 1-Bd, 1-Ad)                                                                                                                                                                 |
| D3DBLEND \_ SRCALPHASAT     | (f, f, f, 1); f = min(As, 1-Ad)                                                                                                                                                          |
| D3DBLEND \_ BOTHSRCALPHA    | Obsoleto para DirectX 6 e posterior. Você pode obter o mesmo efeito definindo os fatores de combinação de origem e destino como D3DBLEND \_ SRCALPHA e D3DBLEND \_ INVSRCALPHA em chamadas separadas. |
| D3DBLEND \_ BOTHINVSRCALPHA | Obsoleto para DirectX 6. Você pode obter o mesmo efeito definindo os fatores de combinação de origem e destino como D3DBLEND \_ INVSRCALPHA e D3DBLEND SRCALPHA em chamadas \_ separadas.           |
| D3DBLEND \_ BLENDFACTOR     | Use color.r, color.g, color.b e color.a obtidos da configuração \_ BLENDFACTOR D3DRS.                                                                                                 |
| D3DBLEND \_ INVBLENDFACTOR  | Use 1-color.r, 1-color.g, 1-color.b e 1-color.a obtidos da configuração \_ BLENDFACTOR D3DRS.                                                                                         |



 

O Direct3D usa o estado de \_ renderização ALPHABLENDENABLE D3DRS para habilitar a combinação de transparência alfa. O tipo de combinação alfa que é feita depende dos estados de renderização D3DRS \_ SRCBLEND e D3DRS \_ DESTBLEND. Os estados de combinação de origem e destino são usados em pares. O fragmento de código a seguir define o estado de combinação de origem como D3DBLEND SRCCOLOR e o estado de combinação de destino \_ como D3DBLEND \_ INVSRCCOLOR.


```
// This code fragment assumes that lpD3DDevice is a 
//   valid pointer to a device.

// Enable alpha blending.
lpD3DDevice->SetRenderState(D3DRS_ALPHABLENDENABLE, 
                            TRUE);

// Set the source blend state.
lpD3DDevice->SetRenderState(D3DRS_SRCBLEND, 
                            D3DBLEND_SRCCOLOR);

// Set the destination blend state.
lpD3DDevice->SetRenderState(D3DRS_DESTBLEND, 
                            D3DBLEND_INVSRCCOLOR);
```



Esse código executa uma combinação linear entre a cor de origem (a cor do primitivo que está sendo renderizado no local atual) e a cor de destino (a cor no local atual no buffer de quadro). A aparência resultante é semelhante ao vidro com sinal de que parte da cor do objeto de destino parece ser transmitida por meio do objeto de origem; o restante parece ser absorbed.

Muitos desses fatores de combinação exigem valores alfa na textura para operar corretamente. Portanto, ao usar vértice ou alfa de material, o aplicativo é restrito quanto a quais modos produzirão resultados interessantes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Combinação alfa](alpha-blending.md)
</dt> </dl>

 

 



