---
title: Mensagem de MCM_GETMAXTODAYWIDTH (commctrl. h)
description: Recupera a largura máxima de \ 0034; hoje \ 0034; Cadeia de caracteres em um controle de calendário mensal. Isso inclui o texto do rótulo e o texto de data. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetMaxTodayWidth.
ms.assetid: bb55c24e-ba04-4a57-97b0-ff04d77e1d43
keywords:
- Controles de MCM_GETMAXTODAYWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETMAXTODAYWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b4c188e994a1dcc5a8fbd80ae3f1b06894bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644729"
---
# <a name="mcm_getmaxtodaywidth-message"></a>\_Mensagem MCM GETMAXTODAYWIDTH

Recupera a largura máxima da cadeia de caracteres "hoje" em um controle de calendário mensal. Isso inclui o texto do rótulo e o texto de data. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a largura da cadeia de caracteres "Today", em pixels.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





