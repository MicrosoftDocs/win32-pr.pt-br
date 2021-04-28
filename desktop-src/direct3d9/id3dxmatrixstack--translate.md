---
description: 'Método ID3DXMATRIXStack:: translate (D3dx9math. h) – determina o produto da matriz atual e a matriz de conversão computada determinada pelos fatores especificados (x, y e z).'
ms.assetid: e0ac72a2-9970-433e-9026-aa79edc8261c
title: 'Método ID3DXMATRIXStack:: translate (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Translate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7fadad95e8e72691a0e030ed89eedc745de2be43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093334"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a>Método ID3DXMATRIXStack:: translate (D3dx9math. h)

Determina o produto da matriz atual e a matriz de conversão computada determinada pelos fatores especificados (x, y e z).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Translate(
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

O fator de conversão na direção x.

</dd> <dt>

*y* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

O fator de conversão na direção y.

</dd> <dt>

*z* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

O fator de conversão na direção z.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK.

## <a name="remarks"></a>Comentários

Esse método multiplica a matriz atual pela matriz de conversão computada (a transformação é sobre a origem do mundo atual).


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
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

[**ID3DXMATRIXStack::TranslateLocal**](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
