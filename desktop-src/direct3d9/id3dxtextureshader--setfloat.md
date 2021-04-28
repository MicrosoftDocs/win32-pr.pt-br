---
description: 'Método ID3DXTextureShader:: SetFloat – define um número de ponto flutuante.'
ms.assetid: 69bb9b15-5d66-4b1a-9559-29bcb38a965f
title: 'Método ID3DXTextureShader:: SetFloat (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6230b0736cb3bc623b0413f7b5a1cb9635f00e07
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107164"
---
# <a name="id3dxtextureshadersetfloat-method"></a>Método ID3DXTextureShader:: SetFloat

Define um número de ponto flutuante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hConstant,
  [in] FLOAT      f
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hConstant* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para a constante. Consulte [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*f* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Número de ponto flutuante.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
