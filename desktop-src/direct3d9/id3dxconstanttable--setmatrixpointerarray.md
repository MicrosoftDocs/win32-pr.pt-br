---
description: Método ID3DXConstantTable::SetMatrixPointerArray – define uma matriz de ponteiros para matrizes não transpostas.
ms.assetid: 1b985e03-b5cb-48e5-969f-115ca165acdc
title: Método ID3DXConstantTable::SetMatrixPointerArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixPointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 766f9f51baeaa7d3f210be96bfec5e7638123b8519a92314d79503b04a0908a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118756"
---
# <a name="id3dxconstanttablesetmatrixpointerarray-method"></a>Método ID3DXConstantTable::SetMatrixPointerArray

Define uma matriz de ponteiros para matrizes não transpostas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMatrixPointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa o dispositivo associado à tabela constante.

</dd> <dt>

*hConstant* \[ Em\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para uma matriz de matrizes constantes. Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).

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

Uma matriz nãotransposta contém dados de linha principal; ou seja, cada vetor está contido em uma linha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
