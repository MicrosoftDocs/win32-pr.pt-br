---
description: Uma lista de triângulos é uma lista de triângulos isolados. Eles podem ou não estar próximos uns dos outros. Uma lista de triângulos deve ter pelo menos três vértices e o número total de vértices deve ser divisível por três.
ms.assetid: e5c3470f-361c-458a-a42a-3549c51d8794
title: Listas de triângulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230cac9b4120d31821d70db022ab50d311d7b73e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105791465"
---
# <a name="triangle-lists"></a>Listas de triângulo

Uma lista de triângulos é uma lista de triângulos isolados. Eles podem ou não estar próximos uns dos outros. Uma lista de triângulos deve ter pelo menos três vértices e o número total de vértices deve ser divisível por três.

Use listas de triângulos para criar um objeto que é composto de peças separadas. Por exemplo, uma maneira de criar uma parede de campo de força em um jogo 3D é especificando uma grande lista de triângulos pequenos, desconectados. Em seguida, aplique um material e textura que parece emitir luz à lista de triângulos. Cada triângulo na parede parece brilhar. A cena por trás da parede fica parcialmente visível por meio dos espaços entre os triângulos, da forma que um jogador pode esperar ao olhar para um campo de força.

As listas de triângulo também são úteis para criar primitivos que têm bordas afiadas e são sombreados com sombreamento Gouraud. Consulte [vetores normais de face e vértice (Direct3D 9)](face-and-vertex-normal-vectors.md).

A ilustração a seguir ilustra uma lista de triângulos renderizada.

![Ilustração de uma lista de triângulos renderizada](images/trilist.png)

O código a seguir mostra como criar vértices para essa lista de triângulos.


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



O exemplo de código abaixo mostra como renderizar esta lista de triângulos no Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 2 );
```



Você também pode usar as faixas de triângulo para renderizar triângulos que não estão conectados entre si. Para fazer isso, especifique um triângulo degenerado (ou seja, um triângulo com tamanho zero) na lista; Isso criará uma linha entre os dois triângulos que não serão exibidos durante a renderização. Por exemplo, para renderizar apenas o primeiro e o último triângulo do exemplo anterior, inicialize o buffer de vértice com os seguintes vértices:


```
CUSTOMVERTEX Vertices[] =
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    { 5.0, -5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Primitivos](primitives.md)
</dt> </dl>

 

 
