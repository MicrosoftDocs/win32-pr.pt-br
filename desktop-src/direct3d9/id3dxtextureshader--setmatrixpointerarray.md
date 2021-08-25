---
description: Define uma matriz de ponteiros para matrizes não transpostas.
ms.assetid: 5ad83abd-1895-4838-85b5-c437c23a3d91
title: Método ID3DXTextureShader::SetMatrixPointerArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixPointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f5e8ba498d089a6d5b947cf908982d7e19af17126aa7414d49d2cd1d9d0a4f92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847026"
---
# <a name="id3dxtextureshadersetmatrixpointerarray-method"></a>Método ID3DXTextureShader::SetMatrixPointerArray

Define uma matriz de ponteiros para matrizes não transpostas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hConstant* \[ Em\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para uma matriz de matrizes constantes. Consulte [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*ppMatrix* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***

Matriz de ponteiros para matrizes não transpostas. Consulte [**D3DXMATRIX**](d3dxmatrix.md).

</dd> <dt>

*Contagem* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de matrizes na matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Uma matriz não transposta contém dados de linha principal; ou seja, cada vetor está contido em uma linha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
