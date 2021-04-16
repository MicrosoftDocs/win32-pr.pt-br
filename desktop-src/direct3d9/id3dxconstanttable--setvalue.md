---
description: Define o conteúdo do buffer para a tabela de constantes.
ms.assetid: 6058795c-fa32-42aa-9a36-af0b7f6eed1d
title: 'Método ID3DXConstantTable:: SetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5e02c43e0d0ad84615650bc0b1c0d5fd5654e38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765227"
---
# <a name="id3dxconstanttablesetvalue-method"></a>Método ID3DXConstantTable:: SetValue

Define o conteúdo do buffer para a tabela de constantes.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetValue(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] LPCVOID           pData,
  [in] UINT              Bytes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.

</dd> <dt>

*hConstant* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para uma constante. Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

*pData* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Buffer que contém dados.

</dd> <dt>

*Bytes* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Tamanho do buffer, em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
