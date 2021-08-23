---
title: Mensagem de RB_SETTEXTCOLOR (commctrl. h)
description: Define a cor de texto padrão de um controle rebar.
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- controles de Windows de mensagem de RB_SETTEXTCOLOR
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
ms.openlocfilehash: 88458f5a131250dbb261040bf26689356c1ba5446db854839ded05ff287a14ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078610"
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

## <a name="return-value"></a>Valor retornado

Retorna um valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a cor de texto padrão anterior.

## <a name="remarks"></a>Comentários

A cor de texto padrão do controle rebar é usada para desenhar o texto em um controle rebar e todas as faixas que são adicionadas depois que essa mensagem é enviada. A cor de texto padrão de uma determinada faixa pode ser substituída quando uma faixa é adicionada ou modificada definindo o \_ sinalizador cores RBBIM em **fMask** e definindo **clrBack** na estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETTEXTCOLOR RB**](rb-gettextcolor.md)
</dt> </dl>

 

