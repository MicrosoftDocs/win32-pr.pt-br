---
description: Cria um objeto enumerador que lerá um arquivo. x.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: 'Método ID3DXFile:: createenumobject (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a58a3341bacf9b323cc5753f8e9e51c4b703b966
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790312"
---
# <a name="id3dxfilecreateenumobject-method"></a>Método ID3DXFile:: createenumobject

Cria um objeto enumerador que lerá um arquivo. x.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateEnumObject(
  [out] LPCVOID               pvSource,
  [in]  D3DXF_FILELOADOPTIONS loadflags,
  [out] ID3DXFileEnumObject   **ppEnumObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pvSource* \[ fora\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

A fonte de dados. Ou:

-   Um nome de arquivo
-   Uma estrutura [**D3DXF \_ FILELOADMEMORY**](d3dxf-fileloadmemory.md)
-   Uma estrutura [**D3DXF \_ FILELOADRESOURCE**](d3dxf-fileloadresource.md)

Dependendo do valor de LoadFlags.

</dd> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Tipo: **[D3DXF \_ fileloadoptions](d3dxf.md)**

Valor que especifica a origem dos dados. Esse valor pode ser um dos sinalizadores [D3DXF \_ fileloadoptions](d3dxf.md) .

</dd> <dt>

*ppEnumObj* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Endereço de um ponteiro para uma interface [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , que representa o objeto enumerador criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Comentários

Depois de usar esse método, use um dos métodos [**ID3DXFileEnumObject**](id3dxfileenumobject.md) para recuperar um objeto de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileEnumObject**](id3dxfileenumobject.md)
</dt> </dl>

 

 
