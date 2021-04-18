---
description: Recupera o número de botões na caneta digitalizadora.
ms.assetid: ae4ce670-769a-4f00-b728-285020f09934
title: 'Método ITabletCursor:: GetButtonCount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButtonCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 08fdf24b2a0b69b7830a683786f18fc5df0805b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812115"
---
# <a name="itabletcursorgetbuttoncount-method"></a>Método ITabletCursor:: GetButtonCount

Recupera o número de botões na caneta digitalizadora.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetButtonCount(
  [out] ULONG *pcButtons
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcButtons* \[ fora\]
</dt> <dd>

A contagem de botões na caneta digitalizadora.

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

[**Interface ITabletCursor**](itabletcursor.md)
</dt> </dl>

 

 




