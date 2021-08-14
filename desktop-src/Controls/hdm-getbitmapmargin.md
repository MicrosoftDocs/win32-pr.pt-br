---
title: Mensagem de HDM_GETBITMAPMARGIN (commctrl. h)
description: Obtém a largura da margem de bitmap para um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetBitmapMargin do cabeçalho.
ms.assetid: 67794ad4-3c22-4fad-a1d7-7a5d5cc6ad67
keywords:
- controles de Windows de mensagem de HDM_GETBITMAPMARGIN
topic_type:
- apiref
api_name:
- HDM_GETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 685fb96e2ecf97a33b264de7bb3a6579f0c3480b6a15fdf99929ae879f4b35c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436206"
---
# <a name="hdm_getbitmapmargin-message"></a>\_Mensagem HDM GETBITMAPMARGIN

Obtém a largura da margem de bitmap para um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetBitmapMargin do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a largura da margem do bitmap em pixels. Se a margem do bitmap não tiver sido especificada anteriormente, o valor padrão de 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM \_ CXEDGE) será retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**HDM \_ SETBITMAPMARGIN**](hdm-setbitmapmargin.md)
</dt> </dl>

 

