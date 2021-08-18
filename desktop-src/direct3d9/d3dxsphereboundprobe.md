---
description: Função D3DXSphereBoundProbe (D3DX9Mesh.h) – determina se um raio intersecção do volume da caixa delimitada de uma esfera.
ms.assetid: fa2e9ecf-7905-4a62-ba48-774bd522525a
title: Função D3DXSphereBoundProbe (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 85dbd46233176d65e7e7abbf0eb266c81868ceba7e67e3257bf902d1775d6a90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731149"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a>Função D3DXSphereBoundProbe (D3DX9Mesh.h)

Determina se um raio intersecção do volume da caixa delimitada de uma esfera.

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

*pCenter* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR3,**](d3dxvector3.md) especificando a coordenada central da esfera.

</dd> <dt>

*Raio* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Raio da esfera.

</dd> <dt>

*pRayPosition* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR3,**](d3dxvector3.md) especificando a coordenada de origem do raio.

</dd> <dt>

*pRayDirection* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR3,**](d3dxvector3.md) especificando a direção do raio. Esse vetor não deve ser (0,0,0), mas não precisa ser normalizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Retornará **TRUE** se o raio intersecção do volume da caixa delimitada da esfera. Caso contrário, **retornará FALSE.**

## <a name="remarks"></a>Comentários

**D3DXSphereBoundProbe** determina se o raio intersecção do volume da caixa delimitada da esfera, não apenas a superfície da esfera.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
