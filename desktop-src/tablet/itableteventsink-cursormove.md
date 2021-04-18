---
description: Ocorre quando o cursor se move sobre o digitalizador digitalizador.
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: 'Método ITabletEventSink:: CursorMove'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorMove
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f6950e0b30c1b8fc8ccf3e60a8aaa05b9eeb3215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788136"
---
# <a name="itableteventsinkcursormove-method"></a>Método ITabletEventSink:: CursorMove

Ocorre quando o cursor se move sobre o digitalizador digitalizador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CursorMove(
   TABLET_CONTEXT_ID tcid,
   CURSOR_ID         cid,
   HWND              hWnd,
   LONG              xPos,
   LONG              yPos
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tcid* 
</dt> <dd>

Dentifier exclusivo do digitalizador do Tablet.

</dd> <dt>

*CID* 
</dt> <dd>

Identificador exclusivo da caneta digitalizadora.

</dd> <dt>

*hWnd* 
</dt> <dd>

A janela sobre a qual o cursor foi movido.

</dd> <dt>

*xPos* 
</dt> <dd>

A posição X da caneta.

</dd> <dt>

*yPos* 
</dt> <dd>

A posição Y da caneta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




