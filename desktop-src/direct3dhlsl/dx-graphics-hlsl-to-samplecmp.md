---
title: SampleCmp (objeto de textura DirectX HLSL)
description: Faz a amostragem de uma textura e compara um único componente com relação ao valor de comparação especificado.
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6991bead4bfc42451c26fe5476b4c114626eb7e8
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/17/2020
ms.locfileid: "104988726"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a>SampleCmp (objeto de textura DirectX HLSL)

Faz a amostragem de uma textura e compara um único componente com relação ao valor de comparação especificado.

<table>
<tbody>
<tr class="odd">
<td>float Object. SampleCmp ( <dl> SamplerComparisonState S,<br />
Local de flutuação,<br />
comparent Comparevalue,<br />
[deslocamento int]<br />
</dl>);</td>
</tr>
</tbody>
</table>
 

A comparação é uma comparação de componente único entre o primeiro componente armazenado na textura e o valor de comparação passado para o método.

Esse método pode ser invocado somente de um sombreador de pixel; Não há suporte para ele em um vértice ou sombreador de geometria.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*
</dt> <dd>

Qualquer tipo [de objeto de textura](dx-graphics-hlsl-to-type.md) (exceto Texture2DMS, Texture2DMSArray ou Texture3D).

</dd> <dt>

<span id="S"></span><span id="s"></span>*&*
</dt> <dd>

\[em \] um estado de comparação de amostras, que é o estado de amostra, mais um estado de comparação (uma função de comparação e um filtro de comparação). Consulte o [tipo de amostra](dx-graphics-hlsl-sampler.md) para obter detalhes e um exemplo.

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Local*
</dt> <dd>

\[nas \] coordenadas de textura. O tipo de argumento é dependente do tipo de objeto Texture.

| Tipo de Texture-Object          | Tipo de parâmetro |
|------------------------------|----------------|
| Texture1D                    | FLOAT          |
| Texture1DArray, Texture2D    | float2         |
| Texture2DArray ¹, TextureCube | float3         |
| TextureCubeArray ¹            | float4         |

</dd> <dt>

<span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*Comparevalue*
</dt> <dd>

Um valor de ponto flutuante a ser usado como um valor de comparação.

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Desvio*
</dt> <dd>

\[em \] um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem. Os deslocamentos de textura precisam ser estáticos. O tipo de argumento é dependente do tipo de objeto Texture. Para obter mais informações, consulte [aplicando deslocamentos de coordenadas de textura](dx-graphics-hlsl-to-sample.md).

| Tipo de Texture-Object            | Tipo de parâmetro |
|--------------------------------|----------------|
| Texture1D, Texture1DArray      | INT            |
| Texture2D, Texture2DArray ¹     | int2           |
| TextureCube, TextureCubeArray ¹ | Sem suporte  |

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor de ponto flutuante no intervalo \[ 0.. 1 \] .

Para cada Texel buscada (com base na configuração de amostra do modo de filtro), **SampleCmp** executa uma comparação do valor z (terceiro componente de entrada) do sombreador com o valor Texel (1 se a comparação for aprovada; caso contrário, 0). Em seguida, **SampleCmp** mistura esses 0 e 1 resultados para cada Texel em conjunto, como na filtragem de textura normal (não uma média) e retorna o \[ valor 0.. 1 resultante \] para o sombreador.

## <a name="remarks"></a>Comentários

A filtragem de comparação fornece uma operação básica de filtragem que é útil para a filtragem de profundidade mais próxima do percentual.

Ao usar esse método em um recurso de ponto flutuante (em vez de um formato assinado de forma normalizada ou não-normalizado), o valor de comparação não é automaticamente clamped entre 0,0 e 1,0. Portanto, um fixe manual do valor de comparação pode ser necessário para técnicas de sombreamento comuns.

Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados diferentes dependendo da implementação do hardware ou das configurações do driver.

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.

| vs \_ 4 \_ 0 | vs \_ 4 \_ 1 ² | PS \_ 4 \_ 0 | PS \_ 4 \_ 1 ² | GS \_ 4 \_ 0 | GS \_ 4 \_ 1 ² |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x ¹       | x         |          |           |

1.  Texture2DArray e TextureCubeArray estão disponíveis no modelo de sombreador 4,1 ou superior.
2.  O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.

> [!NOTE]  
> O **SampleCmp** também está disponível em PS 4 \_ 0 \_ nível \_ 9 \_ 1 e 4 \_ 0 \_ nível \_ 9 \_ 3 quando você usa as técnicas descritas em [implementando buffers de sombra para o nível de recurso do Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)).

## <a name="related-topics"></a>Tópicos relacionados

[Textura-objeto](dx-graphics-hlsl-to-type.md)
