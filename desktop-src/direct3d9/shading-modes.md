---
description: O modo de sombreamento usado para renderizar um polígono tem um efeito profundo em sua aparência. Os modos de sombreamento determinam a intensidade da cor e da iluminação a qualquer momento em um rosto de polígono. O Direct3D dá suporte a dois modos de sombreamento.
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: Modos de sombreamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714e9610e1cae344148bf78ef39bc5e8355cb2af6395e3f92a3bc01b87860605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092215"
---
# <a name="shading-modes-direct3d-9"></a>Modos de sombreamento (Direct3D 9)

O modo de sombreamento usado para renderizar um polígono tem um efeito profundo em sua aparência. Os modos de sombreamento determinam a intensidade da cor e da iluminação a qualquer momento em um rosto de polígono. O Direct3D dá suporte a dois modos de sombreamento.

-   [Sombreamento simples](#flat-shading)
-   [Sombreamento do Gouraud](#gouraud-shading)

## <a name="flat-shading"></a>Sombreamento simples

No modo de sombreamento simples, o pipeline de renderização direct3D renderiza um polígono, usando a cor do material de polígono em seu primeiro vértice como a cor de todo o polígono. Objetos 3D renderizados com sombreamento simples terão bordas visivelmente fortes entre polígonos se não são coplanares.

A ilustração a seguir mostra um bule renderizado com sombreamento simples. O contorno de cada polígono é claramente visível. Sombreamento simples é a forma mais rápida de sombreamento.

![ilustração de um bule usando sombreamento simples](images/flattea.png)

## <a name="gouraud-shading"></a>Sombreamento do Gouraud

Quando o Direct3D renderiza um polígono usando o sombreamento do Gouraud, ele calcula uma cor para cada vértice usando os parâmetros de iluminação e normal do vértice. Em seguida, ele interpola a cor na face dos polígonos A interpolação é feita linearmente. Por exemplo, se o componente vermelho da cor do vértice 1 for 0,8 e o componente vermelho do vértice 2 for 0,4, usando o modo de sombreamento gouraud e o modelo de cor RGB, o módulo de iluminação Direct3D atribuirá um componente vermelho de 0,6 ao pixel no ponto médio da linha entre esses vértices.

A ilustração a seguir demonstra o sombreamento do Gouraud. Esse bule é composto por muitos polígonos simples e triangulares. No entanto, o sombreamento do Gouraud faz com que a superfície do objeto pareça curva e suave.

![ilustração do bule usando sombreamento gouraud](images/gourtea.png)

O sombreamento do Gouraud também pode ser usado para exibir objetos com bordas pontiagudas.

Para obter mais informações, consulte Vetores normais de face e [vértice (Direct3D 9)](face-and-vertex-normal-vectors.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreamento](shading.md)
</dt> </dl>

 

 



