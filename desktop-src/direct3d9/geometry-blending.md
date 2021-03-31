---
description: O Direct3D permite que um aplicativo aumente o realm de seus bastidores ao renderizar objetos Polygons segmentados – especialmente caracteres-que têm junções mescladas suavemente.
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: Combinação de geometria (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19daa40f7d7d8193ae486640bc613dd7a666ec7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645620"
---
# <a name="geometry-blending-direct3d-9"></a>Combinação de geometria (Direct3D 9)

O Direct3D permite que um aplicativo aumente o realm de seus bastidores ao renderizar objetos Polygons segmentados – especialmente caracteres-que têm junções mescladas suavemente. Esses efeitos são geralmente chamados de aparência. O sistema alcança esse efeito aplicando matrizes de transformação mundiais adicionais a um único conjunto de vértices para criar vários resultados e, em seguida, executar uma combinação linear entre os vértices resultantes para criar um único conjunto de geometria para renderização. A ilustração a seguir de um banana mostra esse processo.

![ilustração do processo para misturar dois objetos com a textura banana](images/geometry-blend.png)

A ilustração anterior mostra como você pode imaginar o processo de mesclagem de geometria. Em uma única chamada de renderização, o sistema usa os vértices para o banana, transforma-os duas vezes uma vez sem modificação e uma vez com uma rotação simples e mistura os resultados para criar um banana torto. O sistema mescla a posição do vértice, bem como o vértice normal quando a iluminação está habilitada. Os aplicativos não estão limitados a dois caminhos de mesclagem; O Direct3D pode misturar geometria entre até quatro matrizes mundiais, incluindo a matriz mundial padrão, [**D3DTS \_ World**](d3dts-world.md).

> [!Note]
>
> Quando a iluminação está habilitada, os Normals de vértice são transformados por uma matriz inversa de exibição mundial correspondente, ponderada da mesma maneira que os cálculos de posição de vértice. O sistema normaliza o vetor normal resultante se o estado de \_ RENDERIZAÇÃO D3DRS NORMALIZENORMALS for definido como **true**.

 

Sem a combinação de geometria, os modelos articulados dinâmicos geralmente são renderizados em segmentos. Por exemplo, considere um modelo 3D do braço humano. Na exibição mais simples, um ARM tem duas partes: o braço superior que se conecta ao corpo e o braço inferior, que se conecta à mão. Os dois são conectados no cotovelo e o braço inferior gira nesse ponto. Um aplicativo que renderiza um ARM pode reter dados de vértice para o braço superior e inferior, cada um com uma matriz de transformação do mundo separada. O exemplo de código a seguir ilustra isso.


```
typedef struct _Arm
{
    VERTEX upper_arm_verts[200];
    D3DMATRIX matWorld_Upper;

    VERTEX lower_arm_verts[200];
    D3DMATRIX matWorld_Lower;
} ARM, *LPARM;

ARM MyArm; // This needs to be initialized.
```



Para renderizar o ARM, são feitas duas chamadas de renderização, conforme mostrado no código a seguir.


```
// Render the upper arm.
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Upper );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );

// Render the lower arm, updating its world matrix to articulate
// the arm by pi/4 radians (45 degrees) at the elbow.
MyArm.matWorld_Lower = RotateMyArm(MyArm.matWorld, pi/4);
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Lower );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );
```



A ilustração a seguir é um banana, modificado para usar essa técnica.

![ilustração de um banana combinado sem mesclagem de geometria](images/noblend.png)

As diferenças entre a geometria combinada e a geometria não misturada são óbvias. Este exemplo é um pouco extremo. Em um aplicativo do mundo real, as junções de modelos segmentados são projetadas para que as emendas não sejam tão óbvias. No entanto, as emendas são visíveis às vezes, o que apresenta desafios constantes para designers de modelos.

A combinação de geometria no Direct3D apresenta uma alternativa ao cenário de modelagem segmentada clássica. No entanto, a melhor qualidade visual dos objetos segmentados é o custo dos cálculos de mesclagem durante a renderização. Para minimizar o impacto dessas operações adicionais, o pipeline do Direct3D Geometry é otimizado para misturar geometria com a menor sobrecarga possível. Os aplicativos que usam de forma inteligente os serviços de combinação de geometria oferecidos pelo Direct3D podem melhorar o realm de seus caracteres e, ao mesmo tempo, evitar repercussões de desempenho graves.

## <a name="blending-transform-and-render-states"></a>Mesclando Estados de transformação e de renderização

O método [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) reconhece as macros do [**D3DTS \_ World**](d3dts-world.md) e do [**D3DTS \_ worldn**](d3dts-worldn.md) , que correspondem aos valores que podem ser definidos pela macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) . Essas macros são usadas para identificar as matrizes entre as quais a geometria será mesclada.

O tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) inclui o \_ estado de renderização D3DRS VERTEXBLEND para habilitar e controlar a combinação de geometria. Os valores válidos para esse estado de renderização são definidos pelo tipo enumerado [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . Se a combinação de geometria estiver habilitada, o formato de vértice deverá incluir o número apropriado de pesos de mesclagem.

## <a name="blending-weights"></a>Pesos de mesclagem

Um peso de mesclagem, às vezes chamado de peso beta, controla a extensão até a qual uma determinada matriz do mundo afeta um vértice. Os pesos de mesclagem são valores de ponto flutuante que variam de 0,0 a 1,0, codificados no formato de vértice, em que um valor de 0,0 significa que o vértice não é mesclado com essa matriz e 1,0 significa que o vértice é afetado de forma completa pela matriz.

Os pesos de mesclagem de geometria são codificados no formato de vértice, aparecendo imediatamente após a posição de cada vértice, conforme descrito em [códigos de FVF de função fixas (Direct3D 9)](fixed-function-fvf-codes.md). Você comunica o número de pesos de mesclagem no formato de vértice, incluindo uma das [constantes FVF](d3dfvf.md) na descrição de vértice que você fornece aos métodos de renderização.

O sistema executa uma combinação linear entre os resultados ponderados das matrizes de mistura. A equação a seguir é a fórmula de mesclagem completa.

![equação de mesclagem linear, usando matrizes de transformação mundiais](images/vert-blend-formula.png)

Na equação anterior, vBlend é o vértice de saída, os elementos v são os vértices produzidos pela matriz mundial aplicada ([**D3DTS \_ worldn**](d3dts-worldn.md)). Os elementos W são os valores de peso correspondentes dentro do formato de vértice. Um vértice misturado entre as matrizes n pode ter-1 valores de peso de mesclagem, um para cada matriz de mesclagem, exceto o último. O sistema gera automaticamente o peso para a última matriz mundial para que a soma de todos os pesos seja 1,0, expressa na notação Sigma aqui. Essa fórmula pode ser simplificada para cada um dos casos com suporte do Direct3D, que é mostrado nas equações a seguir.

![equações de mesclagem linear para três casos de mesclagem](images/vert-blend-formulas-simple.png)

Essas são as formas simplificadas da fórmula de mesclagem completa para os dois, três e quatro casos de matriz de mistura.

> [!Note]  
> Embora o Direct3D inclua descritores de FVF para definir vértices que contêm até cinco pesos de mesclagem, somente três podem ser usados nesta versão do DirectX.

 

Informações adicionais estão contidas nos tópicos a seguir.

-   [Usando a combinação de geometria (Direct3D 9)](using-geometry-blending.md)
-   [Mistura de vértices indexados (Direct3D 9)](indexed-vertex-blending.md)
-   [Interpolação de vértice (Direct3D 9)](vertex-tweening.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de vértice](vertex-pipeline.md)
</dt> </dl>

 

 
