---
description: Função D3DXVec3UnprojectArray (D3dx9math.h) – projeta uma matriz (x, y, z, 0) do espaço da tela no espaço do objeto.
ms.assetid: fef2a76c-c2fe-48c5-a1bb-6669bcc76b9b
title: Função D3DXVec3UnprojectArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7173ed5e912dea8eba08a8fc5e40b33e043ff2181df9e9fc2f62354bb2768fc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118986"
---
# <a name="d3dxvec3unprojectarray-function-d3dx9mathh"></a>Função D3DXVec3UnprojectArray (D3dx9math.h)

Projeta uma matriz (x, y, z, 0) do espaço da tela para o espaço do objeto.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_          UINT         OutStride,
  _In_    const D3DXVECTOR3  *pV,
  _In_          UINT         VStride,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld,
  _In_          UINT         n
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para a [**estrutura D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.

</dd> <dt>

*OutStride* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Distância entre vetores no fluxo de dados de saída.

</dd> <dt>

*pV* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para a estrutura [**D3DXVECTOR3 de**](d3dxvector3.md) origem.

</dd> <dt>

*VStride* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Distância entre vetores no fluxo de dados de entrada.

</dd> <dt>

*pViewport* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***

Ponteiro para uma [**estrutura D3DVIEWPORT9,**](d3dviewport9.md) representando o viewport.

</dd> <dt>

*pProjection* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para uma [**estrutura D3DXMATRIX,**](d3dxmatrix.md) representando a matriz de projeção.

</dd> <dt>

*pView* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para uma [**estrutura D3DXMATRIX,**](d3dxmatrix.md) representando a matriz de exibição.

</dd> <dt>

*pWorld* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para uma [**estrutura D3DXMATRIX,**](d3dxmatrix.md) representando a matriz mundial.

</dd> <dt>

*n* \[ em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de elementos na matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para uma [**estrutura D3DXVECTOR3**](d3dxvector3.md) que é a matriz projetada do espaço da tela para o espaço do objeto.

## <a name="remarks"></a>Comentários

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a [**função D3DXVec3Unproject**](d3dxvec3unproject.md) pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Project**](d3dxvec3project.md)
</dt> </dl>

 

 
