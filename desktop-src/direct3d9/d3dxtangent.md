---
description: Define as configurações usadas para cálculos de quadros tangentes de malha.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: Enumeração D3DXTANGENT (D3dx9mesh.h)
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
ms.openlocfilehash: 5d6e57d2027a7366ec2b82ac7bd82aae4275d489c17f1922684e3ca6232be940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749765"
---
# <a name="d3dxtangent-enumeration"></a>Enumeração D3DXTANGENT

Define as configurações usadas para cálculos de quadros tangentes de malha.

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

<span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT \_ WRAP \_ U**
</dt> <dd>

Os valores de coordenadas de textura na direção u estão entre 0 e 1. Nesse caso, um conjunto de coordenadas de textura será escolhido que minimiza o perímetro do triângulo. Consulte [Quebra de textura (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ WRAP \_ V**
</dt> <dd>

Os valores de coordenadas de textura na direção v estão entre 0 e 1. Nesse caso, um conjunto de coordenadas de textura será escolhido que minimiza o perímetro do triângulo. Consulte [Quebra de textura (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT \_ WRAP \_ UV**
</dt> <dd>

Os valores de coordenadas de textura nas direções v e você estão entre 0 e 1. Nesse caso, um conjunto de coordenadas de textura será escolhido que minimiza o perímetro do triângulo. Consulte [Quebra de textura (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ NÃO \_ NORMALIZAR \_ PARCIAIS**
</dt> <dd>

Não normalize derivados parciais em relação às coordenadas de textura. Se não for normalizado, a escala dos derivados parciais será proporcional à escala do modelo 3D dividida pela escala do triângulo no espaço (u, v). Esse valor de escala fornece uma medida de quanto a textura é ampliada em uma determinada direção. O comprimento do vetor resultante é uma soma ponderada dos comprimentos dos derivados parciais.

</dd> <dt>

<span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT \_ DONT \_ ORGONALIZE**
</dt> <dd>

Não transforme coordenadas de textura em coordenadas cartesianas ortogonais. Mutuamente exclusivo com D3DXTANGENT ORTOGONALIZE DE você e \_ \_ \_ D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ V.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**ORTOGONALIZE D3DXTANGENT \_ \_ DE \_ V**
</dt> <dd>

Compute o derivado parcial em relação à coordenada de textura v independentemente para cada vértice e, em seguida, calcule o derivado parcial em relação a você como o produto cruzado do derivado parcial em relação a v e ao vetor normal. Mutuamente exclusivo com D3DXTANGENT \_ DONT \_ ORTHOGONALIZE e D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ U.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**ORTOGONALIZE D3DXTANGENT \_ \_ DA \_ U**
</dt> <dd>

Calcule o derivado parcial em relação à coordenada de textura u independentemente para cada vértice e, em seguida, calcule o derivado parcial em relação a v como o produto cruzado do vetor normal e o derivado parcial em relação a você. Mutuamente exclusivo com D3DXTANGENT \_ DONT \_ ORTHOGONALIZE e D3DXTANGENT \_ ORTOGONALIZE \_ FROM \_ V.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT \_ WEIGHT \_ BY \_ AREA**
</dt> <dd>

Peso a direção do vetor derivado normal ou parcial por vértice calculado de acordo com as áreas dos triângulos anexados a esse vértice. Mutuamente exclusivo com D3DXTANGENT \_ WEIGHT \_ EQUAL.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**PESO IGUAL A D3DXTANGENT \_ \_**
</dt> <dd>

Compute um vetor normal de comprimento de unidade para cada triângulo da malha de entrada. Mutuamente exclusivo com D3DXTANGENT \_ WEIGHT \_ BY \_ AREA.

</dd> <dt>

<span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT \_ WIND \_ CW**
</dt> <dd>

Os vértices são ordenados em uma direção no sentido horário em torno de cada triângulo. Portanto, a direção do vetor normal computada é invertida 180 graus da direção calculada usando a ordenação de vértice no sentido anti-horário.

</dd> <dt>

<span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ CALCULA \_ OS NORMAIS**
</dt> <dd>

Compute o vetor normal por vértice para cada triângulo da malha de entrada e ignore todos os vetores normais já na malha de entrada.

</dd> <dt>

<span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT \_ GENERATE \_ \_ IN-PLACE**
</dt> <dd>

Os resultados são armazenados na malha de entrada original e a malha de saída não é usada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




