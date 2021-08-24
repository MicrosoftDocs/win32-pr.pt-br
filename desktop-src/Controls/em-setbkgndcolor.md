---
title: EM_SETBKGNDCOLOR mensagem (Richedit.h)
description: A mensagem EM \_ SETBKGNDCOLOR define a cor da tela de fundo para um controle de edição rico.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- EM_SETBKGNDCOLOR controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_SETBKGNDCOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1173c2da9f3c04e49211224bd269d79c0634e1cb3f8ea959f6b58e354fdf0dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412650"
---
# <a name="em_setbkgndcolor-message"></a>Mensagem EM \_ SETBKGNDCOLOR

A **mensagem EM \_ SETBKGNDCOLOR** define a cor da tela de fundo para um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica se a cor do sistema deve ser usada. Se esse parâmetro for um valor diferente de zero, a tela de fundo será definida como a cor do sistema de tela de fundo da janela. Caso contrário, a tela de fundo será definida como a cor especificada.

</dd> <dt>

*lParam* 
</dt> <dd>

Uma [**estrutura COLORREF**](/windows/desktop/gdi/colorref) que especifica a cor se *wParam* for zero. Para gerar um **COLORREF,** use a macro [**RGB.**](/windows/desktop/api/wingdi/nf-wingdi-rgb)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem retorna a cor original da tela de fundo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Outros recursos**
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

