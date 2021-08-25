---
description: 'Método ID3DXMATRIXStack:: RotateAxisLocal (D3dx9math. h) – gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.'
ms.assetid: c7ef11e9-f4c4-4801-8f25-190066baeb52
title: 'Método ID3DXMATRIXStack:: RotateAxisLocal (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxisLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e46aa8767506aaabfcff6107ad184fad6dd8166097fbde955ac068f8f934ca22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629476"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx9mathh"></a>Método ID3DXMATRIXStack:: RotateAxisLocal (D3dx9math. h)

Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para o eixo arbitrário de rotação. Consulte [**D3DXVECTOR3**](d3dxvector3.md).

</dd> <dt>

*Ângulo* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Ângulo de rotação sobre o eixo arbitrário, em radianos. Os ângulos são medidos no sentido anti-horário ao examinar o eixo arbitrário em direção à origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método adiciona a rotação à pilha de matriz com a matriz de rotação computada semelhante à seguinte:


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



Como a rotação é multiplicada à esquerda na pilha de matriz, a rotação é relativa ao espaço de coordenadas local do objeto.

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

[**ID3DXMATRIXStack::RotateYawPitchRoll**](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateYawPitchRollLocal**](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
