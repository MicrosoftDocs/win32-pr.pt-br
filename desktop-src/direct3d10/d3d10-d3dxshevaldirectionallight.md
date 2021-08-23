---
description: Função D3DXSHEvalDirectionalLight (D3DX10.h) – avalia uma luz direcional e retorna dados sh (spherical spherical) espectral.
ms.assetid: b5c657f5-d291-4e53-908c-670b29a1888a
title: Função D3DXSHEvalDirectionalLight (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirectionalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7fb50ac274455c67da00d73f91319c0fa17ae85c46f74f4ef605af33e0085ddd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990886"
---
# <a name="d3dxshevaldirectionallight-function-d3dx10h"></a>Função D3DXSHEvalDirectionalLight (D3DX10.h)

Avalia uma luz direcional e retorna dados espéricos especulacionais (SH).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ordem* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordem da avaliação de SH. Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes orderâmicos. O grau da avaliação é Order - 1.

</dd> <dt>

*pDir* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para o vetor (x, y, z) de direção do eixo do sistema no qual as funções de base sh são avaliadas. Consulte Observações.

</dd> <dt>

*RIntensity* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

A intensidade vermelha da luz.

</dd> <dt>

*GIntensity* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

A intensidade verde da luz.

</dd> <dt>

*BIntensity* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

A intensidade azul da luz.

</dd> <dt>

*pROut* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor sh de saída para o componente vermelho.

</dd> <dt>

*pGOut* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro opcional para o vetor sh de saída para o componente verde.

</dd> <dt>

*pBOut* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro opcional para o vetor SH de saída para o componente azul.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

O vetor de saída é calculado para que, se a taxa de intensidade R/G/B for igual a 1, o radiamento de saída resultante de um ponto diretamente sob a luz em um objeto difuso com um albedo de 1 seria 1,0. Isso calculará três exemplos espectrais; pROut será retornado, enquanto pGOut e pBOut podem ser retornados.

Na esfera com raio de unidade, conforme mostrado na ilustração a seguir, a direção pode ser especificada simplesmente com theta, o ângulo sobre o eixo z na direção da direita e o ângulo de z.

![ilustração de uma esfera com raio de unidade](images/spherical-coordinates.png)

As equações a seguir mostram a relação entre as coordenadas cartesianas (x, y, z) e esféricas (theta, yo) na esfera de unidade. O ângulo de theta varia de 0 a 2 pi, enquanto que o valor varia de 0 a pi.

![equações da relação entre coordenadas cartesianas e esféricas](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
