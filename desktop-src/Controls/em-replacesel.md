---
title: EM_REPLACESEL mensagem (Winuser.h)
description: Substitui o texto selecionado em um controle de edição ou um controle de edição rich pelo texto especificado.
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- EM_REPLACESEL controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 478550432aa8c03a081e8de214cdd7e8337a46eca2676a0531b177a81ff20a54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831177"
---
# <a name="em_replacesel-message"></a>Mensagem EM \_ REPLACESEL

Substitui o texto selecionado em um controle de edição ou um controle de edição rich pelo texto especificado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica se a operação de substituição pode ser desfeita. Se for **TRUE,** a operação poderá ser desfeita. Se for **FALSE,** a operação não poderá ser desfeita.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o texto de substituição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Use a **mensagem EM \_ REPLACESEL** para substituir apenas uma parte do texto em um controle de edição. Para substituir todo o texto, use a [**mensagem WM \_ SETTEXT.**](/windows/desktop/winmsg/wm-settext)

Se não houver nenhuma seleção, o texto de substituição será inserido no centro.

**Edição rica:** Com suporte no Microsoft Rich Edit 1.0 e posterior. Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

Em um controle de edição rico, o texto de substituição assume a formatação do caractere no a caret ou, se houver uma seleção, do primeiro caractere na seleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

