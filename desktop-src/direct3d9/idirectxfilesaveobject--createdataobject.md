---
description: Cria um objeto de dados. Preterido.
ms.assetid: bb0ef2cf-db76-40f6-968f-3599c58459a7
title: 'Método IDirectXFileSaveObject:: createdataobject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.CreateDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 7c5a67a72f6ff5a63730167d2fe2d12213a9ab72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298584"
---
# <a name="idirectxfilesaveobjectcreatedataobject-method"></a>Método IDirectXFileSaveObject:: createdataobject

Cria um objeto de dados. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateDataObject(
  [in]                REFGUID           rguidTemplate,
  [in]                LPCSTR            szName,
  [in]          const GUID              *pguid,
  [in]                DWORD             cbSize,
  [in]                LPVOID            pvData,
  [out, retval]       LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rguidTemplate* \[ no\]
</dt> <dd>

Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

GUID que representa o modelo do objeto de dados.

</dd> <dt>

*szName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para o nome do objeto de dados. Especifique **NULL** se o objeto não tiver um nome.

</dd> <dt>

*pGuid* \[ no\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Ponteiro para um GUID que representa o objeto de dados. Especifique **NULL** se o objeto não tiver um GUID.

</dd> <dt>

*cbSize* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Tamanho do objeto de dados, em bytes.

</dd> <dt>

*pvData* \[ no\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ponteiro para um buffer que contém todos os dados do membro necessário.

</dd> <dt>

*ppDataObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Endereço de um ponteiro para uma interface [**IDirectXFileData**](idirectxfiledata.md) , que representa o objeto de dados de arquivo criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser um dos valores a seguir. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Comentários

Se um objeto de referência de dados fizer referência ao objeto de dados, o parâmetro szName ou pGuid deverá ser não **nulo**.

Salve todos os modelos usando o método [**IDirectXFileSaveObject:: SaveTemplates**](idirectxfilesaveobject--savetemplates.md) antes de salvar os dados criados por esse método. Salve os dados criados usando o método [**IDirectXFileSaveObject:: SaveData**](idirectxfilesaveobject--savedata.md) .

Se você precisar salvar dados opcionais, use o método [**IDirectXFileData:: Adddataobject**](idirectxfiledata--adddataobject.md) depois de usar esse método e antes de usar [**IDirectXFileSaveObject:: SaveData**](idirectxfilesaveobject--savedata.md). Se o objeto tiver objetos filho, adicione-os antes de chamar **IDirectXFileSaveObject:: SaveData**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> <dt>

[**IDirectXFileData:: adddataobject**](idirectxfiledata--adddataobject.md)
</dt> <dt>

[**IDirectXFileSaveObject:: SaveData**](idirectxfilesaveobject--savedata.md)
</dt> <dt>

[**IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md)
</dt> </dl>

 

 
