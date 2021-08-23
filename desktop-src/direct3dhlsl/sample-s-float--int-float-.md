---
title: Função de exemplo (S, float, int, float) (referência de HLSL)
description: Amostras de um Texture2D com um valor opcional para fixe os valores de LOD (nível de detalhe) de exemplo para.
ms.assetid: 899FACB6-40BB-471B-82A7-BDBBC63B206E
keywords:
- Exemplo de função HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d22cf5fa8a8fe03a62b554def7caf28b4c4e8ab9065446bab9281e4e791e5d3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986216"
---
# <a name="samplesfloatintfloat-function-hlsl-reference"></a>Função de exemplo (S, float, int, float) (referência de HLSL)

Amostras de um [**Texture2D**](sm5-object-texture2d.md) com um valor opcional para fixe os valores de LOD (nível de detalhe) de exemplo para.

> [!Note]  
> Requer o [modelo de sombreador 5](d3d11-graphics-reference-sm5.md) ou superior.

 

## <a name="syntax"></a>Sintaxe

``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float Location,
  in int Offset,
  in float Clamp
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*S* \[ em\]
</dt> <dd>

Um [estado de amostra](dx-graphics-hlsl-sampler.md). Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.

</dd> <dt>

*Local* \[ do no\]
</dt> <dd>

As coordenadas de textura. O tipo de argumento é dependente do tipo de objeto Texture.



| Tipo de Texture-Object                    | Tipo de parâmetro |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Deslocamento* \[ no\]
</dt> <dd>

Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem. Os deslocamentos de textura precisam ser estáticos. O tipo de argumento é dependente do tipo de objeto Texture. Para obter mais informações, consulte [aplicando deslocamentos de coordenadas de textura](dx-graphics-hlsl-to-sample.md).



| Tipo de Texture-Object           | Tipo de parâmetro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | INT            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | Int3           |
| TextureCube, TextureCubeArray | sem suporte  |



 

</dd> <dt>

*Fixe* \[ no\]
</dt> <dd>

Um valor opcional para fixe os valores de LOD de exemplo para. Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="remarks"></a>Comentários

A amostragem de textura usa a posição Texel para pesquisar um valor de Texel. Um deslocamento pode ser aplicado à posição antes da pesquisa. O estado de amostra contém as opções de amostragem e filtragem. Esse método pode ser invocado dentro de um sombreador de pixel, mas não tem suporte em um sombreador de vértice ou em um sombreador de geometria.

Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados diferentes dependendo da implementação do hardware ou das configurações do driver.

### <a name="calculating-texel-positions"></a>Calculando posições texels

As coordenadas de textura são valores de ponto flutuante que referenciam dados de textura, que também são conhecidos como espaço de textura normalizado. Os modos de disposição de endereço são aplicados nesta ordem (coordenadas de textura + deslocamentos + modo de encapsulamento) para modificar as coordenadas de textura fora do \[ intervalo 0... 1 \] .

Para matrizes de textura, um valor adicional no parâmetro Location especifica um índice em uma matriz de textura. Esse índice é tratado como um valor flutuante de escala (em vez do espaço normalizado para coordenadas de textura padrão). A conversão para um índice de inteiro é feita na seguinte ordem (float + Round-to-the mais próximo inteiro + fixe para o intervalo de matriz).

### <a name="applying-texture-coordinate-offsets"></a>Aplicando deslocamentos de coordenadas de textura

O parâmetro offset modifica as coordenadas de textura, no espaço Texel. Embora as coordenadas de textura sejam números de ponto flutuante normalizados, o deslocamento aplica um deslocamento de inteiro. Observe também que os deslocamentos de textura precisam ser estáticos.

O formato de dados retornado é determinado pelo formato de textura. Por exemplo, se o recurso de textura tiver sido definido com o formato DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, a operação de amostragem converterá texels de amostra de gama 2,0 para 1,0, filtrará e gravará o resultado como um valor de ponto flutuante no intervalo \[ 0.. 1 \] .

Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de exemplo](texture-sample-overload.md)
</dt> <dt>

[Textura-objeto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
