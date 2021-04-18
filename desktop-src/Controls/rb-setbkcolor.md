---
title: Mensagem de RB_SETBKCOLOR (commctrl. h)
description: Define a cor do plano de fundo padrão de um controle rebar.
ms.assetid: 450a1e16-24f6-4f86-8e46-14009da05efc
keywords:
- Controles de RB_SETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9365de2d790b1f28b1330c038b69d30b208143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749073"
---
# <a name="rb_setbkcolor-message"></a>\_Mensagem SETBKCOLOR RB

Define a cor do plano de fundo padrão de um controle rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a nova cor de plano de fundo padrão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a cor de plano de fundo padrão anterior.

## <a name="remarks"></a>Comentários

A cor do plano de fundo padrão do controle rebar é usada para desenhar o plano de fundo em um controle rebar e todas as faixas que são adicionadas depois que essa mensagem é enviada. A cor de plano de fundo padrão para uma banda específica pode ser substituída quando uma banda é adicionada ou modificada definindo o \_ sinalizador de cores RBBIM em **fMask** e definindo **clrBack** na estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .

Quando os estilos visuais são habilitados, essa mensagem não tem nenhum efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETBKCOLOR RB**](rb-getbkcolor.md)
</dt> </dl>

 

