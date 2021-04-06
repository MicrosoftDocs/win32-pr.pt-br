---
title: Mensagem de EM_SETBKGNDCOLOR (RichEdit. h)
description: A \_ mensagem em SETBKGNDCOLOR define a cor do plano de fundo para um controle de edição rico.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- Controles de EM_SETBKGNDCOLOR de mensagens do Windows
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
ms.openlocfilehash: 091f04909e2660498f1380628439c067b5438b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824688"
---
# <a name="em_setbkgndcolor-message"></a>\_Mensagem em SETBKGNDCOLOR

A mensagem em **\_ SETBKGNDCOLOR** define a cor do plano de fundo para um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica se a cor do sistema deve ser usada. Se esse parâmetro for um valor diferente de zero, o plano de fundo será definido como a cor do sistema de plano de fundo da janela. Caso contrário, o plano de fundo será definido como a cor especificada.

</dd> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**COLORREF**](/windows/desktop/gdi/colorref) especificando a cor se *wParam* for zero. Para gerar um **COLORREF**, use a macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna a cor do plano de fundo original.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Outros recursos**
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

