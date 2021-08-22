---
description: 'Método ID3DXMATRIXStack:: TranslateLocal (D3dx9math. h) – determina o produto da matriz de conversão computada determinada pelos fatores especificados (x, y e z) e a matriz atual.'
ms.assetid: d4752a6c-2114-4016-a69f-dcc561d2c76b
title: 'Método ID3DXMATRIXStack:: TranslateLocal (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39984fa20ab0fa84d9b22b86fade2eb59277dd6a919c5bfa8d8a52efd33b1cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493116"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx9mathh"></a>Método ID3DXMATRIXStack:: TranslateLocal (D3dx9math. h)

Determina o produto da matriz de conversão computada determinada pelos fatores especificados (x, y e z) e a matriz atual.

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

Esse método multiplica a matriz atual pela matriz de conversão computada (a transformação é sobre a origem local do objeto).


```
    
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack:: translate**](id3dxmatrixstack--translate.md)
</dt> </dl>

 

 
