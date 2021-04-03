---
description: Recupera o objeto ID3DXFile.
ms.assetid: 832878c6-73a4-400a-af30-57112b172977
title: 'Método ID3DXFileEnumObject:: GetFile (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d3b5d672ca9b462e08c75a6f3352b01b07ead43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930650"
---
# <a name="id3dxfileenumobjectgetfile-method"></a>Método ID3DXFileEnumObject:: GetFile

Recupera o objeto [**ID3DXFile**](id3dxfile.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFile(
  [out] ID3DXFile **ppFile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppFile* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3DXFile**](id3dxfile.md)\*\***

Endereço de um ponteiro para uma interface [**ID3DXFile**](id3dxfile.md) , que representa o objeto retornado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 




