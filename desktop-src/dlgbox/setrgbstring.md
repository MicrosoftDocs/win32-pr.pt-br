---
title: Mensagem de SETRGBSTRING (Commdlg. h)
description: O procedimento de gancho de uma caixa de diálogo de cor, CCHookProc, pode enviar a mensagem registrada SETRGBSTRING para a caixa de diálogo para definir a seleção de cor atual.
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- Caixas de diálogo de mensagem SETRGBSTRING
topic_type:
- apiref
api_name:
- SETRGBSTRING
- SETRGBSTRINGA
- SETRGBSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea5489aaa6fafcaa19a97a44d81fd85abb178d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644921"
---
# <a name="setrgbstring-message"></a>Mensagem SETRGBSTRING

O procedimento de gancho de uma caixa de diálogo de **cor** , [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), pode enviar a mensagem registrada **SETRGBSTRING** para a caixa de diálogo para definir a seleção de cor atual.


```C++
#define SETRGBSTRING TEXT("commdlg_SetRGBColor")
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

O valor RGB da cor a ser selecionada na caixa de diálogo **cor** . Você pode usar a macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) para especificar as intensidades vermelhas, verdes e azuis de um valor de cor RGB.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esta mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Se *lParam* corresponder a uma das cores básicas ou a uma das 16 cores personalizadas, o procedimento da caixa de diálogo selecionará essa cor. O procedimento da caixa de diálogo também atualiza todos os controles na extensão de cor personalizada da caixa de diálogo **cor** , se ela estiver aberta.

Se *lParam* não corresponder a uma cor básica ou personalizada, o procedimento da caixa de diálogo não alterará a seleção de cor atual, mas atualizará os controles de cor personalizados, se estiverem visíveis.

## <a name="examples"></a>Exemplos

O código de exemplo a seguir obtém o identificador de mensagem **SETRGBSTRING** e, em seguida, define a seleção de cor como azul.


```
UINT uiSetRGB;

uiSetRGB = RegisterWindowMessage(SETRGBSTRING);

SendMessage(hdlg, uiSetRGB, 0, (LPARAM) RGB(0, 0, 255)); 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **SETRGBSTRINGW** (Unicode) e **SETRGBSTRINGA** (ANSI)<br/>                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Biblioteca de caixa de diálogo comum](common-dialog-box-library.md)
</dt> </dl>

 

