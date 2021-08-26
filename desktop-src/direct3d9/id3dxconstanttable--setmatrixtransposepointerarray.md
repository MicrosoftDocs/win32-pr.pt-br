---
description: Método ID3DXConstantTable::SetMatrixTransposePointerArray – define uma matriz de ponteiros para matrizes transpostas.
ms.assetid: f2db10cb-a146-412d-8de8-f093253470fd
title: Método ID3DXConstantTable::SetMatrixTransposePointerArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa21e6a19fe3ebb8ea1ee9dfecaa9e7370c5dd412d9dea8599987a55dc1858d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951846"
---
# <a name="id3dxconstanttablesetmatrixtransposepointerarray-method"></a>Método ID3DXConstantTable::SetMatrixTransposePointerArray

Define uma matriz de ponteiros para matrizes transpostas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMatrixTransposePointerArray(
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

Identificador exclusivo para a matriz de constantes de matriz. Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

*ppMatrix* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***

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

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
