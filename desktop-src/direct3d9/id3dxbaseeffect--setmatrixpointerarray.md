---
description: 'Método ID3DXBaseEffect:: SetMatrixPointerArray – define uma matriz de ponteiros para matrizes nontransposed.'
ms.assetid: f2e62470-6882-49d8-ae12-6c5b79dd5c99
title: 'Método ID3DXBaseEffect:: SetMatrixPointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cfe30e0132cfa237ddbccc24758b35e102a62b0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093764"
---
# <a name="id3dxbaseeffectsetmatrixpointerarray-method"></a>Método ID3DXBaseEffect:: SetMatrixPointerArray

Define uma matriz de ponteiros para matrizes nontransposed.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hParameter* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*ppMatrix* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***

Matriz de ponteiros para matrizes nontransposed. Consulte [**D3DXMATRIX**](d3dxmatrix.md).

</dd> <dt>

*Contagem* \[ de no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de matrizes na matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Uma matriz nontransposed contém dados de linha principal; ou seja, cada vetor está contido em uma linha.

Se as matrizes de destino forem menores do que as matrizes de origem, os componentes adicionais das matrizes de origem serão ignorados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetMatrixArray**](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
