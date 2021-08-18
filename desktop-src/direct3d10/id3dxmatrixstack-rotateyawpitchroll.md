---
description: Método ID3DXMATRIXStack::RotateYawPitchRoll (D3DX10.h) – gira (em relação ao espaço de coordenadas do mundo) em torno de um eixo arbitrário.
ms.assetid: 35e237f6-40f2-4001-adb0-f489d61f64e7
title: Método ID3DXMATRIXStack::RotateYawPitchRoll (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRoll
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e43422e5872708a61b5f066725e61c16e55d04dd94f5c8527c7b86e1f7a543c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128328"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx10h"></a>Método ID3DXMATRIXStack::RotateYawPitchRoll (D3DX10.h)

Gira (em relação ao espaço de coordenadas do mundo) em torno de um eixo arbitrário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Yaw* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

O yaw em torno do eixo y em radianos.

</dd> <dt>

*Apresentação* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

O tom em torno do eixo x em radianos.

</dd> <dt>

*Roll* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

O roll around do eixo z em radianos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK.

## <a name="remarks"></a>Comentários

Esse método adiciona a rotação à pilha de matrizes com a matriz de rotação computada semelhante à seguinte:


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



Como a rotação é multiplicada à direita para a pilha de matriz, a rotação é relativa ao espaço de coordenadas do mundo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
