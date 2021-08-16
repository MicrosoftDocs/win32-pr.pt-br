---
description: Recupera o próximo objeto de nível superior no arquivo do DirectX. Preterido.
ms.assetid: 91cd3205-5603-4a62-aab2-7ef4adb9e6d1
title: 'Método IDirectXFileEnumObject:: GetNextDataObject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetNextDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 42d95fcee1b431f5121389d7bb6595e5c53ca56298c75ed6010ee86733c310e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985126"
---
# <a name="idirectxfileenumobjectgetnextdataobject-method"></a>Método IDirectXFileEnumObject:: GetNextDataObject

Recupera o próximo objeto de nível superior no arquivo do DirectX. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNextDataObject(
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppDataObj* \[ fora\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Endereço de um ponteiro para uma interface [**IDirectXFileData**](idirectxfiledata.md) , que representa o objeto de dados de arquivo retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS

## <a name="remarks"></a>Comentários

Os objetos de nível superior são sempre objetos de dados. Objetos de referência de dados e objetos binários só podem ser filhos de objetos de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileEnumObject](idirectxfileenumobject.md)
</dt> </dl>

 

 




