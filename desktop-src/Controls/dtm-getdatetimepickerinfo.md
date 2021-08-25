---
title: Mensagem de DTM_GETDATETIMEPICKERINFO (commctrl. h)
description: Obtém informações sobre um controle do seletor de data e hora (DTP).
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- controles de Windows de mensagem de DTM_GETDATETIMEPICKERINFO
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
ms.openlocfilehash: 48dc639a48455564b9f925f7d6eea9634c01e597323f81d951cfde372a34ea37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878216"
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

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





