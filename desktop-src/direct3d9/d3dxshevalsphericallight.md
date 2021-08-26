---
description: Função D3DXSHEvalSphericalLight (D3dx9math. h) – avalia uma luz esférica e retorna os dados de Spectral esférico harmônica (SH).
ms.assetid: aa46c162-9c2d-49c0-925c-d0c06456f918
title: Função D3DXSHEvalSphericalLight (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalSphericalLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0b6618747659c62b6ce954725690a6d707cead489db56788850bbe8eca216acf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027266"
---
# <a name="d3dxshevalsphericallight-function-d3dx9mathh"></a>Função D3DXSHEvalSphericalLight (D3dx9math. h)

Avalia uma luz esférica e retorna dados Spectral esféricos (SH).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pPos,
  _In_        FLOAT       Radius,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ordem* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da avaliação SH. Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes do Order ². O grau da avaliação é a ordem 1.

</dd> <dt>

*pPos* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para a posição da luz.

</dd> <dt>

*RADIUS* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Raio da fonte de luz esférica.

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

*pROut* \[ fora\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor SH de saída para o componente vermelho.

</dd> <dt>

*pGOut* \[ fora\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor SH de saída para o componente verde.

</dd> <dt>

*pBOut* \[ fora\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor SH de saída para o componente azul.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Avalia uma luz esférica e retorna dados de Spectral SH. Não há nenhuma normalização da intensidade da luz como há para [luzes direcionais](light-types.md), portanto, é preciso tomar cuidado ao especificar as intensidades. Isso computará três exemplos de Spectral; *pROut* será retornado, enquanto *pGOut* e *pBOut* podem ser retornados.

Na esfera com raio de unidade, conforme mostrado na ilustração a seguir, a direção pode ser especificada simplesmente com teta, o ângulo sobre o eixo z na [direção da mão direita](coordinate-systems.md)e Phi, o ângulo de z.

![ilustração de um Sphere com raio de unidade](images/spherical-coordinates.png)

As equações a seguir mostram a relação entre as coordenadas cartesianas (x, y, z) e esférico (teta, Phi) na esfera da unidade. O ângulo teta varia sobre o intervalo de 0 a 2 PI, enquanto Phi varia de 0 a PI.

![equações da relação entre coordenadas cartesianas e esférica](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Transferência radiante de computação (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
