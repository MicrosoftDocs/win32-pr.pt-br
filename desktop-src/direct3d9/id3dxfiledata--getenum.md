---
description: Recupera o objeto de enumeração neste objeto de dados de arquivo.
ms.assetid: 383560e2-1888-4e37-9883-2ddbcb101cf6
title: 'Método ID3DXFileData:: getenum (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetEnum
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7dd565f6f76d42159d77d8b83c638c75648f293b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798526"
---
# <a name="id3dxfiledatagetenum-method"></a>Método ID3DXFileData:: getenum

Recupera o objeto de enumeração neste objeto de dados de arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetEnum(
  [in] ID3DXFileEnumObject **ppObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppObj* \[ no\]
</dt> <dd>

Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Endereço de um ponteiro para receber o objeto de enumeração neste objeto de dados de arquivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 




