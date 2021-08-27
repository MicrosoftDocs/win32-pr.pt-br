---
description: Adiciona um objeto de dados como um filho do objeto ID3DXFileSaveData.
ms.assetid: 710a1588-d766-4555-97a3-4b5a517ce805
title: Método ID3DXFileSaveObject::AddDataObject (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8a1bdea820b90ae68c819ae2755f2abecd892cfd362116f6da37cb643a254048
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802411"
---
# <a name="id3dxfilesaveobjectadddataobject-method"></a>Método ID3DXFileSaveObject::AddDataObject

Adiciona um objeto de dados como um filho do [**objeto ID3DXFileSaveData.**](id3dxfilesavedata.md)

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

*rguidTemplate* \[ Em\]
</dt> <dd>

Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

GUID que representa o modelo do objeto de dados.

</dd> <dt>

*szName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para o nome do objeto de dados. **Especifique NULL** se o objeto não tiver um nome.

</dd> <dt>

*pId* \[ Em\]
</dt> <dd>

Tipo: **const [**GUID**](guid.md) \***

Ponteiro para um GUID que representa o objeto de dados. **Especifique NULL** se o objeto não tiver um GUID.

</dd> <dt>

*cbSize* \[ Em\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Tamanho do objeto de dados, em bytes.

</dd> <dt>

*pvData* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para um buffer que contém todos os dados necessários no objeto de dados.

</dd> <dt>

*ppObj* \[ in, retval\]
</dt> <dd>

Tipo: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***

Endereço de um ponteiro para uma interface [**ID3DXFileSaveData,**](id3dxfilesavedata.md) representando o nó de dados do arquivo ao qual o objeto de dados será adicionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADOBJECT, DXFILEERR \_ BADVALUE, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Se um objeto de referência de dados referenciar o objeto de dados, o parâmetro szName ou pId deverá ser não **NULL.**

Salve os dados criados no disco usando o [**método ID3DXFileSaveObject::Save.**](id3dxfilesaveobject--save.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 
