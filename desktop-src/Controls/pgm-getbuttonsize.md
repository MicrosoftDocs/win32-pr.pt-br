---
title: PGM_GETBUTTONSIZE mensagem (Commctrl.h)
description: Recupera o tamanho atual do botão para o controle pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro Pager GetButtonSize.
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- PGM_GETBUTTONSIZE controles Windows mensagem
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a77bbfdbac95c10afc721cfbae41798083ea98f4dd78e9dfdec9099871d7afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985892"
---
# <a name="pgm_getbuttonsize-message"></a>Mensagem \_ GETBUTTONSIZE PGM

Recupera o tamanho atual do botão para o controle pager. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ Pager GetButtonSize.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor INT que contém o tamanho do botão atual, em pixels.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PGM \_ SETBUTTONSIZE**](pgm-setbuttonsize.md)
</dt> </dl>

 

 





