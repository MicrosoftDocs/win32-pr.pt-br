---
title: Mensagem de BM_SETSTATE (WinUser. h)
description: Define o estado de realce de um botão. O estado de realce indica se o botão é realçado como se o usuário tivesse enviado por push. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetState do botão.
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- Controles de BM_SETSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9b60231980f406b0aeb499d724dc6aa7025513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755660"
---
# <a name="bm_setstate-message"></a>\_Mensagem BM SETstate

Define o estado de realce de um botão. O estado de realce indica se o botão é realçado como se o usuário tivesse enviado por push. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetState do botão**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **bool** que especifica se o botão é realçado. Um valor de **true** realça o botão. Um valor **false** remove qualquer realce.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem sempre retorna zero.

## <a name="remarks"></a>Comentários

Realce afeta apenas a aparência de um botão. Ele não tem nenhum efeito no estado de verificação de um botão de opção ou caixa de seleção.

Um botão é realçado automaticamente quando o usuário posiciona o cursor sobre ele e pressiona e mantém o botão esquerdo do mouse. O realce é removido quando o usuário libera o botão do mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**BM \_ GETstate**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETcheck**](bm-setcheck.md)
</dt> </dl>

 

 





