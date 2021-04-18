---
description: Define as configurações usadas para computações de quadro tangente de malha.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: Enumeração D3DXTANGENT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTANGENT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 43e3c5ced0eee3366b85070ce89d19154d048ab4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798458"
---
# <a name="d3dxtangent-enumeration"></a>Enumeração D3DXTANGENT

Define as configurações usadas para computações de quadro tangente de malha.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXTANGENT { 
  D3DXTANGENT_WRAP_U                   = 0x01,
  D3DXTANGENT_WRAP_V                   = 0x02,
  D3DXTANGENT_WRAP_UV                  = 0x03,
  D3DXTANGENT_DONT_NORMALIZE_PARTIALS  = 0x04,
  D3DXTANGENT_DONT_ORTHOGONALIZE       = 0x08,
  D3DXTANGENT_ORTHOGONALIZE_FROM_V     = 0x010,
  D3DXTANGENT_ORTHOGONALIZE_FROM_U     = 0x020,
  D3DXTANGENT_WEIGHT_BY_AREA           = 0x040,
  D3DXTANGENT_WEIGHT_EQUAL             = 0x080,
  D3DXTANGENT_WIND_CW                  = 0x0100,
  D3DXTANGENT_CALCULATE_NORMALS        = 0x0200,
  D3DXTANGENT_GENERATE_IN_PLACE        = 0x0400
} D3DXTANGENT, *LPD3DXTANGENT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT \_ Wrap \_ U**
</dt> <dd>

Os valores de coordenadas de textura na direção u estão entre 0 e 1. Nesse caso, um conjunto de coordenadas de textura será escolhido para minimizar o perímetro do triângulo. Consulte [quebra de textura (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ Wrap \_ V**
</dt> <dd>

Os valores de coordenadas de textura na direção v estão entre 0 e 1. Nesse caso, um conjunto de coordenadas de textura será escolhido para minimizar o perímetro do triângulo. Consulte [quebra de textura (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**\_UV de encapsulamento D3DXTANGENT \_**
</dt> <dd>

Os valores de coordenadas de textura nas direções você e v estão entre 0 e 1. Nesse caso, um conjunto de coordenadas de textura será escolhido para minimizar o perímetro do triângulo. Consulte [quebra de textura (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ não \_ normalizar \_ parciais**
</dt> <dd>

Não normalizar derivações parciais em relação às coordenadas de textura. Se não for normalizado, a escala dos derivativos parciais será proporcional à escala do modelo 3D dividido pela escala do triângulo no espaço (u, v). Esse valor de escala fornece uma medida de quanto a textura é ampliada em uma determinada direção. O comprimento de vetor resultante é uma soma ponderada dos comprimentos dos derivativos parciais.

</dd> <dt>

<span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT \_ não \_ ortogonalize**
</dt> <dd>

Não transforme coordenadas de textura em coordenadas cartesianas ortogonal. Mutuamente exclusivo com D3DXTANGENT \_ ortogonale \_ de \_ você e D3DXTANGENT \_ ortogonalize \_ da \_ V.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT \_ ortogonalize \_ da \_ V**
</dt> <dd>

Compute a derivada parcial em relação à coordenada de textura v de forma independente para cada vértice e, em seguida, computar a derivada parcial com relação a você como o produto cruzado da derivada parcial em relação ao v e ao vetor normal. Mutuamente exclusivo com D3DXTANGENT não \_ é \_ ortogonalize e D3DXTANGENT \_ ortogonalize a \_ partir de \_ U.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT \_ ortogonale \_ de \_ U**
</dt> <dd>

Compute a derivada parcial em relação à coordenada de textura u independentemente para cada vértice e, em seguida, computar a derivada parcial com relação a v como o produto cruzado do vetor normal e o derivativo parcial em relação a você. Mutuamente exclusivo com D3DXTANGENT não \_ é \_ ortogonalize e D3DXTANGENT \_ ortogonalize \_ da \_ V.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**\_Peso D3DXTANGENT \_ por \_ área**
</dt> <dd>

Peso a direção do vetor derivado normal ou parcial por vértice de acordo com as áreas de triângulos anexadas a esse vértice. Mutuamente exclusivo com peso D3DXTANGENT \_ \_ igual.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**\_Peso D3DXTANGENT \_ igual**
</dt> <dd>

Compute um vetor normal de comprimento de unidade para cada triângulo da malha de entrada. Mutuamente exclusivo com peso D3DXTANGENT \_ \_ por \_ área.

</dd> <dt>

<span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**\_PV de vento D3DXTANGENT \_**
</dt> <dd>

Os vértices são ordenados em uma direção horária em volta de cada triângulo. Portanto, a direção de vetor normal calculada é invertida 180 graus a partir da direção calculada usando a ordenação de vértices no sentido anti-horário.

</dd> <dt>

<span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ calcular \_ Normals**
</dt> <dd>

Calcule o vetor normal por vértice para cada triângulo da malha de entrada e ignore todos os vetores normais já existentes na malha de entrada.

</dd> <dt>

<span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT \_ gerar \_ no \_ local**
</dt> <dd>

Os resultados são armazenados na malha de entrada original e a malha de saída não é usada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




