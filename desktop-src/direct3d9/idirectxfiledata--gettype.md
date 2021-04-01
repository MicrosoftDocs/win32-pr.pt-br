---
description: Recupera o GUID do modelo do objeto. Preterido.
ms.assetid: bb4a4a32-a9e7-4caa-869d-24cfb310d8d1
title: 'Método IDirectXFileData:: GetType (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 463391c661b2d166a6fba773e3b01590daf0ebd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091985"
---
# <a name="idirectxfiledatagettype-method"></a>Método IDirectXFileData:: GetType

Recupera o GUID do modelo do objeto. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetType(
  [out, retval] const GUID **ppguid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppguid* \[ out, retval\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* \* const**

Endereço de um ponteiro para receber o GUID do modelo do objeto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser DXFILEERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> </dl>

 

 




