---
description: Uma faixa de triângulos é uma série de triângulos conectados.
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: Faixas de triângulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2766529a37b994e5fe30815ca6300476f06c7d4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566234"
---
# <a name="triangle-strips"></a>Faixas de triângulo

Uma faixa de triângulos é uma série de triângulos conectados. Como os triângulos são conectados, o aplicativo não precisa especificar repetidamente todos os três vértices de cada triângulo. Por exemplo, você precisa de apenas sete vértices para definir a faixa de triângulos a seguir.

![ilustração de uma faixa de triângulos com sete vértices](images/tristrip.png)

O sistema usa os vértices v1, v2 e v3 para desenhar o primeiro triângulo; v2, v4 e v3 para desenhar o segundo triângulo; v3, v4 e v5 para desenhar o terceiro; V4 e v6 v5 para desenhar o quarto; e assim por diante. Observe que os vértices do segundo e do quarto triângulo estão fora de ordem; isso é necessário para garantir que todos os triângulos sejam desenhados em uma orientação no sentido horário.

A maioria dos objetos em cenas 3D são compostos por faixas de triângulos. Isso ocorre porque as faixas de triângulos podem ser usadas para especificar objetos complexos de maneira a fazer uso eficiente da memória e do tempo de processamento.

A ilustração a seguir ilustra uma faixa de triângulos renderizado.

![ilustração de uma faixa de triângulos renderizada](images/tstrip2.png)

O código a seguir mostra como criar vértices para essa faixa de triângulos.


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



O exemplo de código abaixo mostra como renderizar essa faixa de triângulo no Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



Use uma faixa de triângulo para renderizar triângulos que não estão conectados entre si. Para fazer isso, especifique um triângulo degenerado (ou seja, um triângulo cuja área seja zero) na lista de triângulos. Isso cria uma linha entre os dois triângulos que não serão renderizados. Para renderizar apenas o primeiro e o último triângulos do exemplo anterior, modifique o buffer de vértice conforme mostrado aqui:


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

 

 
