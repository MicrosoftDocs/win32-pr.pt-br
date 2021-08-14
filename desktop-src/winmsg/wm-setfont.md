---
description: Define a fonte que um controle deve usar ao desenhar o texto.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: Mensagem de WM_SETFONT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811bee30237a64955197588f87866d4a64af89edc640762ec16333839aee9220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199932"
---
# <a name="wm_setfont-message"></a>\_Mensagem de SETfont do WM

Define a fonte que um controle deve usar ao desenhar o texto.


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a fonte (**HFONT**). Se esse parâmetro for **nulo**, o controle usará a fonte padrão do sistema para desenhar texto.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior de *lParam* especifica se o controle deve ser redesenhado imediatamente após a configuração da fonte. Se esse parâmetro for **true**, o controle redesenhará a si mesmo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

A mensagem de **\_ fonte do WM** é aplicada a todos os controles, não apenas às caixas de diálogo.

O melhor momento para o proprietário de um controle de caixa de diálogo definir a fonte do controle é quando ele recebe a [**mensagem \_ INITDIALOG do WM**](../dlgbox/wm-initdialog.md) . O aplicativo deve chamar a função [**ExcluirObjeto**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) para excluir a fonte quando ela não for mais necessária; por exemplo, depois de destruir o controle.

O tamanho do controle não é alterado como resultado da recepção desta mensagem. Para evitar o recorte de texto que não caiba nos limites do controle, o aplicativo deve corrigir o tamanho da janela de controle antes de definir a fonte.

Quando uma caixa de diálogo usa o estilo de [ \_ fonte de domínio DS](../dlgbox/about-dialog-boxes.md) para definir o texto em seus controles, o sistema envia a mensagem do **WM \_ SetFont** para o procedimento da caixa de diálogo antes de criar os controles. Um aplicativo pode criar uma caixa de diálogo que contém o \_ estilo de fonte DS chamando qualquer uma das seguintes funções:

-   [**CreateDialogIndirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CreateDialogIndirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGTEMPLATE**](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[**MAKELPARAM**](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**WM \_ GETfont**](wm-getfont.md)
</dt> <dt>

[**INITDIALOG do WM \_**](../dlgbox/wm-initdialog.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
