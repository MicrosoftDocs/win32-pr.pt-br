---
description: Uma lista de linhas contém segmentos de linha reta isolados.
ms.assetid: bb02b3d6-f30f-4f2b-8b40-a7e37faf524a
title: Listas de linhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f06ca68e3fefab1217e77bbf41bc30aa42dac9631b70480fe4bf0a98d38d913
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606787"
---
# <a name="line-lists"></a>Listas de linhas

Uma lista de linhas contém segmentos de linha reta isolados. As listas de linhas são úteis para tarefas como adicionar chuva com neve ou pesada a uma cena 3D. Os apps criam uma lista de linhas preenchendo uma matriz de vértices. Observe que o número de vértices em uma lista de linhas deve ser um número par maior ou igual a dois.

A ilustração a seguir mostra uma lista de linha renderizada.

![Ilustração de uma lista de linhas](images/linelst.png)

Você pode aplicar materiais e texturas a uma lista de linhas. As cores no material ou na textura aparecem somente nas linhas desenhadas, não em qualquer ponto entre as linhas.

O código a seguir mostra como criar vértices para essa lista de linhas.


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



O exemplo de código abaixo mostra como renderizar uma lista de linhas no Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINELIST, 0, 3 );
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Primitivos](primitives.md)
</dt> </dl>

 

 
