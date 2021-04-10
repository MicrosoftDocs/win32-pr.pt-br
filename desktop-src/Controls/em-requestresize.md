---
title: Mensagem de EM_REQUESTRESIZE (RichEdit. h)
description: Força um controle de edição rico a enviar um \_ código de notificação en REQUESTRESIZE para sua janela pai.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- Controles de EM_REQUESTRESIZE de mensagens do Windows
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
ms.openlocfilehash: ec41e7be8e0f30d5c1ec011247f3964292c2218e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163620"
---
# <a name="em_requestresize-message"></a>\_Mensagem em REQUESTRESIZE

Força um controle de edição rico a enviar um código de notificação [**en \_ REQUESTRESIZE**](en-requestresize.md) para sua janela pai.

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

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Essa mensagem é útil durante o processamento de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) para o pai de um controle de edição com formatação inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**REQUESTRESIZE de EN \_**](en-requestresize.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**tamanho do WM \_**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

