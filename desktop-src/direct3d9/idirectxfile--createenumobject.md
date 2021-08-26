---
description: Cria um objeto enumerador. Preterido.
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: Método IDirectXFile::CreateEnumObject (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1af10a0f46877a159ab8c6543fba9c1406d083e6b3f4a57cf1c41b9fb2d92612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985146"
---
# <a name="idirectxfilecreateenumobject-method"></a>Método IDirectXFile::CreateEnumObject

Cria um objeto enumerador. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateEnumObject(
  [in]          LPVOID                  pvSource,
  [in]          DXFILELOADOPTIONS       dwLoadOptions,
  [out, retval] LPDIRECTXFILEENUMOBJECT *ppEnumObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pvSource* \[ Em\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ponteiro para dados cujo conteúdo depende do valor de dwLoadOptions

</dd> <dt>

*dwLoadOptions* \[ Em\]
</dt> <dd>

Tipo: **[ **DXFILELOADOPTIONS**](dxfile.md)**

Valor que especifica a origem dos dados. Esse valor pode ser um dos sinalizadores DXFILELOAD \_ xxx em [Constantes DXFILE](dxfile.md).

</dd> <dt>

*ppEnumObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXF DIGITUMOBJECT**](idirectxfileenumobject.md)\***

Endereço de um ponteiro para uma interface [**IDirectXFileEnumObject,**](idirectxfileenumobject.md) que representa o objeto de enumerador criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: DXFILEERR \_ BADALLOC, \_ DXFILEERR BADFILEFLOATSIZE, \_ \_ \_ \_ DXFILEERR BADFILETYPE, DXFILEERR BADFILEVERSION, DXFILEERR BADRESOURCE, DXFILEERR BADVALUE, DXFILEERR \_ FILENOTFOUND, DXFILEERR \_ RESOURCENOTFOUND, DXFILEERR \_ URLNOTFOUND.

## <a name="remarks"></a>Comentários

Depois de usar esse método, use um dos métodos IDirectXFileEnumObject para recuperar um objeto de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> </dl>

 

 
