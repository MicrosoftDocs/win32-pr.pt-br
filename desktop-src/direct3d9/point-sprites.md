---
description: O suporte para sprites de ponto no Direct3D 9 permite a renderização de alto desempenho de pontos (sistemas de partículas). Os sprites de ponto são generalizações de pontos genéricos que permitem renderizar formas arbitrárias conforme definido por texturas.
ms.assetid: a9046c7e-779c-4f33-b8ff-f189da3dcfc5
title: Sprites de ponto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90abd21207d9b3866ff93bd6c73069b655056f1c28811689762b0ce669183793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520459"
---
# <a name="point-sprites-direct3d-9"></a>Sprites de ponto (Direct3D 9)

O suporte para sprites de ponto no Direct3D 9 permite a renderização de alto desempenho de pontos (sistemas de partículas). Os sprites de ponto são generalizações de pontos genéricos que permitem renderizar formas arbitrárias conforme definido por texturas.

-   [Controles de renderização primitivos de ponto](#point-primitive-rendering-controls)
-   [Cálculos de tamanho de ponto](#point-size-computations)
-   [Renderização de ponto](#point-rendering)

## <a name="point-primitive-rendering-controls"></a>Controles de renderização primitivos de ponto

O Direct3D 9 dá suporte a parâmetros adicionais para controlar a renderização de sprites de ponto (primitivos de ponto). Esses parâmetros permitem que os pontos sejam de tamanho variável e tenham um mapa de textura completo aplicado. O tamanho de cada ponto é determinado por um tamanho especificado pelo aplicativo combinado com uma função baseada em distância computada pelo Direct3D. O aplicativo pode especificar o tamanho do ponto por vértice ou definindo D3DRS POINTSIZE, que se aplica a pontos sem um tamanho por \_ vértice. O tamanho do ponto é expresso em unidades de espaço da câmera, com exceção de quando o aplicativo está passando vértices FVF (formato de vértice flexível) pós-transformados. Nesse caso, a função baseada em distância não é aplicada e o tamanho do ponto é expresso em unidades de pixels no destino de renderização.

As coordenadas de textura computadas e usadas quando os pontos de renderização dependem da configuração de D3DRS \_ POINTSPRIABLE. Quando esse valor é definido como **TRUE,** as coordenadas de textura são definidas para que cada ponto exibe a textura completa. Em geral, isso só é útil quando os pontos são significativamente maiores que um pixel. Quando D3DRS POINTSPRIABLE é definido como FALSE, a coordenada de textura de vértice de cada \_ ponto é usada para todo o ponto. 

## <a name="point-size-computations"></a>Cálculos de tamanho de ponto

O tamanho do ponto é determinado por D3DRS \_ POINTSCALEENABLE. Se esse valor for definido como **FALSE,** o tamanho do ponto especificado pelo aplicativo será usado como o tamanho do espaço na tela (pós-transformado). Os vértices passados para Direct3D no espaço na tela não têm tamanhos de ponto computados; o tamanho do ponto especificado é interpretado como tamanho de espaço na tela.

Se D3DRS \_ POINTSCALEENABLE for **TRUE,** o Direct3D calculará o tamanho do ponto de espaço na tela de acordo com a fórmula a seguir. O tamanho do ponto especificado pelo aplicativo é expresso em unidades de espaço da câmera.

S = Vh \* S <sub>i</sub> \* sqrt(1/(A + B \* D + C ( D Meio \* )))

Nesta fórmula, o tamanho do ponto de entrada, S <sub>i</sub>, é por vértice ou o valor do estado de renderização D3DRS \_ POINTSIZE. Os fatores de escala de ponto, D3DRS \_ POINTSCALE \_ A, D3DRS POINTSCALE B e \_ \_ D3DRS \_ POINTSCALE C, são representados pelos pontos \_ A, B e C. A altura do viewport, V h, é o membro Altura da estrutura [**D3DVIEWPORT9**](d3dviewport9.md) que representa o viewport. D , a distância do olho até a posição (o olho na origem) é calculada pela posição do espaço ocular do ponto (X, Y, Z) e executando a operação a seguir.

D = sqrt (XÁ + Y Trimestre + Z 2)

O tamanho máximo do ponto, Pm, é determinado com o menor do membro MaxPointSize da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) ou do estado de renderização D3DRS \_ POINTSIZE \_ MAX. O tamanho mínimo do ponto, P<sub>min,</sub>é determinado consultando o valor de D3DRS \_ POINTSIZE \_ MIN. Portanto, o tamanho final do ponto de espaço na tela, S, é determinado da seguinte maneira.

-   Se ss > Pm, então S = P m
-   se S < P<sub>min,</sub>em seguida, S = P <sub>min</sub>
-   Caso contrário, S = S s

## <a name="point-rendering"></a>Renderização de ponto

Um ponto de espaço na tela, P = ( X, Y, Z, W), do tamanho do espaço na tela S é rasterizado como um telão dos quatro vértices a seguir.

(( X + S/2, Y + S/2, Z, W), ( X + S/2, Y - S/2, Z, W), ( X - S/2, Y- S/2, Z, W), ( X - S/2, Y + S/2, Z, W))

Os atributos de cor do vértice são duplicados em cada vértice; portanto, cada ponto é sempre renderizado com cores constantes.

A atribuição de índices de textura é controlada pela configuração de estado de renderização D3DRS \_ POINTSPRIABLEABLE. Se D3DRS POINTSPRIABLE for definido como FALSE, as coordenadas de textura de \_ vértice serão duplicadas em cada vértice.  Se D3DRS POINTSPRIABLE for definido como TRUE, as coordenadas de textura nos quatro \_ vértices serão definidas com os valores a seguir. 

(0.F, 0.F), (0.F, 1.F), (1.F, 0.F), (1.F, 1.F)

Isso é mostrado no diagrama a seguir.

![diagrama de um quadrado com vértices rotulados para valores de coordenadas (u,v) e (x,y)](images/spritepoint.png)

Quando o recorte está habilitado, os pontos são recortados da seguinte maneira. Se o vértice exceder o intervalo de valores de profundidade – MinZ e MaxZ da estrutura [**D3DVIEWPORT9**](d3dviewport9.md) – na qual uma cena deve ser renderizada, o ponto existe fora da exibição e não é renderizado. Se o ponto, levando em conta o tamanho do ponto, estiver completamente fora do viewport em X e Y, o ponto não será renderizado; os pontos restantes são renderizados. É possível que a posição do ponto esteja fora do viewport em X ou Y e ainda esteja parcialmente visível.

Os pontos podem ou não ser recortados corretamente em planos de clipe definidos pelo usuário. Se D3DPMISCCAPS CLIPPLANESCALEDPOINTS não estiver definido no membro \_ PrimitiveMiscCaps da estrutura [**D3DCAPS9,**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) os pontos serão recortados para planos de clipe definidos pelo usuário com base apenas na posição do vértice, ignorando o tamanho do ponto. Nesse caso, os pontos dimensionados são totalmente renderizados quando a posição do vértice está dentro dos planos de clipe e descartados quando a posição do vértice está fora de um plano de clipe. Os aplicativos podem impedir possíveis artefatos adicionando uma geometria de borda aos planos de corte tão grandes quanto o tamanho máximo do ponto.

Se o bit D3DPMISCCAPS CLIPPLANESCALEDPOINTS estiver definido, os pontos dimensionados serão recortados corretamente em planos de \_ clipe definidos pelo usuário.

O processamento de vértice de hardware pode ou não dar suporte ao tamanho do ponto. Por exemplo, se um dispositivo for criado com D3DCREATE HARDWARE VERTEXPROCESSING em um dispositivo de CAMADA de abstração de \_ \_ hardware (HAL) (D3DDEVTYPE HAL) que tenha o membro MaxPointSize da estrutura \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) definido como 1.0 ou 0,0, todos os pontos serão um único pixel. Para renderizar sprites de ponto de pixel menores que 1,0, você deve usar vértices TL de FVF (transformados e acesos) ou processamento de vértices de software (D3DCREATE SOFTWARE VERTEXPROCESSING), nesse caso, o tempo de run \_ time direct3D emula a renderização de sprite de \_ ponto.

Um dispositivo de hardware que faz processamento de vértice e dá suporte a sprites de ponto – MaxPointSize definido como maior que 1,0f – é necessário para executar a computação de tamanho para sprites não formados e é necessário para definir corretamente o vértice por vértice ou D3DRS \_ POINTSIZED3DRS POINTSIZE para \_ vértices TL.

Para obter informações sobre regras de renderização para pontos, linhas e triângulos, consulte [Regras de rasterização (Direct3D 9)](rasterization-rules.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de vértice](vertex-pipeline.md)
</dt> </dl>

 

 



