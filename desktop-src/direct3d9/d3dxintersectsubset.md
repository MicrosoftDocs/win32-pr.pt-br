---
description: Intersecção do raio especificado com o subconjunto de malha especificado. Isso fornece funcionalidade semelhante ao D3DXIntersect.
ms.assetid: 4a757b9e-18eb-424e-9f3e-cdf917c23787
title: Função D3DXIntersectSubset (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectSubset
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95a987730706f32654aab8f63feed61ae87c4d58d27ccccdaed9767d3303bbf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460376"
---
# <a name="d3dxintersectsubset-function"></a>Função D3DXIntersectSubset

Intersecção do raio especificado com o subconjunto de malha especificado. Isso fornece funcionalidade semelhante ao [**D3DXIntersect.**](d3dxintersect.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXIntersectSubset(
  _In_        LPD3DXBASEMESH pMesh,
  _In_        DWORD          AttribId,
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

*pMesh* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Ponteiro para uma [**interface ID3DXBaseMesh,**](id3dxbasemesh.md) representando a malha a ser testada. A malha deve ser classificação de atributo.

</dd> <dt>

*AttribId* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Identificador de atributo do subconjunto com o que intersecção.

</dd> <dt>

*pRayPos* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR3,**](d3dxvector3.md) especificando o ponto em que o raio começa.

</dd> <dt>

*pRayDir* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR3,**](d3dxvector3.md) especificando a direção do raio.

</dd> <dt>

*pHit* \[ out\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)\***

Ponteiro para um BOOL. Se o raio intersecção de um rosto triangular na malha, esse valor será definido como **TRUE.** Caso contrário, esse valor será definido como **FALSE.**

</dd> <dt>

*pFaceIndex* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para um valor de índice da face mais próxima da origem do raio, se pHit for **TRUE.**

</dd> <dt>

*pU* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para uma coordenada de acerto centrada em barras, U.

</dd> <dt>

*pV* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para uma coordenada de acerto centrada em barras, V.

</dd> <dt>

*pDist* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para uma distância de parâmetro de interseção de raio.

</dd> <dt>

*ppAllHits* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Matriz de [**estruturas D3DXINTERSECTINFO,**](d3dxintersectinfo.md) representando todas as acertos, não apenas as acertos mais próximos.

</dd> <dt>

*pCountOfHits* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Número de elementos na matriz retornada de ppAllHits.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser o seguinte valor: E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A **função D3DXIntersectSubset** fornece uma maneira de entender os pontos dentro e ao redor de um triângulo, independentemente de onde o triângulo está realmente localizado. Essa função retorna o ponto resultante usando a seguinte equação: V1 + U(V2 - V1) + V(V3 - V1).

Qualquer ponto no plano V1V2V3 pode ser representado pela coordenada centrada em barras (U,V). O parâmetro U controla quanto V2 é ponderado no resultado e o parâmetro V controla quanto V3 é ponderado no resultado. Por fim, o valor de 1 - (U + V) controla quanto V1 é \[ \] ponderado no resultado.

Coordenadas barycentric são uma forma de coordenadas gerais. Nesse contexto, o uso de coordenadas centradas em barras representa uma alteração em sistemas de coordenadas. O que é verdadeiro para coordenadas cartesianas é verdadeiro para coordenadas centradas em barras.

As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo. Para obter uma descrição mais detalhada das coordenadas centradas em barras, consulte Descrição de [coordenadas barycentric da Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
