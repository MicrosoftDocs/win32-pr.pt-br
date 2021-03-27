---
title: Função de exemplo (S, float, int, float, uint) (referência de HLSL)
description: Exemplifica um Texture2D com um valor opcional para fixe de exemplo (LOD) de amostra para e retorna o status da operação.
ms.assetid: 1B9F48C4-DDB9-4547-B4AF-81A3ADA44C3F
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
ms.openlocfilehash: 9b378cb4031acecb8e0018053c7547e1948cc3e6
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/17/2020
ms.locfileid: "103643079"
---
# <a name="samplesfloatintfloatuint-function-hlsl-reference"></a>Função de exemplo (S, float, int, float, uint) (referência de HLSL)

Exemplifica um [**Texture2D**](sm5-object-texture2d.md) com um valor opcional para fixe de exemplo (LOD) de amostra para e retorna o status da operação.

> [!Note]  
> Requer o [modelo de sombreador 5](d3d11-graphics-reference-sm5.md) ou superior.

 

## <a name="syntax"></a>Sintaxe

``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float Location,
  in  int Offset,
  in  float Clamp,
  out uint Status
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

</dd> <dt>

*Status* \[ do fora\]
</dt> <dd>

O status da operação. Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features). Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de exemplo](texture-sample-overload.md)
</dt> <dt>

[Textura-objeto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
