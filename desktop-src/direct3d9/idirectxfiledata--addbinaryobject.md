---
description: Cria um objeto binário e o adiciona como um objeto filho. Preterido.
ms.assetid: 6164951d-dd87-4318-ac08-b97c22f58d45
title: 'Método IDirectXFileData:: addbinaryobject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddBinaryObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3d619fde6cd5d22f161188d46f710caeadfaedba2fbcf1167486e05dee539fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728972"
---
# <a name="idirectxfiledataaddbinaryobject-method"></a>Método IDirectXFileData:: addbinaryobject

Cria um objeto binário e o adiciona como um objeto filho. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddBinaryObject(
  [in]       LPCSTR szName,
  [in] const GUID   *pguid,
  [in]       LPCSTR szMimeType,
  [in]       LPVOID pvData,
  [in]       DWORD  cbSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para o nome do objeto. Especifique **NULL** se o objeto não precisar de um nome.

</dd> <dt>

*pGuid* \[ no\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Ponteiro para o GUID que representa o objeto. Especifique **NULL** se o objeto não precisar de um GUID.

</dd> <dt>

*szMimeType* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para o tipo MIME do objeto.

</dd> <dt>

*pvData* \[ no\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ponteiro para os dados do objeto.

</dd> <dt>

*cbSize* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Tamanho do buffer apontado por pvData, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser um dos valores a seguir. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileBinary:: getMimeType**](idirectxfilebinary--getmimetype.md)
</dt> </dl>

 

 
