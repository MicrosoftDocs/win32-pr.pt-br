---
description: Define a fonte que um controle deve usar ao desenhar texto.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: WM_SETFONT mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811bee30237a64955197588f87866d4a64af89edc640762ec16333839aee9220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199932"
---
# <a name="wm_setfont-message"></a>Mensagem WM \_ SETFONT

Define a fonte que um controle deve usar ao desenhar texto.


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para a fonte (**HFONT**). Se esse parâmetro for **NULL,** o controle usará a fonte padrão do sistema para desenhar texto.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem baixa *de lParam* especifica se o controle deve ser redesenhado imediatamente após a configuração da fonte. Se esse parâmetro for **TRUE,** o controle redesenhará a si mesmo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

A **mensagem WM \_ SETFONT** se aplica a todos os controles, não apenas àqueles nas caixas de diálogo.

O melhor momento para o proprietário de um controle de caixa de diálogo definir a fonte do controle é quando ele recebe a mensagem [**WM \_ INITDIALOG.**](../dlgbox/wm-initdialog.md) O aplicativo deve chamar a [**função DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) para excluir a fonte quando ela não for mais necessária; por exemplo, depois de destruir o controle .

O tamanho do controle não muda como resultado do recebimento dessa mensagem. Para evitar o recorte de texto que não se ajusta aos limites do controle, o aplicativo deve corrigir o tamanho da janela de controle antes de define a fonte.

Quando uma caixa de diálogo usa o estilo [ \_ DS SETFONT](../dlgbox/about-dialog-boxes.md) para definir o texto em seus controles, o sistema envia a mensagem **WM \_ SETFONT** para o procedimento da caixa de diálogo antes de criar os controles. Um aplicativo pode criar uma caixa de diálogo que contém o estilo DS SETFONT chamando qualquer \_ uma das seguintes funções:

-   [**Createdialogindirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [**Createdialogindirectparam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [**Dialogboxindirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [**Dialogboxindirectparam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

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

[**Createdialogindirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**Createdialogindirectparam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**Dialogboxindirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**Dialogboxindirectparam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**Dlgtemplate**](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[**MAKELPARAM**](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**WM \_ GETFONT**](wm-getfont.md)
</dt> <dt>

[**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
