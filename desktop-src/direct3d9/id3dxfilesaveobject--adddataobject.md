---
description: Adiciona um objeto de dados como um filho do objeto ID3DXFileSaveData.
ms.assetid: 710a1588-d766-4555-97a3-4b5a517ce805
title: 'Método ID3DXFileSaveObject:: adddataobject (D3DX9Xof. h)'
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
ms.openlocfilehash: d1586035a0d8a81c2210009bad903aac5197bcf7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798189"
---
# <a name="id3dxfilesaveobjectadddataobject-method"></a>Método ID3DXFileSaveObject:: adddataobject

Adiciona um objeto de dados como um filho do objeto [**ID3DXFileSaveData**](id3dxfilesavedata.md) .

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

Ponteiro para o nome do objeto de dados. Especifique **NULL** se o objeto não tiver um nome.

</dd> <dt>

*pid* \[ no\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Ponteiro para um GUID que representa o objeto de dados. Especifique **NULL** se o objeto não tiver um GUID.

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

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADOBJECT, DXFILEERR \_ BADVALUE, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Se um objeto de referência de dados fizer referência ao objeto de dados, o parâmetro szName ou pId deverá ser não **nulo**.

Salve os dados criados no disco usando o método [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 
