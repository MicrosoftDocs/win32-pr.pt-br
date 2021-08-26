---
title: PGM_GETPOS mensagem (Commctrl.h)
description: Recupera a posição de rolagem atual do controle de pager. Você pode enviar essa mensagem explicitamente ou usar a macro GetPos do \_ Pager.
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- PGM_GETPOS controles Windows mensagem
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f1d5608b720d5a5d3d661a368d094da9469d71108874a6cec5495bf120cc54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046866"
---
# <a name="pgm_getpos-message"></a>Mensagem \_ GETPOS do PGM

Recupera a posição de rolagem atual do controle de pager. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ GetPos do Pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor INT que contém a posição de rolagem atual, em pixels.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





