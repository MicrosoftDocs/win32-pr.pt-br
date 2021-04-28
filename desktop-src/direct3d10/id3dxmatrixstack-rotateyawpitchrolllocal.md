---
description: 'Método ID3DXMATRIXStack:: RotateYawPitchRollLocal (D3DX10. h) – gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.'
ms.assetid: da023816-5176-460d-ab6b-909b89cc46cd
title: 'Método ID3DXMATRIXStack:: RotateYawPitchRollLocal (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRollLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 726a6d7092b95f53d17625f68884b92d347de3a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107834"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx10h"></a>Método ID3DXMATRIXStack:: RotateYawPitchRollLocal (D3DX10. h)

Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RotateYawPitchRollLocal(
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

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK.

## <a name="remarks"></a>Comentários

Esse método adiciona a rotação à pilha de matriz com a matriz de rotação computada semelhante à seguinte:


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



Como a rotação é multiplicada à esquerda na pilha de matriz, a rotação é relativa ao espaço de coordenadas local do objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
