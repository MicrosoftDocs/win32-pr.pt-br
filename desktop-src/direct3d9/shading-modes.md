---
description: O modo de sombreamento usado para renderizar um polígono tem um efeito profundo sobre sua aparência. Os modos de sombreamento determinam a intensidade de cor e iluminação em qualquer ponto em um título de polígono. O Direct3D dá suporte a dois modos de sombreamento.
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: Modos de sombreamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84e791bed0098838760f10f6605f716444e7688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104558223"
---
# <a name="shading-modes-direct3d-9"></a>Modos de sombreamento (Direct3D 9)

O modo de sombreamento usado para renderizar um polígono tem um efeito profundo sobre sua aparência. Os modos de sombreamento determinam a intensidade de cor e iluminação em qualquer ponto em um título de polígono. O Direct3D dá suporte a dois modos de sombreamento.

-   [Sombreamento simples](#flat-shading)
-   [Sombreamento Gouraud](#gouraud-shading)

## <a name="flat-shading"></a>Sombreamento simples

No modo de sombreamento simples, o pipeline de renderização do Direct3D renderiza um polígono, usando a cor do material do polígono em seu primeiro vértice como a cor do polígono inteiro. objetos 3D que são renderizados com sombreamento simples têm bordas nítidas visivelmente entre polígonos se não forem coplanar.

A ilustração a seguir mostra um bule renderizado com sombreamento simples. O contorno de cada polígono é claramente visível. O sombreamento simples é a forma mais rápida de sombreamento.

![ilustração de um bule usando sombreamento simples](images/flattea.png)

## <a name="gouraud-shading"></a>Sombreamento Gouraud

Quando o Direct3D renderiza um polígono usando sombreamento Gouraud, ele computa uma cor para cada vértice usando os parâmetros normal de vértice e iluminação. Em seguida, ele interpola a cor na face dos polígonos que a interpolação é feita linearmente. Por exemplo, se o componente vermelho da cor do vértice 1 for 0,8 e o componente vermelho do vértice 2 for 0,4, usando o modo de sombreamento Gouraud e o modelo de cores RGB, o módulo Direct3D Lighting atribuirá um componente vermelho de 0,6 para o pixel no ponto médio da linha entre esses vértices.

A ilustração a seguir demonstra o sombreamento Gouraud. Esse bule é composto por muitos polígonos simples e triangulares. No entanto, o sombreamento de Gouraud faz com que a superfície do objeto pareça curva e suave.

![ilustração de bule usando sombreamento Gouraud](images/gourtea.png)

O sombreamento de Gouraud também pode ser usado para exibir objetos com bordas nítidas.

Para obter mais informações, consulte [vetores normais de face e vértice (Direct3D 9)](face-and-vertex-normal-vectors.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreamento](shading.md)
</dt> </dl>

 

 



