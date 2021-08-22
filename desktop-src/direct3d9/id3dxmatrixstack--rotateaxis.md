---
description: Método ID3DXMATRIXStack::RotateAxis (D3dx9math.h) – gira (em relação ao espaço de coordenadas do mundo) em torno de um eixo arbitrário.
ms.assetid: b7ae5195-a2af-429f-9a0d-51cd7e955362
title: Método ID3DXMATRIXStack::RotateAxis (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6f0009eb3f6b0a2f05a76cb51261712b8b5744bff9bcc28f55449deb5d854b8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606996"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx9mathh"></a>Método ID3DXMATRIXStack::RotateAxis (D3dx9math.h)

Gira (em relação ao espaço de coordenadas do mundo) em torno de um eixo arbitrário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pV* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para o eixo arbitrário de rotação. Consulte [**D3DXVECTOR3**](d3dxvector3.md).

</dd> <dt>

*Ângulo* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ângulo de rotação sobre o eixo arbitrário, em radianos. Os ângulos são medidos no sentido anti-horário ao olhar ao longo do eixo arbitrário em direção à origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método adiciona a rotação à pilha de matrizes com a matriz de rotação computada semelhante à seguinte:


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



Como a rotação é multiplicada à direita para a pilha de matriz, a rotação é relativa ao espaço de coordenadas do mundo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateAxisLocal**](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateYawPitchRoll**](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateYawPitchRollLocal**](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
