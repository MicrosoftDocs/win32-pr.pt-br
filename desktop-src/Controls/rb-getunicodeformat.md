---
title: RB_GETUNICODEFORMAT mensagem (Commctrl.h)
description: RB_GETUNICODEFORMAT mensagem - recupera o sinalizador de formato de caractere Unicode para o controle .
ms.assetid: 48a4472b-dda4-41a2-b5bc-6f74b1cdc70b
keywords:
- RB_GETUNICODEFORMAT controles Windows mensagem
topic_type:
- apiref
api_name:
- RB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe1fd66ce5a6c4052543ee925011057e592375fa64b2841147e7bf97831a2302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409399"
---
# <a name="rb_getunicodeformat-message"></a>Mensagem \_ GETUNICODEFORMAT do RB

Recupera o sinalizador de formato de caractere Unicode para o controle .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o sinalizador de formato Unicode para o controle . Se esse valor for diferentes de zero, o controle está usando caracteres Unicode. Se esse valor for zero, o controle está usando caracteres ANSI.

## <a name="remarks"></a>Comentários

Consulte os comentários de [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para uma discussão sobre essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RB \_ SETUNICODEFORMAT**](rb-setunicodeformat.md)
</dt> </dl>

 

 





