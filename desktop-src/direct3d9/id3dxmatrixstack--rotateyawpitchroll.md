---
description: Gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.
ms.assetid: 25a7eff4-a575-4ddb-85eb-ef3fa2d6ae3b
title: 'Método ID3DXMATRIXStack:: RotateYawPitchRoll (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5020cb6ff3af41b9ef32ef77bb71607f6cd5ea6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793818"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx9mathh"></a>Método ID3DXMATRIXStack:: RotateYawPitchRoll (D3dx9math. h)

Gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.

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

*Guinada* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

A guinada em volta do eixo y em radianos.

</dd> <dt>

*Pitch* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

A inclinação em volta do eixo x em radianos.

</dd> <dt>

*Rolar* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

O rolo em volta do eixo z em radianos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK.

## <a name="remarks"></a>Comentários

Esse método adiciona a rotação à pilha de matriz com a matriz de rotação computada semelhante à seguinte:


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



Como a rotação é multiplicada à pilha da matriz, a rotação é relativa ao espaço de coordenadas do mundo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateAxis**](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateAxisLocal**](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateYawPitchRollLocal**](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
