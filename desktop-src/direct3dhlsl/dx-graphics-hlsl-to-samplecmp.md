---
title: SampleCmp (objeto de textura HLSL do DirectX)
description: Amostra uma textura e compara um único componente com o valor de comparação especificado.
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a606ad9081f1ca1fdc4261d862ea6edfef4460989bb6d51d839d85f5797c1466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854636"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a>SampleCmp (objeto de textura HLSL do DirectX)

Amostra uma textura e compara um único componente com o valor de comparação especificado.

<table>
<tbody>
<tr class="odd">
<td>float Object.SampleCmp( <dl> SamplerComparisonState S,<br />
local float,<br />
float CompareValue,<br />
[int Offset]<br />
</dl>);</td>
</tr>
</tbody>
</table>
 

A comparação é uma comparação de componente único entre o primeiro componente armazenado na textura e o valor de comparação passado para o método .

Esse método pode ser invocado somente de um sombreador de pixel; Não há suporte para ele em um sombreador de vértice ou geometry.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*
</dt> <dd>

Qualquer [tipo de objeto de](dx-graphics-hlsl-to-type.md) textura (exceto Texture2DMS, Texture2DMSArray ou Texture3D).

</dd> <dt>

<span id="S"></span><span id="s"></span>*S*
</dt> <dd>

\[em Um estado de comparação de amostra, que é o estado do amostrador mais um estado de comparação (uma função de comparação \] e um filtro de comparação). Consulte o [tipo de amostra para](dx-graphics-hlsl-sampler.md) obter detalhes e um exemplo.

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Localização*
</dt> <dd>

\[em \] As coordenadas de textura. O tipo de argumento depende do tipo de objeto de textura.

| Texture-Object tipo          | Tipo de parâmetro |
|------------------------------|----------------|
| Texture1D                    | FLOAT          |
| Texture1DArray, Texture2D    | float2         |
| Texture2DArray; TextureCube | float3         |
| TextureCubeArray;            | float4         |

</dd> <dt>

<span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*
</dt> <dd>

Um valor de ponto flutuante a ser usado como um valor de comparação.

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Deslocamento*
</dt> <dd>

\[em Um deslocamento de coordenada de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao \] local antes da amostragem. Os deslocamentos de textura precisam ser estáticos. O tipo de argumento depende do tipo de objeto de textura. Para obter mais informações, consulte [Aplicando deslocamentos de coordenadas de textura.](dx-graphics-hlsl-to-sample.md)

| Texture-Object tipo            | Tipo de parâmetro |
|--------------------------------|----------------|
| Texture1D, Texture1DArray      | INT            |
| Texture2D, Texture2DArrayArray     | int2           |
| TextureCube, TextureCubeArrayArray | Sem suporte  |

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor de ponto flutuante no intervalo \[ 0,.1 \] .

Para cada texel buscado (com base na configuração de amostra do modo de filtro), **SampleCmp** executa uma comparação do valor z (3º componente de entrada) do sombreador em relação ao valor de texel (1 se a comparação for aprovada; caso contrário, 0). Em seguida, **SampleCmp** combina esses resultados 0 e 1 para cada texel como na filtragem de textura normal (não uma média) e retorna o valor resultante \[ de 0,.1 para o \] sombreador.

## <a name="remarks"></a>Comentários

A filtragem de comparação fornece uma operação de filtragem básica que é útil para filtragem de porcentagem mais próxima.

Ao usar esse método em um recurso de ponto flutuante (em vez de um formato normalizado ou não assinado normalizado), o valor de comparação não é fixado automaticamente entre 0,0 e 1,0. Portanto, uma fixação manual do valor de comparação pode ser necessária para técnicas comuns de sombreamento.

Use um deslocamento somente em um miplevel inteiro; caso contrário, você poderá obter resultados diferentes dependendo da implementação de hardware ou das configurações de driver.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.

| vs \_ 4 \_ 0 | vs \_ 4 \_ 1; | ps \_ 4 \_ 0 | ps \_ 4 \_ 1; | gs \_ 4 \_ 0 | gs \_ 4 \_ 1; |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x;       | x         |          |           |

1.  Texture2DArray e TextureCubeArray estão disponíveis no Modelo de Sombreador 4.1 ou superior.
2.  O Modelo de Sombreador 4.1 está disponível no Direct3D 10.1 ou superior.

> [!NOTE]  
> **SampleCmp** também está disponível em ps 4 \_ 0 \_ nível 9 1 e \_ 4 0 nível 9 3 quando você usa as técnicas descritas em Implementando buffers de sombra para o nível de recurso \_ \_ \_ \_ \_ [Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)).

## <a name="related-topics"></a>Tópicos relacionados

[Objeto de textura](dx-graphics-hlsl-to-type.md)
