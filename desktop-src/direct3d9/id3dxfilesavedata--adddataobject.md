---
description: Adiciona um objeto de dados como um filho do nó de dados do arquivo ID3DXFileSaveData.
ms.assetid: 47faad99-3ee8-4ca8-b8d7-413d4cd5b090
title: 'Método ID3DXFileSaveData:: adddataobject (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ed4b0abd35f9f53fb2111f40903e4b2b81a75c9d402a53fbb2fdb1cdc9a75750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847836"
---
# <a name="id3dxfilesavedataadddataobject-method"></a>Método ID3DXFileSaveData:: adddataobject

Adiciona um objeto de dados como um filho do nó de dados do arquivo [**ID3DXFileSaveData**](id3dxfilesavedata.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddDataObject(
  [in]               REFGUID           rguidTemplate,
  [in]               LPCSTR            szName,
  [in]         const GUID              *pId,
  [in]               SIZE_T            cbSize,
  [in]               LPCVOID           pvData,
  [in, retval]       ID3DXFileSaveData **ppObj
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

Ponteiro para o nome do objeto de dados a ser adicionado. Especifique **NULL** se o objeto não tiver um nome.

</dd> <dt>

*pid* \[ no\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Ponteiro para um GUID que representa o objeto de dados. O objeto de dados deve ter sido registrado com [**ID3DXFile:: RegisterTemplates**](id3dxfile--registertemplates.md) ou [**ID3DXFile:: RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md). Especifique **NULL** se o objeto não tiver um GUID.

</dd> <dt>

*cbSize* \[ no\]
</dt> <dd>

Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**

Tamanho do objeto de dados, em bytes.

</dd> <dt>

*pvData* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para um buffer que contém todos os dados necessários no objeto de dados.

</dd> <dt>

*ppObj* \[ no, retval\]
</dt> <dd>

Tipo: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***

Endereço de um ponteiro para uma interface [**ID3DXFileSaveData**](id3dxfilesavedata.md) , que representa o nó de dados do arquivo ao qual o objeto de dados será adicionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
