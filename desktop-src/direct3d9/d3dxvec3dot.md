---
description: Determina o produto de ponto de dois vetores 3D.
ms.assetid: 61aa7751-cc06-4673-929b-d7c1e691e395
title: Função D3DXVec3Dot (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 32b1387c1299c5ed3a379b06e3157d1c359c3f1d4fc3db39ee8c51c4997b6834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297788"
---
# <a name="d3dxvec3dot-function"></a>Função D3DXVec3Dot

Determina o produto de ponto de dois vetores 3D.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT D3DXVec3Dot(
  _In_ const D3DXVECTOR3 *pV1,
  _In_ const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pV1* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3 de**](d3dxvector3.md) origem.

</dd> <dt>

*pV2* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3 de**](d3dxvector3.md) origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

O produto de ponto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Cross**](d3dxvec3cross.md)
</dt> </dl>

 

 
