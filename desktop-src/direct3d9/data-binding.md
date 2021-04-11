---
description: Use a coleção SasHostParameterValue para definir a coleção de valores do aplicativo host, bem como seu tipo e membros, expostos a efeitos.
ms.assetid: 3fef353d-323a-4cc1-a8c9-2bf154754835
title: Associação de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b67305d4acc8a4ed9e0827203e4602db26a99da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104295957"
---
# <a name="data-binding"></a>Associação de dados

Use a [coleção SasHostParameterValue](#sashostparametervalue-collection) para definir a coleção de valores do aplicativo host, bem como seu tipo e membros, expostos a efeitos. Use a anotação [SasBindAddress](#sasbindaddress) em um arquivo de efeito para associar um parâmetro de efeito ao seu parâmetro correspondente no aplicativo host.

## <a name="sashostparametervalue-collection"></a>Coleção SasHostParameterValue

O SasHostParameterValue é definido usando a sintaxe de arquivo de efeito (. FX). Embora a sintaxe seja muito semelhante à sintaxe do arquivo de efeito, existem algumas diferenças. Por exemplo, tipos de objeto, como Texture2D, amostras e cadeias de caracteres, não são válidos em arquivos de efeito reais, mas são válidos no SasHostParameterValue. Um aplicativo host pode implementar o SasHostParameterValue de qualquer forma, desde que esteja de acordo com a descrição abaixo; a definição real está localizada no arquivo de inclusão do efeito padrão DXSAS ( \[ /Utilities/Source/SAS/SAS.fxh raiz do SDK \] ).

Observe que as matrizes no SasHostParameterValue, como luzes ou câmeras, têm comprimento não associado. Isso significa que os efeitos podem ser associados a qualquer índice arbitrário nessas matrizes e os aplicativos de host devem fornecer padrões significativos nos casos em que nenhum valor de aplicativo pode ser fornecido.

Alguns tipos e constantes são necessários para serem definidos no DXSAS padrão include, conforme observado na definição da inclusão padrão. Isso permite que os efeitos associem facilmente os valores agregados do SasHostParameterValue aos parâmetros de efeito estruturados.



| Coleção SasHostParameterValue    | Tipo            | Membro                                       |
|-------------------------------------|-----------------|----------------------------------------------|
| [Hora](#time)                       | FLOAT           | SAS. time. Now                                 |
|                                     | FLOAT           | SAS. time. Last                                |
|                                     | INT             | SAS. time. FrameNumber                         |
| [Mapa de ambiente](#environment-map) | textureCUBE     | SAS. EnvironmentMap                           |
| [Câmera](#camera)                   | SasCamera       | SAS. Camera                                   |
|                                     | float4x4        | SAS. Camera. WorldToView                       |
|                                     | float4x4        | SAS. Camera. projeção                        |
|                                     | float2          | SAS. Camera. NearFarClipping                   |
| [Claro](#light)                     | SasAmbientLight | AmbientLight \[ ZeroOrMore \] ;                  |
|                                     | INT             | SAS. NumAmbientLights                         |
|                                     | SasAmbientLight | DirectionalLight \[ ZeroOrMore \] ;              |
|                                     | INT             | SAS. NumDirectionalLights                     |
|                                     | SasAmbientLight | PointLight \[ ZeroOrMore \] ;                    |
|                                     | INT             | SAS. NumPointLights                           |
|                                     | SasAmbientLight | \[ZeroOrMore Spotlight \] ;                     |
|                                     | INT             | SAS. NumSpotLights                            |
| [Shadow](#shadow)                   | float4x4        | SAS. Shadow \[ ZeroOrMore \] . WorldToShadow       |
|                                     | texture2D       | SAS. Shadow \[ ZeroOrMore \] . ShadowMap           |
| [Reduzida](#skeleton)               | float4x4        | SAS. esqueleto. MeshToJointToWorld \[ OneOrMore\] |
|                                     | INT             | SAS. esqueleto. NumJoints                       |



 

### <a name="time"></a>Hora

O valor do relógio ou tempo virtual do aplicativo host. Os membros incluem:

-   SAS. time. Now-o valor do relógio virtual do aplicativo host no ponto em que o efeito será renderizado.
-   SAS. time. Last-o valor de agora na renderização anterior.
-   SAS. time. FrameNumber-o valor do contador que é incrementado uma vez por quadro renderizado.

Os efeitos devem lidar corretamente com o fato de que os valores desses membros podem ser encapsulados potencialmente durante tempos de execução extremamente longos. Agora e o último podem ter valores muito grandes.

### <a name="environment-map"></a>Mapa de ambiente

Um mapa de ambiente cúbico. Os aplicativos host devem fornecer uma textura de cubo válida se um efeito tentar se associar a SAS. EnvironmentMap.

### <a name="camera"></a>Câmera

A câmera que está sendo renderizada no momento. Os membros incluem:

-   SAS. Camera. WorldToView-a matriz de exibição do mundo composto da câmera.
-   SAS. Camera. Projetion-a matriz de projeção da câmera.
-   SAS. Camera. NearFarClipping-os valores dos planos de recorte próximo e longe.

### <a name="light"></a>Claro

Uma ou mais luzes de cena. A coleção de luzes é declarada como uma matriz em que:

-   Cor-uma cor RGB. O valor padrão é (0, 0, 0).
-   Direção-a direção da luz. O valor padrão é (0, 0, 0).
-   Intervalo – a distância da luz em que os raios claros não têm efeito sobre a cena. O valor padrão é 0.
-   Teta-o ângulo de cone interno de um Spotlight, medido em radianos. O valor padrão é 0.
-   Phi-o ângulo de cone externo de um Spotlight, medido em radianos. O valor padrão é 0.

O número de luzes deve ser definido como o número de luzes associadas à matriz associada. Os efeitos podem optar por ignorar o número de luzes e associar a qualquer elemento de uma das matrizes leves. Portanto, os aplicativos host devem fornecer uma Associação válida para elementos além do número de luzes na matriz.

ZeroOrMore implica que a matriz pode ter qualquer número de elementos.

### <a name="shadow"></a>Shadow

Buffers de sombra que consistem em:

-   WorldToShadow – uma matriz de matrizes.
-   ShadowMap-um arquivo de textura 2D.

ZeroOrMore implica que a matriz pode ter qualquer número de elementos (zero significa uma matriz vazia).

Um efeito declararia um amostra da seguinte maneira:


```
texture2D Shadow 
<
  string SasBindAddress = "Sas.Shadow[0].ShadowMap";
>;

sampler ShadowSampler = shadow_sampler(Shadow);
```



### <a name="skeleton"></a>Reduzida

O conjunto de quadros que compõem o objeto de processamento no momento. Os exemplos de quadro são Bones e transformações. Isso inclui:

-   MeshToJointToWorld – uma matriz de matrizes.
-   NumJoints-o número de junções no esqueleto.

OneOrMore implica que a matriz tem pelo menos uma e pode conter qualquer número de elementos.

A definição dá suporte a objetos de malha rígidas e com revestimento, usando o mesmo conjunto de valores de [coleção SasHostParameterValue](#sashostparametervalue-collection) com diferentes interpretações.

## <a name="sasbindaddress"></a>SasBindAddress

Essa anotação é adicionada à parte superior de um arquivo de efeito para associar um parâmetro de efeito ao seu parâmetro correspondente definido na [coleção SasHostParameterValue](#sashostparametervalue-collection). A anotação é declarada da seguinte maneira:


```
string SasBindAddress = "SasHostParameterValue";
```



Este exemplo associa a matriz mundial de efeito à matriz MeshToJointToWorld:


```
float4x3 World
<
  string SasBindAddress = "Sas.Skeleton.MeshToJointToWorld[0]";
>;
```



Essa anotação informa ao aplicativo host que ele precisa para definir o valor da matriz mundial de efeito usando os dados na matriz MeshToJointToWorld.

A sintaxe de anotação de endereço de associação foi definida para ser muito semelhante à sintaxe usada pelo [**ID3DXEffect**](id3dxeffect.md) para obter e definir parâmetros de efeito. A única diferença entre os métodos DXSAS Grammar e **ID3DXEffect** é a adição do token de índice de asterisco. Aqui está outro exemplo usando o índice de asterisco:


```
float3 LightColors[6]
<
  string SasBindAddress = "Sas.Light[*].Color";
>;
```



O token de índice de asterisco denota que todos os elementos da matriz de valores de envirnmant do host específico (cor, nesse caso) devem estar associados ao parâmetro associado. Vários tokens de índice de asterisco permitem que os efeitos sejam associados a subelementos de uma matriz de estruturas sem a necessidade de associar toda a estrutura em si. Este exemplo associa os valores de cor das seis primeiras luzes a um parâmetro de efeito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de semântica e anotações padrão do DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



