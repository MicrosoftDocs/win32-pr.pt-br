---
description: 'Método ID3DXTextureShader:: SetFloatArray – define uma matriz de números de ponto flutuante.'
ms.assetid: 8e64b569-a6bf-4925-9d21-4df0b6661ee2
title: 'Método ID3DXTextureShader:: SetFloatArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd42455e16cbfc203f76de868a82935e0e25401f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090244"
---
# <a name="id3dxtextureshadersetfloatarray-method"></a>Método ID3DXTextureShader:: SetFloatArray

Define uma matriz de números de ponto flutuante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hConstant,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hConstant* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para a matriz de constantes. Consulte [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*PF* \[ no\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Matriz de números de ponto flutuante.

</dd> <dt>

*Contagem* \[ de no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de valores de ponto flutuante na matriz.

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

 

 
