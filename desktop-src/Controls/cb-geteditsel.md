---
title: Mensagem de CB_GETEDITSEL (WinUser. h)
description: Obtém as posições de caractere inicial e final da seleção atual no controle de edição de uma caixa de combinação.
ms.assetid: 72b64135-e35a-4f72-9fc7-e6bedf495f23
keywords:
- Controles de CB_GETEDITSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319ce4a3c7a5a61903d4fc3bf04eed223e749787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009365"
---
# <a name="cb_geteditsel-message"></a>\_Mensagem de GETEDITSEL CB

Obtém as posições de caractere inicial e final da seleção atual no controle de edição de uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um ponteiro para um valor **DWORD** que recebe a posição inicial da seleção. Este parâmetro pode ser **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para um valor **DWORD** que recebe a posição final da seleção. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um valor **DWORD** com base em zero com a posição inicial da seleção no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e com a posição final do primeiro caractere após o último caractere selecionado no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra duas maneiras de recuperar o intervalo de seleção atual.


```C++
DWORD start, end;

// Get the range from [out] parameters.
// hwnd is the handle of the combo box control.
SendMessage(hwnd, CB_GETEDITSEL, (WPARAM)&start, (LPARAM)&end;

// Get the range from the return value.
DWORD range = SendMessage(hwnd, CB_GETEDITSEL, NULL, NULL);
start = LOWORD(range);
end = HIWORD(range);
```



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

[**\_SETEDITSEL CB**](cb-seteditsel.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

