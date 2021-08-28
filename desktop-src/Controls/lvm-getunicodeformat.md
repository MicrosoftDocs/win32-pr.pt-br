---
title: LVM_GETUNICODEFORMAT mensagem (Commctrl.h)
description: Recupera o sinalizador de formato de caractere UNICODE para o controle . Você pode enviar essa mensagem explicitamente ou usar a \_ macro ListView GetUnicodeFormat.
ms.assetid: b0598b60-4d0e-4c68-b63a-e614c6268129
keywords:
- LVM_GETUNICODEFORMAT controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3166d7349bf138fa853523c019a4c1db86e3f1a2d81a6da86c4ef25b5ed405
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019254"
---
# <a name="lvm_getunicodeformat-message"></a>Mensagem GETUNICODEFORMAT do LVM \_

Recupera o sinalizador de formato de caractere UNICODE para o controle . Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ ListView GetUnicodeFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat)

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
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LVM \_ SETUNICODEFORMAT**](lvm-setunicodeformat.md)
</dt> </dl>

 

 





