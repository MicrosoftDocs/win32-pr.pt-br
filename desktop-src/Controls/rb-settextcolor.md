---
title: Mensagem de RB_SETTEXTCOLOR (commctrl. h)
description: Define a cor de texto padrão de um controle rebar.
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- Controles de RB_SETTEXTCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68311572927f2e8dac623c697ac366d37d7ab5fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455527"
---
# <a name="rb_settextcolor-message"></a>\_Mensagem SETTEXTCOLOR RB

Define a cor de texto padrão de um controle rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a nova cor de texto padrão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a cor de texto padrão anterior.

## <a name="remarks"></a>Comentários

A cor de texto padrão do controle rebar é usada para desenhar o texto em um controle rebar e todas as faixas que são adicionadas depois que essa mensagem é enviada. A cor de texto padrão de uma determinada faixa pode ser substituída quando uma faixa é adicionada ou modificada definindo o \_ sinalizador cores RBBIM em **fMask** e definindo **clrBack** na estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETTEXTCOLOR RB**](rb-gettextcolor.md)
</dt> </dl>

 

