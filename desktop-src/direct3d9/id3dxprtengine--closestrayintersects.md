---
description: Usa o rastreamento de raio eficiente em simulações de computação radiante (PRT) para determinar se um raio cruza uma malha.
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: 'Método ID3DXPRTEngine:: ClosestRayIntersects (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ClosestRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2620140337807891efa739da4540e3895394f63bcc494396c13e7c15d0c1b29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729782"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a>Método ID3DXPRTEngine:: ClosestRayIntersects

Usa o rastreamento de raio eficiente em simulações de computação radiante (PRT) para determinar se um raio cruza uma malha. Se uma interseção for encontrada, o método retornará o índice da face de malha mais próxima atingida pelas coordenadas Ray e barycentric do ponto de interseção.

## <a name="syntax"></a>Sintaxe


```C++
BOOL ClosestRayIntersects(
  [in]  const D3DXVECTOR3 *pRayPos,
  [in]  const D3DXVECTOR3 *pRayDir,
  [in]        DWORD       *pFaceIndex,
  [out]       FLOAT       *pU,
  [out]       FLOAT       *pV,
  [out]       FLOAT       *pDist
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pRayPos* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando o ponto em que o raio começa.

</dd> <dt>

*pRayDir* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando a direção normalizada do raio.

</dd> <dt>

*pFaceIndex* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para o índice da face de malha atual que é primeiro atingido pelo raio fornecido, com base no empilhamento de todas as faces de malha de bloqueadores na frente da malha atual.

</dd> <dt>

*pU* \[ fora\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para uma coordenada de pressionamento de barycentric, U, para o vértice 0 do triângulo.

</dd> <dt>

*VP* \[ fora\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para uma coordenada de pressionamento de barycentric, V, para o vértice 1 do triângulo.

</dd> <dt>

*pDist* \[ fora\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para a distância do ponto de interseção ao longo do raio.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Retornará **true** se Ray Interseccionar a malha atual; caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Use [**ID3DXPRTEngine:: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) para definir distâncias mínimas e máximas de interseção com Ray.

A coordenada barycentric do terceiro vértice (vértice 2) do triângulo é 1-(U + V).

Esse método é executado mais devagar que [**ID3DXPRTEngine:: ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md). Use **ID3DXPRTEngine:: ShadowRayIntersects** se o local do ponto de interseção não for necessário.

As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo. Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
