---
description: O buffer de quadro alpha-blending é um pouco diferente do vértice alfa, do material alfa e da textura alfa.
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: Buffer de quadro alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb310e2c66f43282e65425fd0d6c6a24961accaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087385"
---
# <a name="frame-buffer-alpha-direct3d-9"></a>Buffer de quadro alfa (Direct3D 9)

O buffer de quadro alpha-blending é um pouco diferente do vértice alfa, do material alfa e da textura alfa. O vértice, o material e a textura Alpha definem valores de transparência que são usados apenas para o primitivo atual e, por si só, não têm nenhum efeito em outros primitivos. Mesclagem alfa do buffer de quadros controla como o primitivo atual é combinado com pixels existentes no buffer de quadro para gerar uma cor de pixel final.

Ao executar a mesclagem alfa, duas cores estão sendo combinadas: uma cor de origem e uma cor de destino. A cor de origem é do objeto transparente, a cor de destino é a cor que já está no local do pixel. A cor de destino é o resultado da renderização de algum outro objeto que está atrás do objeto transparente, ou seja, o objeto que ficará visível por meio do objeto transparente. A mistura alfa usa uma fórmula para controlar a taxa entre os objetos de origem e de destino.


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



Objectcolor é a contribuição do primitivo que está sendo renderizado no local atual do pixel. PixelColor é a contribuição do buffer de quadro no local do pixel atual.

O conjunto de fatores de mistura alfa que podem ser usados está listado abaixo.



| Fator de modo de mesclagem         | Descrição                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DBLEND \_ zero            | (0, 0, 0, 0)                                                                                                                                                                             |
| D3DBLEND \_ um             | (1, 1, 1, 1)                                                                                                                                                                             |
| D3DBLEND \_ SRCCOLOR        | (RS, GS, BS, as)                                                                                                                                                                         |
| D3DBLEND \_ INVSRCCOLOR     | (1-RS, 1-GS, 1-BS, 1-como)                                                                                                                                                                 |
| D3DBLEND \_ SRCALPHA        | (As, as, as, as)                                                                                                                                                                         |
| D3DBLEND \_ INVSRCALPHA     | (1-como, 1-como, 1-como, 1-como)                                                                                                                                                                 |
| D3DBLEND \_ DESTALPHA       | (AD, AD, AD, AD)                                                                                                                                                                         |
| D3DBLEND \_ INVDESTALPHA    | (1-AD, 1-AD, 1-AD, 1-AD)                                                                                                                                                                 |
| D3DBLEND \_ DESTCOLOR       | (RD, GD, BD, AD)                                                                                                                                                                         |
| D3DBLEND \_ INVDESTCOLOR    | (1-Rd, 1-gd, 1-BD, 1-AD)                                                                                                                                                                 |
| D3DBLEND \_ SRCALPHASAT     | (f, f, f, 1); f = min (as, 1-AD)                                                                                                                                                          |
| D3DBLEND \_ BOTHSRCALPHA    | Obsoleto para DirectX 6 e posterior. Você pode obter o mesmo efeito definindo os fatores de mesclagem de origem e de destino como D3DBLEND \_ SRCALPHA e D3DBLEND \_ INVSRCALPHA em chamadas separadas. |
| D3DBLEND \_ BOTHINVSRCALPHA | Obsoleto para DirectX 6. Você pode obter o mesmo efeito definindo os fatores de mesclagem de origem e de destino como D3DBLEND \_ INVSRCALPHA e D3DBLEND \_ SRCALPHA em chamadas separadas.           |
| D3DBLEND \_ BLENDFACTOR     | Use Color. r, Color. g, Color. b e Color. a obtida da \_ configuração D3DRS BLENDFACTOR.                                                                                                 |
| D3DBLEND \_ INVBLENDFACTOR  | Use 1-Color. r, 1-Color. g, 1-Color. b e 1-Color. a obtida na \_ configuração D3DRS BLENDFACTOR.                                                                                         |



 

O Direct3D usa o \_ estado de RENDERIZAÇÃO D3DRS ALPHABLENDENABLE para habilitar a mesclagem de transparência alfa. O tipo de mistura alfa que é feito depende dos \_ Estados de RENDERIZAÇÃO D3DRS SRCBLEND e \_ D3DRS DESTBLEND. Os Estados de mesclagem de origem e destino são usados em pares. O fragmento de código a seguir define o estado de mesclagem de origem como D3DBLEND \_ SRCCOLOR e o estado de mesclagem de destino como D3DBLEND \_ INVSRCCOLOR.


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



Esse código executa uma combinação linear entre a cor de origem (a cor da primitiva que está sendo renderizada no local atual) e a cor de destino (a cor no local atual no buffer de quadro). A aparência resultante é semelhante ao vidro colorido, pois parte da cor do objeto de destino parece ser transmitida por meio do objeto de origem; o restante dele parece ser absorvido.

Muitos desses fatores de mistura exigem valores Alfa na textura para operar corretamente. Portanto, ao usar o vértice ou o material alfa, o aplicativo é restrito ao que os modos produzirão resultados interessantes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem alfa](alpha-blending.md)
</dt> </dl>

 

 



