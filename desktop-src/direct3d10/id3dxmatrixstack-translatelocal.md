---
description: Método ID3DXMATRIXStack::TranslateLocal (D3DX10.h) – determina o produto da matriz de tradução computada determinada pelos fatores determinados (x, y e z) e a matriz atual.
ms.assetid: 96399801-dd80-4e9a-a5c3-c5d41eb9368a
title: Método ID3DXMATRIXStack::TranslateLocal (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.TranslateLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 88a70c9d8b57663e393d6eecb736a19e203e8f186d56e8b47042e30743664861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028676"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx10h"></a>Método ID3DXMATRIXStack::TranslateLocal (D3DX10.h)

Determina o produto da matriz de tradução computada determinada pelos fatores determinados (x, y e z) e a matriz atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TranslateLocal(
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

O fator de tradução na direção x.

</dd> <dt>

*y* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

O fator de tradução na direção y.

</dd> <dt>

*z* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

O fator de tradução na direção z.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK.

## <a name="remarks"></a>Comentários

Esse método multiplica à esquerda a matriz atual com a matriz de tradução computada (a transformação é sobre a origem local do objeto).


```
D3DXMATRIX tmp;
D3DXMatrixTranslation(&tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
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

 

 
