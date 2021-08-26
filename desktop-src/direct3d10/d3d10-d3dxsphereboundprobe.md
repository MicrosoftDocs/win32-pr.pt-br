---
description: Função D3DXSphereBoundProbe (D3DX10math. h) – determina se um raio intersecciona o volume da caixa delimitadora de uma esfera.
ms.assetid: 5984a1a6-d36c-4a05-8c74-0ece7443356c
title: Função D3DXSphereBoundProbe (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSphereBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 39e2b3871365cddd70b942f6d9d9f0fc9af85eca23944f388e3afd6ad9b4fc63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989956"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a>Função D3DXSphereBoundProbe (D3DX10math. h)

Determina se um raio intersecciona o volume da caixa delimitadora de uma esfera.

## <a name="syntax"></a>Sintaxe


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCenter* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , especificando a coordenada central da esfera.

</dd> <dt>

*RADIUS* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Raio da esfera.

</dd> <dt>

*pRayPosition* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , especificando a coordenada de origem do raio.

</dd> <dt>

*pRayDirection* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , especificando a direção do raio. Esse vetor não deve ser (0, 0, 0), mas não precisa ser normalizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Retornará **true** se Ray Interseccionar o volume da caixa delimitadora da esfera. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

**D3DXSphereBoundProbe** determina se Ray cruza o volume da caixa delimitadora da esfera, não apenas a superfície da esfera.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
