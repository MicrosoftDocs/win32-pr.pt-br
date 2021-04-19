---
description: Adicionar a neblina a uma cena 3D pode aprimorar o realm, fornecer ambiance ou definir um humor, e os artefatos obscuros às vezes são causados quando a geometria distante chega à exibição.
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: Neblina (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b9ed234bef0f3dea76baa98390f25e9b2003a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105771319"
---
# <a name="fog-direct3d-9"></a>Neblina (Direct3D 9)

Adicionar a neblina a uma cena 3D pode aprimorar o realm, fornecer ambiance ou definir um humor, e os artefatos obscuros às vezes são causados quando a geometria distante chega à exibição. O Direct3D dá suporte a dois modelos de neblina, sombra de pixel e neblina de vértice, cada um com seus próprios recursos e interface de programação.

Essencialmente, a neblina é implementada combinando a cor dos objetos em uma cena com uma cor de neblina escolhida com base na profundidade de um objeto em uma cena ou em sua distância do ponto de vista. À medida que os objetos crescem mais distantes, sua cor original se mistura cada vez mais com a cor de neblina escolhida, criando a ilusão de que o objeto está sendo mais obscuro por pequenas partículas flutuantes na cena. A ilustração a seguir mostra uma cena renderizada sem neblina e uma cena semelhante renderizada com a neblina habilitada.

![ilustração da mesma cena com e sem sombra](images/fogcomp.png)

Nesta ilustração, a cena à esquerda tem um horizonte claro, além do qual nenhum cenário está visível, embora fique visível no mundo real. A cena à direita obscurece o horizonte usando uma cor de neblina idêntica à cor do plano de fundo, fazendo com que os polígonos pareçam desaparecer na distância. Ao combinar efeitos discretos de neblina com o design de cena criativa, você pode adicionar humor e suavizar a cor dos objetos em uma cena.

O Direct3D fornece duas maneiras de adicionar a neblina a uma cena: sombra de pixel e neblina de vértice, chamados de como os efeitos de neblina são aplicados. Para obter detalhes, consulte [sombra de pixel (Direct3D 9)](pixel-fog.md) e [neblina de vértice (Direct3D 9)](vertex-fog.md). Em suma, a neblina de pixel – também chamada de sombra de tabela – é implementada no driver de dispositivo e a neblina de vértice é implementada no mecanismo de iluminação Direct3D. Um aplicativo pode implementar a neblina com um sombreador de vértice e sombra de pixel simultaneamente, se desejado.

> [!Note]  
> Independentemente de você usar sombra de pixel ou vértice, seu aplicativo deve fornecer uma matriz de projeção compatível para garantir que os efeitos de neblina sejam aplicados corretamente. Essa restrição se aplica até mesmo a aplicativos que não usam o mecanismo de transformação e iluminação do Direct3D. Para obter detalhes adicionais sobre como você pode fornecer uma matriz apropriada, consulte [projetion Transform (Direct3D 9)](projection-transform.md).

 

Os tópicos a seguir apresentam a neblina e apresentam informações sobre como usar vários recursos de neblina em aplicativos Direct3D.

-   [Fórmulas de neblina (Direct3D 9)](fog-formulas.md)
-   [Parâmetros de neblina (Direct3D 9)](fog-parameters.md)
-   [Fusão de neblina (Direct3D 9)](fog-blending.md)
-   [Cor da neblina (Direct3D 9)](fog-color.md)
-   [Neblina de vértice (Direct3D 9)](vertex-fog.md)
-   [Sombra de pixel (Direct3D 9)](pixel-fog.md)

A fusão de neblina é controlada por Estados de renderização; Ele não faz parte do pipeline de pixel programável.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de Direct3D](direct3d-rendering.md)
</dt> </dl>

 

 



