---
description: Recupera um ponteiro para o GUID que identifica um objeto de arquivo DirectX. Preterido.
ms.assetid: 74c7a1d9-85e4-43eb-bcd8-1f3ddd713e9f
title: Método IDirectXFileObject::GetId (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetId
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 5cb6788afe0b937822b8895790584f6928a7b5aecb564a31540337935763b2f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800170"
---
# <a name="idirectxfileobjectgetid-method"></a>Método IDirectXFileObject::GetId

Recupera um ponteiro para o GUID que identifica um objeto de arquivo DirectX. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetId(
  [out, retval] 
            LPGUID pGuid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGuid* \[ out, retval\]
</dt> <dd>

Tipo: **LPGUID**

Ponteiro para um GUID para receber a ID do objeto. A função definirá o GUID como um GUID **NULO** se o objeto não tiver uma ID.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser DXFILEERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileObject](idirectxfileobject.md)
</dt> </dl>

 

 




