---
title: Mensagem de HDM_SETBITMAPMARGIN (commctrl. h)
description: Define a largura da margem, especificada em pixels, de um bitmap em um controle de cabeçalho existente. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetBitmapMargin do cabeçalho.
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- Controles de HDM_SETBITMAPMARGIN de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_SETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a5384151a63918a5828608b0aa8e829df61cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824642"
---
# <a name="hdm_setbitmapmargin-message"></a>\_Mensagem HDM SETBITMAPMARGIN

Define a largura da margem, especificada em pixels, de um bitmap em um controle de cabeçalho existente. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetBitmapMargin do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A largura, especificada em pixels, da margem que circunda um bitmap dentro de um controle de cabeçalho existente.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a largura da margem do bitmap, em pixels. Se a margem do bitmap não tiver sido especificada anteriormente, o valor padrão de 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ CXEDGE*) será retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**HDM \_ GETBITMAPMARGIN**](hdm-getbitmapmargin.md)
</dt> </dl>

 

