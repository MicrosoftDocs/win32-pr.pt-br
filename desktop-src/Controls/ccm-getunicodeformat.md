---
title: CCM_GETUNICODEFORMAT mensagem (Commctrl.h)
description: Obtém o sinalizador de formato de caractere Unicode para o controle .
ms.assetid: 8a23cd1c-549e-4d48-891a-b37dbf5c524b
keywords:
- CCM_GETUNICODEFORMAT controles de Windows mensagem
topic_type:
- apiref
api_name:
- CCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa115ba341478990b46600bc76ee02e4ecf750d5a7ccde9f1110aa8856d30fa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119438276"
---
# <a name="ccm_getunicodeformat-message"></a>Mensagem \_ GETUNICODEFORMAT do CCM

Obtém o sinalizador de formato de caractere Unicode para o controle .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o sinalizador de formato Unicode para o controle . Se esse valor for diferentes de zero, o controle está usando caracteres Unicode. Se esse valor for zero, o controle está usando caracteres ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md)
</dt> </dl>

 

 





