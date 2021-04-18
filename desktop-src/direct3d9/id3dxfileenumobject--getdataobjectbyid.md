---
description: Recupera o objeto de dados que tem o GUID especificado.
ms.assetid: c3d598bd-0646-4f99-8517-4475ef7cd8c9
title: 'Método ID3DXFileEnumObject:: GetDataObjectById (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 82a74ca4ff472d678ded92aa01f2c2406560955e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788712"
---
# <a name="id3dxfileenumobjectgetdataobjectbyid-method"></a>Método ID3DXFileEnumObject:: GetDataObjectById

Recupera o objeto de dados que tem o GUID especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID        rguid,
  [out] LPD3DXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rguid* \[ no\]
</dt> <dd>

Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

Referência ao GUID solicitado.

</dd> <dt>

*ppDataObj* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)\***

Endereço de um ponteiro para uma interface [**ID3DXFileData**](id3dxfiledata.md) , que representa o objeto de dados de arquivo retornado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: DXFILEERR \_ BADVALUE, DXFILEERR não \_ encontrado.

## <a name="remarks"></a>Comentários

Obtenha o rguid do GUID do objeto de dados do arquivo atual com o método [**ID3DXFileData:: GetID**](id3dxfiledata--getid.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
