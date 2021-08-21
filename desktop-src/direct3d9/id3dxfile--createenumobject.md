---
description: Cria um objeto enumerador que lerá um arquivo .x.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: Método ID3DXFile::CreateEnumObject (D3DX9Xof.h)
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
ms.openlocfilehash: 528ab441da6cd4370de4ecad5d8490e6e74b5977672d0c7d4126cea1b7bab8fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044394"
---
# <a name="id3dxfilecreateenumobject-method"></a>Método ID3DXFile::CreateEnumObject

Cria um objeto enumerador que lerá um arquivo .x.

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

*pvSource* \[ out\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

A fonte de dados. Ou:

-   Um nome de arquivo
-   Uma [**estrutura \_ FILELOADMEMORY D3DXF**](d3dxf-fileloadmemory.md)
-   Uma [**estrutura \_ FILELOADRESOURCE D3DXF**](d3dxf-fileloadresource.md)

Dependendo do valor de loadflags.

</dd> <dt>

*loadflags* \[ Em\]
</dt> <dd>

Tipo: **[ \_ FILELOADOPTIONS D3DXF](d3dxf.md)**

Valor que especifica a origem dos dados. Esse valor pode ser um dos sinalizadores [ \_ FILELOADOPTIONS D3DXF.](d3dxf.md)

</dd> <dt>

*ppEnumObj* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Endereço de um ponteiro para uma interface [**ID3DXFileEnumObject,**](id3dxfileenumobject.md) que representa o objeto de enumerador criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Comentários

Depois de usar esse método, use um dos métodos [**ID3DXFileEnumObject**](id3dxfileenumobject.md) para recuperar um objeto de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileEnumObject**](id3dxfileenumobject.md)
</dt> </dl>

 

 
