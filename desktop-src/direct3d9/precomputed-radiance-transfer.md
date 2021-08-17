---
description: Transferência radiante de computação (Direct3D 9)
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: Transferência radiante de computação (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc18eff66dab9a696a3e441d894a327890c53888da008d72a5f143ca0d345a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798683"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a>Transferência radiante de computação (Direct3D 9)

## <a name="using-precomputed-radiance-transfer"></a>Usando a transferência radiante precomputada

Há várias formas de complexidade presentes em cenas interessantes, incluindo como o ambiente de iluminação é modelado (ou seja, modelos de iluminação de área versus pontos/direcionais) e que tipo de efeitos globais são modelados (por exemplo, sombras, interflexões, dispersão de subsuperfície). As técnicas tradicionais de renderização interativa modelam um valor limitado dessa complexidade. O PRT habilita esses efeitos com algumas restrições significativas:

-   Os objetos são considerados rígidos (ou seja, sem deformações).
-   É uma abordagem centrada no objeto (a menos que os objetos sejam movidos juntos, esses efeitos globais não são mantidos entre eles).
-   Apenas iluminação de baixa frequência é modelada (resultando em sombras suaves). Para luzes de alta frequência (sombras nítidas), as técnicas tradicionais teriam de ser empregadas.

O PRT requer um dos seguintes, mas não ambos:

-   modelos altamente mosaico e vs \_ 1 \_
-   PS \_ 2 \_ 0

### <a name="standard-diffuse-lighting-versus-prt"></a>Iluminação difusa padrão versus PRT

A ilustração a seguir é renderizada usando o modelo de iluminação tradicional (n · l). As sombras nítidas poderiam ser habilitadas usando outra passagem e alguma forma de técnica de sombreamento (mapas de profundidade de sombra ou volumes de sombra). A adição de várias luzes exigiria várias passagens (se as sombras fossem usadas) ou sombreadores mais complexos com técnicas tradicionais.

![captura de tela de uma ilustração renderizada usando o modelo de iluminação tradicional](images/prt-diffuse-cropped.png)

A próxima ilustração é renderizada com PRT usando a melhor aproximação de uma única luz direcional que ele pode resolver. Isso resulta em sombras suaves que seriam difíceis de produzir com técnicas tradicionais. Como o PRT sempre modela os ambientes completos de iluminação adicionando várias luzes ou usando um mapa de ambiente, você só alteraria os valores (mas não o número) de constantes usadas pelo sombreador.

![captura de tela de uma ilustração renderizada usando PRT](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a>PRT com interflexões

A iluminação direta atinge a superfície diretamente da luz. As interflexões estão se esgotando na superfície após o encerramento de alguma outra superfície, certo número de vezes. O PRT pode modelar esse comportamento sem alterar o desempenho em tempo de execução simplesmente executando o simulador com parâmetros diferentes.

A ilustração a seguir é criada usando somente o PRT direto (0 salta sem interflexões).

![captura de tela de uma ilustração renderizada usando somente o PRT direto](images/prt-nointerreflections.png)

A ilustração a seguir é criada usando o PRT com interflexões (2 salta com interflexões).

![captura de tela de uma ilustração renderizada usando o PRT com interflexões](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a>PRT com dispersão de subsuperfície

A dispersão de subsuperfície é uma técnica que modela como a luz passa por determinados materiais. Por exemplo, pressione uma lanterna acesa em relação ao Palm de sua mão. A luz da lanterna passa por sua mão, salta (alterando a cor do processo) e sai do outro lado de sua mão. Isso também pode ser modelado com alterações simples no simulador e nenhuma alteração no tempo de execução.

A ilustração a seguir demonstra o PRT com dispersão de subsuperfície.

![captura de tela de uma ilustração renderizada usando o PRT com dispersão de subsuperfície](images/prt-subsurface.png)

## <a name="how-prt-works"></a>Como o PRT funciona

Os termos a seguir são úteis para entender como o PRT funciona, conforme ilustrado no diagrama a seguir.

Radiante de origem: o radiante de origem representa o ambiente de iluminação como um todo. No PRT, um ambiente arbitrário é aproximado usando a base harmônica esférica – essa iluminação é considerada distante em relação ao objeto (a mesma suposição feita com mapas de ambiente).

Saia de radiante: Exit radiante é a luz saindo de um ponto na superfície de qualquer fonte possível (refletida radiante, dispersão de subsuperfície, emissão).

Vetores de transferência: os vetores de transferência mapeiam a origem radiante para Exit radiante e são preputados offline usando uma simulação de transporte leve complexa.

![diagrama de como o PRT funciona](images/prt-lightingpicture.png)

O PRT considera o processo de renderização em dois estágios, conforme mostrado no diagrama a seguir:

1.  Uma simulação cara de transporte leve computa os coeficientes de transferência que podem ser usados em tempo de execução.
2.  Um estágio de tempo de execução relativamente simples aproxima primeiro o ambiente de iluminação usando a base harmônica esférica, em seguida, usa esses coeficientes de iluminação e os coeficientes de transferência pré-computados (do estágio 1) com um sombreador simples, resultando na saída de radiante (a luz deixando o objeto).

![diagrama de fluxo de dados de PRT](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a>Como usar a API PRT

1.  Compute os vetores de transferência com um dos cálculos... métodos de [**ID3DXPRTEngine**](id3dxprtengine.md).

    Lidar diretamente com esses vetores de transferência requer uma quantidade significativa de memória e computação de sombreador. A compactação reduz significativamente a quantidade de memória e a computação do sombreador necessários.

    Os valores de iluminação final são calculados em um sombreador de vértice que implementa a seguinte equação de renderização compactada.

    ![equação de renderização de PRT](images/prt-shaderequation.png)

    Em que:

    

    | Parâmetro      | Descrição                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | RP             | Um único canal de saída radiante no vértice p e é avaliado em cada vértice na malha.                     |
    | MK             | A média do cluster k. Este é um vetor de ordem ² de coeficientes.                                               |
    | k              | A ID do cluster para o vértice p.                                                                                    |
    | L<sup>'</sup>  | A aproximação do radiante de origem nas funções de base SH. Este é um vetor de ordem ² de coeficientes. |
    | j              | Um inteiro que soma o número de vetores do PCA.                                                            |
    | w<sub>PJ</sub> | O peso do PCA jth para o ponto p. Esse é um único coeficiente.                                                   |
    | B<sub>KJ</sub> | O vetor de base do PCA do jth para o cluster k. Este é um vetor de ordem ² de coeficientes.                               |

    

     

    A extração... os métodos de [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) fornecem acesso a dados compactados da simulação.

2.  Compute a origem radiante.

    Há várias funções auxiliares na API para lidar com uma variedade de cenários de iluminação comuns.

    

    | Função                                                         | Finalidade                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [**D3DXSHEvalDirectionalLight**](d3dxshevaldirectionallight.md) | Aproxima uma luz direcional convencional.                                                              |
    | [**D3DXSHEvalSphericalLight**](d3dxshevalsphericallight.md)     | Aproxima fontes de luz esférica local. (Observe que o PRT só funciona com ambientes de iluminação de distância.) |
    | [**D3DXSHEvalConeLight**](d3dxshevalconelight.md)               | Aproxima uma fonte de luz de área distante. Um exemplo seria o sol (ângulo de cone muito pequeno).              |
    | [**D3DXSHEvalHemisphereLight**](d3dxshevalhemispherelight.md)   | Avalia uma luz que é uma interpolação linear entre duas cores (uma em cada pólo de uma esfera).         |

    

     

3.  Compute o radiante de saída.

    A equação 1 agora precisa ser avaliada em todos os pontos usando um vértice ou um sombreador de pixel. Antes que o sombreador possa ser avaliado, as constantes devem ser computadas e carregadas na tabela de constantes (consulte a [amostra de demonstração de PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) para obter detalhes). O próprio sombreador é uma implementação simples desta equação.

    ```
    struct VS_OUTPUT
    {
        float4 Position   : POSITION;   // vertex position 
        float2 TextureUV  : TEXCOORD0;  // vertex texture coordinates 
        float4 Diffuse    : COLOR0;     // vertex diffuse color
    };

    VS_OUTPUT Output;   
    Output.Position = mul(vPos, mWorldViewProjection);

    float4 vExitR = float4(0,0,0,0);
    float4 vExitG = float4(0,0,0,0);
    float4 vExitB = float4(0,0,0,0);
        
    for (int i=0; i < (NUM_PCA_VECTORS/4); i++) 
    {
       vExitR += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*0];
       vExitG += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*1];
       vExitB += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*2];
    }
       
    float4 vExitRadiance = vClusteredPCA[iClusterOffset];
    vExitRadiance.r += dot(vExitR,1);
    vExitRadiance.g += dot(vExitG,1);
    vExitRadiance.b += dot(vExitB,1);

    Output.Diffuse = vExitRadiance;
    ```

    

## <a name="references"></a>Referências

Para obter mais informações sobre PRT e harmônicas esféricos, consulte os seguintes documentos:


```
Precomputed Radiance Transfer for Real-Time Rendering in Dynamic, 
Low-Frequency Lighting Environments 
P.-P. Sloan, J. Kautz, J. Snyder
SIGGRAPH 2002 

Clustered Principal Components for Precomputed Radiance Transfer 
P.-P. Sloan, J. Hall, J. Hart, J. Snyder 
SIGGRAPH 2003 

Efficient Evaluation of Irradiance Environment Maps 
P.-P. Sloan 
ShaderX 2,  W. Engel 

Spherical Harmonic Lighting: The Gritty Details 
R. Green 
GDC 2003 

An Efficient Representation for Irradiance Environment Maps 
R. Ramamoorthi, P. Hanrahan 

A Practical Model for Subsurface Light Transport 
H. W. Jensen, S. R. Marschner, M. Levoy, and P. Hanrahan 
SIGGRAPH 2001 

Bi-Scale Radiance Transfer 
P.-P. Sloan, X. Liu, H.-Y. Shum, J. Snyder
SIGGRAPH 2003 

Fast, Arbitrary BRDF Shading for Low-Frequency Lighting Using Spherical 
Harmonics 
J. Kautz, P.-P. Sloan, J. Snyder
12th Eurographics Workshop on Rendering 

Precomputing Interactive Dynamic Deformable Scenes 
D. James, K. Fatahalian 
SIGGRAPH 2003 

All-Frequency Shadows Using Non-linear Wavelet Lighting Approximation 
R. Ng, R. Ramamoorth, P. Hanrahan 
SIGGRAPH 2003 

Matrix Radiance Transfer 
J. Lehtinen, J. Kautz
SIGGRAPH 2003 

Math World 
E. W. Weisstein, Wolfram Research, Inc. 

Quantum Theory of Angular Momentum 
D. A. Varshalovich, A.N. Moskalev, V.K. Khersonskii 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos avançados](advanced-topics.md)
</dt> <dt>

[Equações de PRT (Direct3D 9)](prt-equations.md)
</dt> <dt>

[Representando o PRT com texturas (Direct3D 9)](representing-prt-with-textures.md)
</dt> <dt>

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> <dt>

[**ID3DXPRTEngine**](id3dxprtengine.md)
</dt> <dt>

[**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md)
</dt> <dt>

[Funções de transferência de Radiance pré-comutadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 



