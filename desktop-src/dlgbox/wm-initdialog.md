---
title: Mensagem de WM_INITDIALOG (WinUser. h)
description: Enviado para o procedimento da caixa de diálogo imediatamente antes de uma caixa de diálogo ser exibida. Os procedimentos da caixa de diálogo normalmente usam essa mensagem para inicializar controles e executar qualquer outra tarefa de inicialização que afete a aparência da caixa de diálogo.
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- Caixas de diálogo de WM_INITDIALOG mensagem
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
ms.openlocfilehash: 64646075bc3d5c90076d6c1ca0d61f80111c90ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769649"
---
# <a name="wm_initdialog-message"></a>Mensagem do WM \_ INITDIALOG

Enviado para o procedimento da caixa de diálogo imediatamente antes de uma caixa de diálogo ser exibida. Os procedimentos da caixa de diálogo normalmente usam essa mensagem para inicializar controles e executar qualquer outra tarefa de inicialização que afete a aparência da caixa de diálogo.


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para o controle para receber o foco padrão do teclado. O sistema atribuirá o foco padrão do teclado somente se o procedimento da caixa de diálogo retornar **true**.

</dd> <dt>

*lParam* 
</dt> <dd>

Dados de inicialização adicionais. Esses dados são passados para o sistema como o parâmetro *lParam* em uma chamada para a [**função CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)ou [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) usada para criar a caixa de diálogo. Para folhas de propriedades, esse parâmetro é um ponteiro para a estrutura [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) usada para criar a página. Esse parâmetro será zero se qualquer outra função de criação de caixa de diálogo for usada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O procedimento da caixa de diálogo deve retornar **true** para instruir o sistema a definir o foco do teclado para o controle especificado por *wParam*. Caso contrário, ele deve retornar **false** para impedir que o sistema defina o foco padrão do teclado.

O procedimento da caixa de diálogo deve retornar o valor diretamente. O valor de **\_ MSGRESULT DWL** definido pela função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.

## <a name="remarks"></a>Comentários

O controle para receber o foco padrão do teclado é sempre o primeiro controle na caixa de diálogo que está visível, não desabilitado, e que tem o estilo **WS \_ TabStop** . Quando o procedimento da caixa de diálogo retorna **true**, o sistema verifica o controle para garantir que o procedimento não o tenha desabilitado. Se ele tiver sido desabilitado, o sistema definirá o foco do teclado para o próximo controle que está visível, não desabilitado e que tem o **WS \_ TabStop**.

Um aplicativo pode retornar **false** somente se tiver definido o foco do teclado para um dos controles da caixa de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Caixas de diálogo](dialog-boxes.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

