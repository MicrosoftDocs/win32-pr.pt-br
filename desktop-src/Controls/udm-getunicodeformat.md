---
title: UDM_GETUNICODEFORMAT mensagem (Commctrl.h)
description: UDM_GETUNICODEFORMAT mensagem - recupera o sinalizador de formato de caractere Unicode para o controle .
ms.assetid: 8c09d37b-95a2-49cd-b578-919f9c39fa8b
keywords:
- UDM_GETUNICODEFORMAT controles de Windows mensagem
topic_type:
- apiref
api_name:
- UDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbce0af6ad559524d7662a0ce386777a5186777a4cb65b4270fc7c4c9bdff70d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957745"
---
# <a name="udm_getunicodeformat-message"></a>Mensagem GETUNICODEFORMAT do UDM \_

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
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**UDM \_ SETUNICODEFORMAT**](udm-setunicodeformat.md)
</dt> </dl>

 

 





