---
title: WM_INITDIALOG mensagem (Winuser.h)
description: Enviado para o procedimento da caixa de diálogo imediatamente antes de uma caixa de diálogo ser exibida. Os procedimentos da caixa de diálogo normalmente usam essa mensagem para inicializar controles e executar outras tarefas de inicialização que afetam a aparência da caixa de diálogo.
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- WM_INITDIALOG caixa de diálogo de mensagem
topic_type:
- apiref
api_name:
- WM_INITDIALOG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e272ac93514fb60069a9217c3100318f95b1e9a8c77d9e75af56e2e7fbfbf66e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117766"
---
# <a name="wm_initdialog-message"></a>Mensagem WM \_ INITDIALOG

Enviado para o procedimento da caixa de diálogo imediatamente antes de uma caixa de diálogo ser exibida. Os procedimentos da caixa de diálogo normalmente usam essa mensagem para inicializar controles e executar outras tarefas de inicialização que afetam a aparência da caixa de diálogo.


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para o controle para receber o foco padrão do teclado. O sistema atribuirá o foco padrão do teclado somente se o procedimento da caixa de diálogo retornar **TRUE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Dados de inicialização adicionais. Esses dados são passados para o sistema como o parâmetro *lParam* em uma chamada para a função [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)ou [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) usada para criar a caixa de diálogo. Para folhas de propriedades, esse parâmetro é um ponteiro para a estrutura [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) usada para criar a página. Esse parâmetro será zero se qualquer outra função de criação de caixa de diálogo for usada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O procedimento da caixa de diálogo deve retornar **TRUE** para direcionar o sistema para definir o foco do teclado para o controle especificado por *wParam*. Caso contrário, ele deverá retornar **FALSE** para impedir que o sistema de definir o foco do teclado padrão.

O procedimento da caixa de diálogo deve retornar o valor diretamente. O **valor \_ MSGRESULT** do DWL definido pela função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.

## <a name="remarks"></a>Comentários

O controle para receber o foco padrão do teclado é sempre o primeiro controle na caixa de diálogo visível, não desabilitado e que tem o estilo **\_ TABSTOP do WS.** Quando o procedimento da caixa de diálogo **retorna TRUE**, o sistema verifica o controle para garantir que o procedimento não o desabilitou. Se ele tiver sido desabilitado, o sistema define o foco do teclado para o próximo controle visível, não desabilitado e tem o **\_ TABSTOP do WS.**

Um aplicativo só poderá **retornar FALSE** se tiver definido o foco do teclado como um dos controles da caixa de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Createdialogindirectparam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**Createdialogparam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[**Dialogboxindirectparam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**Dialogboxparam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Caixas de diálogo](dialog-boxes.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**Propsheetpage**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

