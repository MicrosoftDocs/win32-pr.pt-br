---
description: Método ID3DXMATRIXStack::Scale (D3DX10.h) – dimensione a matriz atual sobre a origem da coordenada mundial.
ms.assetid: d0f4b341-b3b6-42e4-84df-78f203c3728e
title: Método ID3DXMATRIXStack::Scale (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Scale
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 788c26f129bbd5078a63827653f0ec9b053321f1ca609f6cb1bda032f37c371c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461486"
---
# <a name="id3dxmatrixstackscale-method-d3dx10h"></a>Método ID3DXMATRIXStack::Scale (D3DX10.h)

Dimensione a matriz atual sobre a origem da coordenada do mundo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*x* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

O componente de dimensionamento na direção x.

</dd> <dt>

*y* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

O componente de dimensionamento na direção y.

</dd> <dt>

*z* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

O componente de dimensionamento na direção z.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK.

## <a name="remarks"></a>Comentários

Esse método multiplica à direita a matriz atual com a matriz de escala computada. A transformação é sobre a origem do mundo atual.


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



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

 

 
