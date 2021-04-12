---
title: Mensagem de EM_EMPTYUNDOBUFFER (WinUser. h)
description: Redefine o sinalizador de desfazer de um controle de edição. O sinalizador de desfazer é definido sempre que uma operação dentro do controle de edição pode ser desfeita. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- Controles de EM_EMPTYUNDOBUFFER de mensagens do Windows
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
ms.openlocfilehash: 0abbdc067b603a032b8d311ddd7930a8ca6de01c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455442"
---
# <a name="em_emptyundobuffer-message"></a>\_Mensagem em EMPTYUNDOBUFFER

Redefine o sinalizador de desfazer de um controle de edição. O sinalizador de desfazer é definido sempre que uma operação dentro do controle de edição pode ser desfeita. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

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

O sinalizador de desfazer é redefinido automaticamente sempre que o controle de edição recebe uma mensagem do [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) ou em [**\_ SetHandle**](em-sethandle.md) .

**Editar controles e edição avançada 1,0:** O controle só pode desfazer ou refazer a operação mais recente.

**Edição avançada 2,0 e posterior:** A mensagem em **\_ EMPTYUNDOBUFFER** esvazia todos os buffers de desfazer e refazer. Os controles de edição avançados permitem que o usuário desfaça ou refaça várias operações.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

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

[**em \_ CANcelamento**](em-canundo.md)
</dt> <dt>

[**\_ONhandle**](em-sethandle.md)
</dt> <dt>

[**em \_ desfazer**](em-undo.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**SetText do WM \_**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

