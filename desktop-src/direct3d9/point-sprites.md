---
description: O suporte para sprites de ponto no Direct3D 9 permite a renderização de pontos de alto desempenho (sistemas de partículas). Os sprites de ponto são generalizações de pontos genéricos que permitem que formas arbitrárias sejam renderizadas conforme definido por texturas.
ms.assetid: a9046c7e-779c-4f33-b8ff-f189da3dcfc5
title: Sprites de ponto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c988a104eb65b5e2d7e56ff2444e8d422c422df2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500464"
---
# <a name="point-sprites-direct3d-9"></a>Sprites de ponto (Direct3D 9)

O suporte para sprites de ponto no Direct3D 9 permite a renderização de pontos de alto desempenho (sistemas de partículas). Os sprites de ponto são generalizações de pontos genéricos que permitem que formas arbitrárias sejam renderizadas conforme definido por texturas.

-   [Controles de renderização de ponto primitivo](#point-primitive-rendering-controls)
-   [Cálculos de tamanho de ponto](#point-size-computations)
-   [Renderização de ponto](#point-rendering)

## <a name="point-primitive-rendering-controls"></a>Controles de renderização de ponto primitivo

O Direct3D 9 dá suporte a parâmetros adicionais para controlar a renderização de sprites de ponto (primitivos de ponto). Esses parâmetros permitem que os pontos sejam do tamanho da variável e tenham um mapa de textura completo aplicado. O tamanho de cada ponto é determinado por um tamanho especificado pelo aplicativo, combinado com uma função baseada em distância calculada pelo Direct3D. O aplicativo pode especificar um tamanho de ponto como por vértice ou definindo D3DRS \_ Points, que se aplica a pontos sem um tamanho por vértice. O tamanho do ponto é expresso em unidades de espaço da câmera, com exceção de quando o aplicativo está passando vértices de FVF (formato de vértice flexível) após a transformação. Nesse caso, a função baseada em distância não é aplicada e o tamanho do ponto é expresso em unidades de pixels no destino de renderização.

As coordenadas de textura computadas e usadas quando os pontos de renderização dependem da configuração de D3DRS \_ POINTSPRITEENABLE. Quando esse valor é definido como **true**, as coordenadas de textura são definidas para que cada ponto exiba a textura completa. Em geral, isso só é útil quando os pontos são significativamente maiores que um pixel. Quando D3DRS \_ POINTSPRITEENABLE é definido como **false**, a coordenada de textura do vértice de cada ponto é usada para todo o ponto.

## <a name="point-size-computations"></a>Cálculos de tamanho de ponto

O tamanho do ponto é determinado por D3DRS \_ POINTSCALEENABLE. Se esse valor for definido como **false**, o tamanho do ponto especificado pelo aplicativo será usado como o tamanho do espaço da tela (após a transformação). Os vértices passados para o Direct3D no espaço da tela não têm tamanhos de ponto calculados; o tamanho do ponto especificado é interpretado como tamanho do espaço de tela.

Se D3DRS \_ POINTSCALEENABLE for **true**, o Direct3D calculará o tamanho do ponto de espaço de tela de acordo com a fórmula a seguir. O tamanho do ponto especificado pelo aplicativo é expresso em unidades de espaço da câmera.

S s = VH \* s <sub></sub> \* sqrt (1/B \* D ₑ + C \* (D ₑ ²)))

Nessa fórmula, o tamanho do ponto de entrada, S <sub>i</sub>, é por vértice ou o valor de D3DRS pontos de \_ processamento. Os fatores de escala de pontos, D3DRS \_ POINTSCALE \_ A, D3DRS \_ POINTSCALE \_ B e D3DRS \_ POINTSCALE \_ C, são representados pelos pontos a, B e c. A altura do visor, V h, é o membro de altura da estrutura [**D3DVIEWPORT9**](d3dviewport9.md) que representa o visor. D ₑ, a distância do olho até a posição (o olho na origem), é calculada por meio da posição do espaço de olho do ponto (X ₑ, Y ₑ, Z ₑ) e da execução da operação a seguir.

D ₑ = sqrt (X ₑ ² + Y ₑ ² + Z ₑ ²)

O tamanho máximo do ponto, PM ₐ ₓ, é determinado com o menor valor do membro MaxPointSize da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) ou o \_ estado máximo de processamento de D3DRS de pontos de extremidade \_ . O tamanho mínimo do ponto, P<sub>min</sub>, é determinado pela consulta do valor de D3DRS \_ pointse \_ min. Portanto, o tamanho do ponto de espaço da tela final, S, é determinado da seguinte maneira.

-   Se SS > PM ₐ ₓ, então S = P m ₐ ₓ
-   se S < P<sub>min</sub>, s = P <sub>min</sub>
-   Caso contrário, S = S s

## <a name="point-rendering"></a>Renderização de ponto

Um ponto de espaço na tela, P = (X, Y, Z, W), do tamanho do espaço de tela S é rasterizado como um diamante dos quatro vértices a seguir.

(X + S/2, Y + S/2, Z, W), (X + S/2, Y-S/2, Z, W), (X-S/2, Y-S/2, Z, W), (X-S/2, Y + S/2, Z, W))

Os atributos de cor do vértice são duplicados em cada vértice; Portanto, cada ponto sempre é renderizado com cores constantes.

A atribuição de índices de textura é controlada pela \_ configuração do estado de RENDERIZAÇÃO D3DRS POINTSPRITEENABLE. Se D3DRS \_ POINTSPRITEENABLE for definido como **false**, as coordenadas de textura de vértice serão duplicadas em cada vértice. Se D3DRS \_ POINTSPRITEENABLE for definido como **true**, as coordenadas de textura nos quatro vértices serão definidas com os valores a seguir.

(0. F, 0. F), (0. F, 1. F), (1. F, 0. F), (1. F, 1. F)

Isso é mostrado no diagrama a seguir.

![diagrama de um quadrado com vértices rotulados para valores de coordenadas (u, v) e (x, y)](images/spritepoint.png)

Quando o recorte está habilitado, os pontos são recortados da maneira a seguir. Se o vértice exceder o intervalo de valores de profundidade – MinZ e MaxZ da estrutura [**D3DVIEWPORT9**](d3dviewport9.md) – no qual uma cena deve ser renderizada, o ponto existirá fora da exibição frustum e não será renderizado. Se o ponto, levando em conta o tamanho do ponto, estiver completamente fora do visor em X e Y, o ponto não será renderizado; os pontos restantes são renderizados. É possível que a posição do ponto esteja fora do visor em X ou Y e ainda esteja parcialmente visível.

Os pontos podem ou não ser corretamente recortados em planos de clipes definidos pelo usuário. Se D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS não estiver definido no membro PrimitiveMiscCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) , os pontos serão recortados para os planos de clipes definidos pelo usuário com base apenas na posição do vértice, ignorando o tamanho do ponto. Nesse caso, os pontos dimensionados são totalmente renderizados quando a posição do vértice está dentro dos planos de corte e descartados quando a posição do vértice está fora de um plano de corte. Os aplicativos podem impedir possíveis artefatos adicionando uma geometria de borda a planos de clipes que seja tão grande quanto o tamanho máximo do ponto.

Se o \_ bit D3DPMISCCAPS CLIPPLANESCALEDPOINTS for definido, os pontos dimensionados serão recortados corretamente em planos de clipe definidos pelo usuário.

O processamento de vértices de hardware pode ou não dar suporte ao tamanho do ponto. Por exemplo, se um dispositivo for criado com D3DCREATE de \_ hardware \_ VERTEXPROCESSING em um dispositivo HAL (camada de abstração de hardware) ( \_ Hal D3DDEVTYPE) que tenha o membro MaxPointSize da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) definido como 1,0 ou 0,0, todos os pontos serão um único pixel. Para renderizar sprites de ponto de pixel menor que 1,0, você deve usar vértices FVF TL (transformados e iluminados) ou o processamento de vértice de software (D3DCREATE \_ software \_ VERTEXPROCESSING). nesse caso, o tempo de execução do Direct3D emula a renderização de Sprite de ponto.

Um dispositivo de hardware que faz o processamento de vértices e dá suporte a Point sprites-MaxPointSize definido como maior que 1,0 f-é necessário para executar a computação de tamanho para sprites não transformados e é necessário para definir corretamente os vértices por vértice ou D3DRS \_ POINTSIZED3DRS \_ para os cantos de TL.

Para obter informações sobre regras de renderização para pontos, linhas e triângulos, consulte [regras de rasterização (Direct3D 9)](rasterization-rules.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de vértice](vertex-pipeline.md)
</dt> </dl>

 

 



