---
description: Salva um objeto de dados e seus filhos em um arquivo do DirectX. Preterido.
ms.assetid: 18bd5ef6-9e17-4c21-bc14-373de8df9ffb
title: 'Método IDirectXFileSaveObject:: SaveData (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: cb901bd984e1fcd923d0ea172fb5f387b3a9302a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791624"
---
# <a name="idirectxfilesaveobjectsavedata-method"></a>Método IDirectXFileSaveObject:: SaveData

Salva um objeto de dados e seus filhos em um arquivo do DirectX. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SaveData(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDataObj* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**

Ponteiro para uma interface [**IDirectXFileData**](idirectxfiledata.md) , representando o objeto de dados de arquivo a ser salvo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> </dl>

 

 




