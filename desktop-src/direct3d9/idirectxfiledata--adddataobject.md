---
description: Adiciona um objeto de dados como um objeto filho. Preterido.
ms.assetid: 43771dd6-c17f-4376-9b0a-459ba61ff4c5
title: 'Método IDirectXFileData:: adddataobject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: db11f5f3c0d9078663c87db8948bc483ab05d229cd4d7fd0950efaf5143e1408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491826"
---
# <a name="idirectxfiledataadddataobject-method"></a>Método IDirectXFileData:: adddataobject

Adiciona um objeto de dados como um objeto filho. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddDataObject(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDataObj* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**

Ponteiro para uma interface [**IDirectXFileData**](idirectxfiledata.md) , representando o objeto de dados de arquivo a ser adicionado como um objeto filho.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser um dos valores a seguir. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Comentários

Use o método [**IDirectXFileSaveObject:: Createdataobject**](idirectxfilesaveobject--createdataobject.md) para criar o objeto [**IDirectXFileData**](idirectxfiledata.md) antes de chamar esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileSaveObject:: createdataobject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 




