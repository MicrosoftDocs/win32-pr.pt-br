---
title: Mensagem de COLOROKSTRING (Commdlg. h)
description: Uma caixa de diálogo cor envia a mensagem registrada COLOROKSTRING para o procedimento de gancho, CCHookProc, quando o usuário seleciona uma cor e clica no botão OK.
ms.assetid: 18b28558-1262-4c88-becf-76ce799b7542
keywords:
- Caixas de diálogo de mensagem COLOROKSTRING
topic_type:
- apiref
api_name:
- COLOROKSTRING
- COLOROKSTRINGA
- COLOROKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86229c71f1234efb4b561ac73bc8aa20f6258cdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085545"
---
# <a name="colorokstring-message"></a>Mensagem COLOROKSTRING

Uma caixa de diálogo **cor** envia a mensagem registrada **COLOROKSTRING** para o procedimento de gancho, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), quando o usuário seleciona uma cor e clica no botão **OK** . O procedimento de gancho pode aceitar a cor e permitir que a caixa de diálogo seja fechada, ou rejeitar a cor e forçar a caixa de diálogo a permanecer aberta.


```C++
#define COLOROKSTRING TEXT("commdlg_ColorOK")
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) . O membro **rgbResult** dessa estrutura contém o valor de cor RGB da cor selecionada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o procedimento de gancho retornar zero, a caixa de diálogo **cor** aceitará a cor selecionada e fechará.

Se o procedimento de gancho retornar um valor diferente de zero, a caixa de diálogo **cor** rejeitará a cor selecionada e permanecerá aberta.

## <a name="remarks"></a>Comentários

O procedimento de gancho deve especificar a constante **COLOROKSTRING** em uma chamada para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador da mensagem enviada pela caixa de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **COLOROKSTRINGW** (Unicode) e **COLOROKSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Biblioteca de caixa de diálogo comum](common-dialog-box-library.md)
</dt> </dl>

 

