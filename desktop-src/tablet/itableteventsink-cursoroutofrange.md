---
description: Ocorre quando a caneta sai do intervalo de detecção física (proximidade) do tablet.
ms.assetid: ded01278-126d-415d-9a7b-1e6fe3650a37
title: Método ITabletEventSink::CursorOutOfRange
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorOutOfRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 215ab448d573f83222d04547c4dccbeb88d7fe7c4358b3cca0ed09e936e286d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041668"
---
# <a name="itableteventsinkcursoroutofrange-method"></a>Método ITabletEventSink::CursorOutOfRange

Ocorre quando a caneta sai do intervalo de detecção física (proximidade) do tablet.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CursorOutOfRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tcid* \[ Em\]
</dt> <dd>

O identificador do tablet.

</dd> <dt>

*Cid* 
</dt> <dd>

O identificador da caneta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITabletEventSink Interface**](itableteventsink.md)
</dt> </dl>

 

 




