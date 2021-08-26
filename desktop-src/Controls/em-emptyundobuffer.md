---
title: EM_EMPTYUNDOBUFFER mensagem (Winuser.h)
description: Redefine o sinalizador desfazer de um controle de edição. O sinalizador desfazer é definido sempre que uma operação dentro do controle de edição pode ser desfeita. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- EM_EMPTYUNDOBUFFER controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_EMPTYUNDOBUFFER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63d59dab38bca921e2125377889f8d18ddf6eb45c023badeead47f7e07b860fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915896"
---
# <a name="em_emptyundobuffer-message"></a>Mensagem EM \_ EMPTYUNDOBUFFER

Redefine o sinalizador desfazer de um controle de edição. O sinalizador desfazer é definido sempre que uma operação dentro do controle de edição pode ser desfeita. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

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

O sinalizador de desfazer é redefinido automaticamente sempre que o controle de edição recebe uma [**mensagem WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) [**ou EM \_ SETHANDLE.**](em-sethandle.md)

**Editar controles e Edição 1.0 rich:** O controle só pode desfazer ou refazer a operação mais recente.

**Edição Rich 2.0 e posterior:** A **mensagem EM \_ EMPTYUNDOBUFFER** esvazia todos os buffers desfazer e refazer. Controles de edição rich permitem que o usuário desfaça ou refaça várias operações.

**Edição rica:** Com suporte no Microsoft Rich Edit 1.0 e posterior. Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**EM \_ CANUNDO**](em-canundo.md)
</dt> <dt>

[**EM \_ SETHANDLE**](em-sethandle.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

