---
description: Recupera o identificador da caneta.
ms.assetid: 27320a2f-1e4a-4d7d-a1f8-5244f4a03415
title: 'Método ITabletCursor:: GetId'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: a7dc053b880c3ebaf4b94ae88a09c85f32f1dd5b8dc335756c8906c9a6f0fb4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938616"
---
# <a name="itabletcursorgetid-method"></a>Método ITabletCursor:: GetId

Recupera o identificador da caneta.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetId(
  [out] CURSOR_ID *pCid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCid* \[ fora\]
</dt> <dd>

O identificador da caneta digitalizadora.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

\_A ID do cursor é definida como um DWORD.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITabletCursor**](itabletcursor.md)
</dt> </dl>

 

 




