---
description: Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.
ms.assetid: 90837762-9bfe-4065-94b3-1ca61184a78e
title: 'Método ID3DXMATRIXStack:: RotateAxisLocal (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5b00e1fd5b678d89d6b5ca4680499f6fde723c12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760246"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx10h"></a>Método ID3DXMATRIXStack:: RotateAxisLocal (D3DX10. h)

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

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para o eixo arbitrário de rotação. Consulte [**D3DXVECTOR3**](d3d10-d3dxvector3.md).

</dd> <dt>

*Ângulo* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Ângulo de rotação sobre o eixo arbitrário, em radianos. Os ângulos são medidos no sentido anti-horário ao examinar o eixo arbitrário em direção à origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
