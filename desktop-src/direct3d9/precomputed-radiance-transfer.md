---
description: Transferência de Radiance pré-comutada (Direct3D 9)
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: Transferência de Radiance pré-comutada (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc18eff66dab9a696a3e441d894a327890c53888da008d72a5f143ca0d345a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798683"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a>Transferência de Radiance pré-comutada (Direct3D 9)

## <a name="using-precomputed-radiance-transfer"></a>Usando a transferência de radiance pré-comutada

Há várias formas de complexidade presentes em cenas interessantes, incluindo como o ambiente de iluminação é modelado (ou seja, modelos de iluminação de área versus pontos/direcionais) e que tipo de efeitos globais são modelados (por exemplo, sombras, interrefleções, dispersão de subsuperfiguração).) Técnicas de renderização interativa tradicionais modelam uma quantidade limitada dessa complexidade. O PRT habilita esses efeitos com algumas restrições significativas:

-   Supõe-se que os objetos sejam rígidos (ou seja, sem deformações).
-   É uma abordagem centrada em objeto (a menos que os objetos sejam movidos juntos, esses efeitos globais não são mantidos entre eles).
-   Somente a iluminação de baixa frequência é modelada (resultando em sombras suaves.) Para luzes de alta frequência (sombras fortes), técnicas tradicionais teriam que ser empregadas.

O PRT requer um dos seguintes, mas não ambos:

-   modelos altamente mosaico e vs \_ 1 \_ 1
-   ps \_ 2 \_ 0

### <a name="standard-diffuse-lighting-versus-prt"></a>Iluminação difusa padrão versus PRT

A ilustração a seguir é renderizada usando o modelo de iluminação tradicional (n · l). Sombras fortes podem ser habilitadas usando outra passagem e alguma forma de técnica de sombreamento (mapas de profundidade de sombra ou volumes de sombra). Adicionar várias luzes exigiria várias passagens (se sombras devem ser usadas) ou sombreadores mais complexos com técnicas tradicionais.

![captura de tela de uma ilustração renderizada usando o modelo de iluminação tradicional](images/prt-diffuse-cropped.png)

A próxima ilustração é renderizada com PRT usando a melhor aproximação de uma única luz direcional que ele pode resolver. Isso resulta em sombras suaves que seriam difíceis de produzir com técnicas tradicionais. Como o PRT sempre modela ambientes de iluminação completos adicionando várias luzes ou usando um mapa de ambiente, você só alteraria os valores (mas não o número) de constantes usadas pelo sombreador.

![captura de tela de uma ilustração renderizada usando prt](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a>PRT com Interreflections

A iluminação direta atinge a superfície diretamente da luz. As interrefleções são luz que atinge a superfície depois de saltar de alguma outra superfície algumas vezes. O PRT pode modelar esse comportamento sem alterar o desempenho em tempo de execução simplesmente executando o simulador com parâmetros diferentes.

A ilustração a seguir é criada usando apenas PRT direto (0 ressalto sem interrefleções).

![captura de tela de uma ilustração renderizada usando apenas prt direto](images/prt-nointerreflections.png)

A ilustração a seguir é criada usando PRT com interrefleções (2 saltos com interrefleções).

![captura de tela de uma ilustração renderizada usando prt com interreflections](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a>PRT com dispersão de subsuficiência

O dispersão de sub-superfície é uma técnica que modela como a luz passa por determinados materiais. Por exemplo, pressione uma luz de luz sobre a mão. A luz da lâmpada passa pela mão, salta (alterando a cor no processo) e sai do outro lado da sua mão. Isso também pode ser modelado com alterações simples no simulador e sem alterações no runtime.

A ilustração a seguir demonstra PRT com dispersão de subsuficiência.

![captura de tela de uma ilustração renderizada usando prt com dispersão de sub-superfície](images/prt-subsurface.png)

## <a name="how-prt-works"></a>Como funciona o PRT

Os termos a seguir são úteis para entender como o PRT funciona, conforme ilustrado no diagrama a seguir.

Radiance de origem: o radiance de origem representa o ambiente de iluminação como um todo. No PRT, um ambiente arbitrário é aproximado usando a base alfabética esférica – essa iluminação é assumida como distante em relação ao objeto (a mesma suposição feita com mapas de ambiente.)

Sair do Radiance: sair do radiance é a luz que sai de um ponto na superfície de qualquer fonte possível (radiação refletida, dispersão de subsuperfiguração, emissão).

Vetores de Transferência: os vetores de transferência mapeiam o Radiance de Origem para o radiance de saída e são pré-computados offline usando uma simulação de transporte leve complexa.

![diagrama de como o prt funciona](images/prt-lightingpicture.png)

O PRT fatora o processo de renderização em dois estágios, conforme mostrado no diagrama a seguir:

1.  Uma simulação de transporte leve cara pré-comuta coeficientes de transferência que podem ser usados em tempo de operação.
2.  Um estágio de tempo de run time relativamente leve primeiro aproxima o ambiente de iluminação usando a base alfabética esférica e, em seguida, usa esses coeficientes de iluminação e os coeficientes de transferência pré-calculados (do estágio 1) com um sombreador simples, resultando em radiação de saída (a luz que sai do objeto).

![diagrama do fluxo de dados prt](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a>Como usar a API prt

1.  Compute os vetores de transferência com um dos dados de computação... métodos de [**ID3DXPRTEngine**](id3dxprtengine.md).

    Lidar diretamente com esses vetores de transferência requer uma quantidade significativa de memória e computação do sombreador. A compactação reduz significativamente a quantidade de memória e o cálculo do sombreador necessários.

    Os valores de iluminação finais são calculados em um sombreador de vértice que implementa a seguinte equação de renderização compactada.

    ![equação de renderização prt](images/prt-shaderequation.png)

    Em que:

    

    | Parâmetro      | Descrição                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | Rp             | Um único canal de radiação de saída no vértice p e é avaliado em cada vértice na malha.                     |
    | Mk             | A média do cluster k. Este é um vetor Orderâmico de coeficientes.                                               |
    | k              | A ID do cluster para vértice p.                                                                                    |
    | L<sup>'</sup>  | A aproximação da radiação de origem para as funções base sh. Este é um vetor Orderâmico de coeficientes. |
    | j              | Um inteiro que soma o número de vetores PCA.                                                            |
    | w<sub>pj</sub> | O peso da PCA jth para o ponto p. Esse é um coeficiente único.                                                   |
    | B<sub>kj</sub> | O vetor base da PCA jth para o cluster k. Este é um vetor Orderâmico de coeficientes.                               |

    

     

    A extração... os métodos de [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) fornecem acesso aos dados compactados da simulação.

2.  Compute o radiance de origem.

    Há várias funções auxiliares na API para lidar com uma variedade de cenários comuns de iluminação.

    

    | Função                                                         | Finalidade                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [**D3DXSHEvalDirectionalLight**](d3dxshevaldirectionallight.md) | Aproxima uma luz direcional convencional.                                                              |
    | [**D3DXSHEvalSphericalLight**](d3dxshevalsphericallight.md)     | Aproxima fontes de luz esféricas locais. (Observe que o PRT só funciona com ambientes de iluminação de distância.) |
    | [**D3DXSHEvalConeLight**](d3dxshevalconelight.md)               | Aproxima uma fonte de luz de área distante. Um exemplo seria o sol (ângulo de cone muito pequeno).              |
    | [**D3DXSHEvalHemisphereLight**](d3dxshevalhemispherelight.md)   | Avalia uma luz que é uma interpolação linear entre duas cores (uma em cada polo de uma esfera).         |

    

     

3.  Compute o radiance de saída.

    A equação 1 agora precisa ser avaliada em cada ponto usando um vértice ou sombreador de pixel. Antes que o sombreador possa ser avaliado, as constantes devem ser pré-computadas e carregadas na tabela constante (consulte o Exemplo de demonstração de [PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) para obter detalhes). O sombreador em si é uma implementação simples dessa equação.

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

Para obter mais informações sobre PRT e harmônicos esféricos, consulte os seguintes artigos:


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

[Equações prt (Direct3D 9)](prt-equations.md)
</dt> <dt>

[Representando PRT com texturas (Direct3D 9)](representing-prt-with-textures.md)
</dt> <dt>

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> <dt>

[**ID3DXPRTEngine**](id3dxprtengine.md)
</dt> <dt>

[**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md)
</dt> <dt>

[Funções de transferência radiante preputadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 



