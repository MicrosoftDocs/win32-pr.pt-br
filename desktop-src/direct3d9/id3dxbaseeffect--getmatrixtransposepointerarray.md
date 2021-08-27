---
description: Obtém uma matriz de ponteiros para matrizes transpostas.
ms.assetid: b859ff2f-cf62-4619-b8be-b940fa0513b3
title: Método ID3DXBaseEffect::GetMatrixTransposePointerArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposePointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 42014ed5a829f6dc0d45d7fe0dbcc96f52e945d47ae02b8effd217329e92bda8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118826"
---
# <a name="id3dxbaseeffectgetmatrixtransposepointerarray-method"></a>Método ID3DXBaseEffect::GetMatrixTransposePointerArray

Obtém uma matriz de ponteiros para matrizes transpostas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMatrixTransposePointerArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX **ppMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hParameter* \[ Em\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*ppMatrix* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\*\***

Matriz de ponteiros para matrizes transpostas. Consulte [**D3DXMATRIX**](d3dxmatrix.md).

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

Uma matriz transposta contém dados de coluna principal; ou seja, cada vetor está contido em uma coluna.

Se as matrizes de destino são maiores que as matrizes de origem, somente os componentes superiores esquerdos de cada matriz de destino serão preenchidos e os componentes restantes da matriz de destino serão definidos como zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetMatrixTransposeArray**](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
