---
title: Mensagem de DTM_GETDATETIMEPICKERINFO (commctrl. h)
description: Obtém informações sobre um controle do seletor de data e hora (DTP).
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- Controles de DTM_GETDATETIMEPICKERINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_GETDATETIMEPICKERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398a2543caa6d7104339fb8debd83fcee3ac71f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454709"
---
# <a name="dtm_getdatetimepickerinfo-message"></a>\_Mensagem DTM GETDATETIMEPICKERINFO

Obtém informações sobre um controle do seletor de data e hora (DTP).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd> Um ponteiro para <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> para receber as informações. O chamador é responsável por alocar a memória para essa estrutura. Defina o membro **cbSize** da estrutura como sizeof (DATETIMEPICKERINFO) antes de enviar esta mensagem.</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





