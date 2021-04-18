---
description: Recupera o próximo objeto de dados filho, objeto de referência de dados ou objeto binário no arquivo do DirectX. Preterido.
ms.assetid: 8232e911-6552-4b2b-a9c2-59e6a13a0d9b
title: 'Método IDirectXFileData:: GetNextObject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetNextObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e03351068cdc4f8fca28c612b7bb4c546125a4cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814175"
---
# <a name="idirectxfiledatagetnextobject-method"></a>Método IDirectXFileData:: GetNextObject

Recupera o próximo objeto de dados filho, objeto de referência de dados ou objeto binário no arquivo do DirectX. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNextObject(
  [out, retval] LPDIRECTXFILEOBJECT *ppChildObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppChildObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***

Endereço de um ponteiro para uma interface [**IDirectXFileObject**](idirectxfileobject.md) , que representa a interface de objeto de arquivo do objeto filho retornado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS.

## <a name="remarks"></a>Comentários

Para determinar o tipo de objeto recuperado, use QueryInterface para consultar o objeto recuperado para oferecer suporte às interfaces [**IDirectXFileData**](idirectxfiledata.md), [**IDirectXFileDataReference**](idirectxfiledatareference.md)ou [**IDirectXFileBinary**](idirectxfilebinary.md) . A interface suportada indica o tipo de objeto (dados, referência de dados ou binário).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDirectXFileBinary**](idirectxfilebinary.md)
</dt> <dt>

[**IDirectXFileData**](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileDataReference**](idirectxfiledatareference.md)
</dt> </dl>

 

 




