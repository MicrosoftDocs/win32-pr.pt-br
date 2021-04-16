---
description: Determina se um raio intersecciona com uma malha.
ms.assetid: 325f5b40-80ba-4400-a143-bae41146ab07
title: Função D3DXIntersect (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc877fb1301e01b05184625ba2e92a2c680cfa9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105773003"
---
# <a name="d3dxintersect-function"></a>Função D3DXIntersect

Determina se um raio intersecciona com uma malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXIntersect(
  _In_        LPD3DXBASEMESH pMesh,
  _In_  const D3DXVECTOR3    *pRayPos,
  _In_  const D3DXVECTOR3    *pRayDir,
  _Out_       BOOL           *pHit,
  _Out_       DWORD          *pFaceIndex,
  _Out_       FLOAT          *pU,
  _Out_       FLOAT          *pV,
  _Out_       FLOAT          *pDist,
  _Out_       LPD3DXBUFFER   *ppAllHits,
  _Out_       DWORD          *pCountOfHits
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMesh* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Ponteiro para uma interface [**ID3DXBaseMesh**](id3dxbasemesh.md) , representando a malha a ser testada.

</dd> <dt>

*pRayPos* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando o ponto em que o raio começa.

</dd> <dt>

*pRayDir* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando a direção do raio.

</dd> <dt>

*pHit* \[ fora\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)\***

Ponteiro para um BOOL. Se Ray Interseccionar uma face triangular na malha, esse valor será definido como **true**. Caso contrário, esse valor será definido como **false**.

</dd> <dt>

*pFaceIndex* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Aponta para um valor de índice da face mais próxima da origem Ray, se pHit for **true**.

</dd> <dt>

*pU* \[ fora\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para uma coordenada de pressionamento de barycentric, U.

</dd> <dt>

*VP* \[ fora\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para uma coordenada de pressionamento de barycentric, V.

</dd> <dt>

*pDist* \[ fora\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para uma distância de parâmetro de interseção de raio.

</dd> <dt>

*ppAllHits* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ponteiro para um objeto [**ID3DXBuffer**](id3dxbuffer.md) , que contém uma matriz de estruturas [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) .

</dd> <dt>

*pCountOfHits* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para um DWORD que contém o número de entradas na matriz ppAllHits.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A função **D3DXIntersect** fornece uma maneira de entender os pontos em um triângulo, independentemente de onde o triângulo realmente está localizado. Essa função retorna o ponto resultante usando a seguinte equação: v1 + U (v2-v1) + V (v3-v1).

Qualquer ponto no V1V2V3 do plano pode ser representado pela coordenada barycentric (U, V). O parâmetro U controla a quantidade de v2 que é ponderada no resultado, e o parâmetro V controla a quantidade de v3 ponderada no resultado. Por fim, o valor de \[ 1-(U + V) \] controla o quanto v1 é ponderado no resultado.

As coordenadas de barycentric são uma forma de coordenadas gerais. Nesse contexto, o uso de coordenadas barycentric representa uma alteração nos sistemas de coordenadas. O que se aplica a coordenadas cartesianas é verdadeiro para coordenadas barycentrics.

As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo. Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
