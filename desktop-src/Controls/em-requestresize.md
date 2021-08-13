---
title: EM_REQUESTRESIZE mensagem (Richedit.h)
description: Força um controle de edição rico a enviar um código de notificação EN \_ REQUESTRESIZE para sua janela pai.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- EM_REQUESTRESIZE controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7113f52e2fa3a293549443f779ba937bf20b85736c6751cd9ab77bdbecd45c3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440156"
---
# <a name="em_requestresize-message"></a>Mensagem EM \_ REQUESTRESIZE

Força um controle de edição rico a enviar um código [**de notificação EN \_ REQUESTRESIZE**](en-requestresize.md) para sua janela pai.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Essa mensagem é útil durante o [**processamento do WM \_ SIZE**](/windows/desktop/winmsg/wm-size) para o pai de um controle de edição rico sem inferioridade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**EN \_ REQUESTRESIZE**](en-requestresize.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**TAMANHO \_ DO WM**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

