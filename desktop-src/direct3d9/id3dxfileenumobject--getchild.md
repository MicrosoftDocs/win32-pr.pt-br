---
description: 'Método ID3DXFileEnumObject:: GetChild – recupera um objeto filho neste objeto de dados de arquivo.'
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: 'Método ID3DXFileEnumObject:: GetChild (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 20075c0e30985ab4f5c7c691b40caf302db98d6b5c8cf863fd9c57fca895ee40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802789"
---
# <a name="id3dxfileenumobjectgetchild-method"></a>Método ID3DXFileEnumObject:: GetChild

Recupera um objeto filho neste objeto de dados de arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ID* \[ em\]
</dt> <dd>

Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**

ID do objeto filho a ser recuperado.

</dd> <dt>

*ppObj* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Endereço de um ponteiro para receber o ponteiro de interface do objeto filho.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
