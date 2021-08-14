---
description: Uma faixa de linhas é um primitivo composto de segmentos de linha conectados.
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: Faixas de linha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8ba98518cac542a9b8272e4f96494889ef24f269744626aa24e882c7af509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799623"
---
# <a name="line-strips"></a>Faixas de linha

Uma faixa de linhas é um primitivo composto de segmentos de linha conectados. O app pode usar faixas de linhas para criar polígonos não fechados. Um polígono fechado tem o último vértice conectado ao primeiro por um segmento de linhas. Se o app faz polígonos com base em faixas alinhadas, os vértices não têm garantia de estar coplanares.

A ilustração a seguir mostra uma faixa de linhas renderizada.

![Ilustração de uma faixa de linhas](images/linstrip.gif)

O código a seguir mostra como criar vértices para essa faixa de linhas.


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



O exemplo de código abaixo mostra como renderizar uma faixa de linha no Direct3D 9 usando [**IDirect3DDevice9::D rawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINESTRIP, 0, 5 );
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Primitivos](primitives.md)
</dt> </dl>

 

 
