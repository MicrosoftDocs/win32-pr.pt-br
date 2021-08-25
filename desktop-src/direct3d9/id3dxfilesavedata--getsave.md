---
description: Recupera um ponteiro para este nó de dados do arquivo ID3DXFileSaveObject.
ms.assetid: 092d1c6f-0a53-4b8e-84ec-bc76f3f647ac
title: 'Método ID3DXFileSaveData:: getsave (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetSave
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 05b30c34f7e9d1383270c06ee70aca63d3f24b0f4f721d6859366794f2df361a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856636"
---
# <a name="id3dxfilesavedatagetsave-method"></a>Método ID3DXFileSaveData:: getsave

Recupera um ponteiro para este nó de dados do arquivo [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSave(
  [out] ID3DXFileSaveObject **ppObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppObj* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Endereço de um ponteiro para uma interface [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) que representa esse nó de dados de arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




