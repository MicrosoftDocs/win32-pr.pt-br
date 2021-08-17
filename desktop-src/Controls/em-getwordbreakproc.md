---
title: EM_GETWORDBREAKPROC mensagem (Winuser.h)
description: Obtém o endereço da função wordwrap atual. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- EM_GETWORDBREAKPROC controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f615721328ce0062d6bba9c282466744e7b47c78ad335b905343893f9c1b6343
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119438056"
---
# <a name="em_getwordbreakproc-message"></a>Mensagem EM \_ GETWORDBREAKPROC

Obtém o endereço da função wordwrap atual. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

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

O valor de retorno especifica o endereço da função Wordwrap definida pelo aplicativo. O valor de retorno será **NULL** se nenhuma função Wordwrap existir.

## <a name="remarks"></a>Comentários

Uma função Wordwrap examina um buffer de texto que contém o texto a ser enviado para a exibição, procurando a primeira palavra que não se ajusta à linha de exibição atual. A função wordwrap coloca essa palavra no início da próxima linha na exibição. Uma função Wordwrap define o ponto no qual o sistema deve quebrar uma linha de texto para controles de edição de várias linhas, geralmente em um caractere de espaço que separa duas palavras.

**Edição rica:** Com suporte no Microsoft Rich Edit 1.0 e posterior. Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[**EM \_ FMTLINES**](em-fmtlines.md)
</dt> <dt>

[**EM \_ SETWORDBREAKPROC**](em-setwordbreakproc.md)
</dt> </dl>

 

