---
title: Mensagem de UDM_GETUNICODEFORMAT (commctrl. h)
description: Mensagem de UDM_GETUNICODEFORMAT-recupera o sinalizador de formato de caractere Unicode para o controle.
ms.assetid: 8c09d37b-95a2-49cd-b578-919f9c39fa8b
keywords:
- Controles de UDM_GETUNICODEFORMAT de mensagens do Windows
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
ms.openlocfilehash: 273164df7f7021f39ec26a22eb637e8b9969fc24
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113585"
---
# <a name="udm_getunicodeformat-message"></a>\_Mensagem de GETUNICODEFORMAT UDM

Recupera o sinalizador de formato de caractere Unicode para o controle.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o sinalizador de formato Unicode para o controle. Se esse valor for diferente de zero, o controle estará usando caracteres Unicode. Se esse valor for zero, o controle estará usando caracteres ANSI.

## <a name="remarks"></a>Comentários

Consulte os comentários para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para uma discussão sobre esta mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_SETUNICODEFORMAT UDM**](udm-setunicodeformat.md)
</dt> </dl>

 

 





