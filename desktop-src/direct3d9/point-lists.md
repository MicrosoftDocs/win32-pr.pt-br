---
description: Uma lista de ponto é uma coleção de vértices que são renderizados como pontos isolados. Seu aplicativo pode usá-los em cenas 3D para campos de estrela ou linhas pontilhadas na superfície de um polígono.
ms.assetid: 82866b07-5043-433f-974a-0a301d4b5491
title: Listas de pontos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57086a445209d9e60173910e07166a6149e0b8d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645969"
---
# <a name="point-lists"></a>Listas de pontos

Uma lista de ponto é uma coleção de vértices que são renderizados como pontos isolados. Seu aplicativo pode usá-los em cenas 3D para campos de estrela ou linhas pontilhadas na superfície de um polígono.

A ilustração a seguir mostra uma lista de ponto renderizada.

![ilustração de uma lista de ponto](images/pointlst.png)

Seu app pode aplicar materiais e texturas a uma lista de ponto. As cores na textura ou no material aparecem apenas nos pontos desenhados e não entre os pontos.

O código a seguir mostra como criar vértices para essa lista de pontos.


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



O exemplo de código abaixo mostra como renderizar esta lista de pontos no Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_POINTLIST, 0, 6 );
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Primitivos](primitives.md)
</dt> </dl>

 

 
