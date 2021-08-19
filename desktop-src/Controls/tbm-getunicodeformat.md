---
title: TBM_GETUNICODEFORMAT mensagem (Commctrl.h)
description: TBM_GETUNICODEFORMAT mensagem - recupera o sinalizador de formato de caractere Unicode para o controle .
ms.assetid: cecd7e55-f482-4381-bde8-a60b8c5173eb
keywords:
- TBM_GETUNICODEFORMAT controles de Windows mensagem
topic_type:
- apiref
api_name:
- TBM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e15f5b12a60b58958dad1364848120f391c91906bb6057727f3a4e22b8a7813
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046166"
---
# <a name="tbm_getunicodeformat-message"></a>Mensagem \_ TBM GETUNICODEFORMAT

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

[**TBM \_ SETUNICODEFORMAT**](tbm-setunicodeformat.md)
</dt> </dl>

 

 





