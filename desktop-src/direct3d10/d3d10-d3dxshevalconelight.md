---
description: Função D3DXSHEvalConeLight (D3DX10. h) – avalia uma luz que é um cone de intensidade constante e retorna Spectral dados harmônicas esféricas (SH).
ms.assetid: ad2b9c86-cf1a-426e-88e6-4c543519e002
title: Função D3DXSHEvalConeLight (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalConeLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f3dd506c8349bd4b8648e2670baf815fcc7bb946d8996e196cd4a9a1fc8e8067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990896"
---
# <a name="d3dxshevalconelight-function-d3dx10h"></a>Função D3DXSHEvalConeLight (D3DX10. h)

Avalia uma luz que é um cone de intensidade constante e retorna dados Spectral esféricos harmônicas (SH).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXSHEvalConeLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       Radius,
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

*Ordem* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da avaliação SH. Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes do Order ². O grau da avaliação é a ordem 1.

</dd> <dt>

*pDir* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para o vetor de direção do eixo hemisfério (x, y, z) no qual avaliar as funções de base SH. Consulte Observações.

</dd> <dt>

*RADIUS* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Raio de cone em radianos.

</dd> <dt>

*RIntensity* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

A intensidade vermelha da luz.

</dd> <dt>

*GIntensity* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

A intensidade verde da luz.

</dd> <dt>

*BIntensity* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

A intensidade azul da luz.

</dd> <dt>

*pROut* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor SH de saída para o componente vermelho.

</dd> <dt>

*pGOut* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor SH de saída para o componente verde.

</dd> <dt>

*pBOut* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor SH de saída para o componente azul.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Avalia uma luz que é um cone de intensidade constante e retorna dados Spectral SH. O vetor de saída é calculado de forma que, se a taxa de intensidade R/G/B for igual a 1, a saída radiante de um ponto diretamente sob a luz (orientada na direção do cone em um objeto difuso com um albedo de 1) seria 1,0. Isso computará três exemplos de Spectral; pROut será retornado, enquanto pGOut e pBOut podem ser retornados.

Na esfera com raio de unidade, conforme mostrado na ilustração a seguir, a direção pode ser especificada simplesmente com teta, o ângulo sobre o eixo z na direção da mão direita e Phi, o ângulo de z.

![ilustração de um Sphere com raio de unidade](images/spherical-coordinates.png)

As equações a seguir mostram a relação entre as coordenadas cartesianas (x, y, z) e esférico (teta, Phi) na esfera da unidade. O ângulo teta varia sobre o intervalo de 0 a 2 PI, enquanto Phi varia de 0 a PI.

![equações da relação entre coordenadas cartesianas e esférica](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
