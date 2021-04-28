---
description: 'Método ID3DXMATRIXStack:: ScaleLocal (D3dx9math. h) – dimensione a matriz atual sobre a origem do objeto.'
ms.assetid: fe71da67-c8c9-4c78-9055-9bc3cadc0780
title: 'Método ID3DXMATRIXStack:: ScaleLocal (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.ScaleLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5bd9f47b6c38b5ec72bcd25ecb5981859a87038b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093324"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx9mathh"></a>Método ID3DXMATRIXStack:: ScaleLocal (D3dx9math. h)

Dimensione a matriz atual sobre a origem do objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*x* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

O componente de dimensionamento na direção x.

</dd> <dt>

*y* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

O componente de dimensionamento na direção y.

</dd> <dt>

*z* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

O componente de dimensionamento na direção z.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK.

## <a name="remarks"></a>Comentários

Esse método multiplica a matriz atual pela matriz de escala computada. A transformação é sobre a origem local do objeto.


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Scale**](id3dxmatrixstack--scale.md)
</dt> </dl>

 

 
