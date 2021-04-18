---
description: Determina se um raio intersecciona com essa malha.
ms.assetid: 74565d4a-94e6-4faa-bf70-9c1b35e5e5d8
title: Método ID3DX10Mesh::Intersect (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Intersect
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8ceed03ab21debf61371da9e53b5150d2dc83e4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105750535"
---
# <a name="id3dx10meshintersect-method"></a>Método ID3DX10Mesh:: Intersect

Determina se um raio intersecciona com essa malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Intersect(
  [in]  D3DXVECTOR3 *pRayPos,
  [in]  D3DXVECTOR3 *pRayDir,
  [in]  UINT        *pHitCount,
  [in]  UINT        *pFaceIndex,
  [in]  float       *pU,
  [in]  float       *pV,
  [in]  float       *pDist,
  [out] ID3D10Blob  **ppAllHits
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pRayPos* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , especificando o ponto em que o raio começa.

</dd> <dt>

*pRayDir* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , especificando a direção do raio.

</dd> <dt>

*pHitCount* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

O número de vezes que Ray interseccionado com a malha.

</dd> <dt>

*pFaceIndex* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Aponta para um valor de índice da face mais próxima da origem Ray, se pHit for **true**.

</dd> <dt>

*pU* \[ no\]
</dt> <dd>

Tipo: **float \***

Ponteiro para uma coordenada de pressionamento de barycentric, U.

</dd> <dt>

*VP* \[ no\]
</dt> <dd>

Tipo: **float \***

Ponteiro para uma coordenada de pressionamento de barycentric, V.

</dd> <dt>

*pDist* \[ no\]
</dt> <dd>

Tipo: **float \***

Ponteiro para uma distância de parâmetro de interseção de raio.

</dd> <dt>

*ppAllHits* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Ponteiro para uma [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), contendo uma matriz de estruturas de [**\_ \_ informações de interseção D3DX10**](d3dx10-intersect-info.md) . Esta é uma lista de todas as ocorrências que ocorreram no teste de interseção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Essa API fornece uma maneira de entender os pontos em um triângulo, independentemente de onde o triângulo realmente está localizado. Essa função retorna o ponto resultante usando a seguinte equação: v1 + U (v2-v1) + V (v3-v1).

Qualquer ponto no V1V2V3 do plano pode ser representado pela coordenada barycentric (U, V). O parâmetro U controla a quantidade de v2 que é ponderada no resultado, e o parâmetro V controla a quantidade de v3 ponderada no resultado. Por fim, o valor de \[ 1-(U + V) \] controla o quanto v1 é ponderado no resultado.

As coordenadas de barycentric são uma forma de coordenadas gerais. Nesse contexto, o uso de coordenadas barycentric representa uma alteração nos sistemas de coordenadas. O que se aplica a coordenadas cartesianas é verdadeiro para coordenadas barycentrics.

As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo. Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
