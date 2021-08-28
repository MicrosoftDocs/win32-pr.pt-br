---
title: Mensagem de WM_CHOOSEFONT_SETFLAGS (Commdlg. h)
description: Um aplicativo envia a mensagem do WM \_ ChooseFont \_ SetFlags para uma caixa de diálogo de fonte para definir as opções de exibição para a caixa de diálogo.
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- Caixas de diálogo de WM_CHOOSEFONT_SETFLAGS mensagem
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETFLAGS
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d77290dfb3668e24d3586cf6d742b524e05fb07979de7c8d45f39998aca9708
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726076"
---
# <a name="wm_choosefont_setflags-message"></a>Mensagem do WM \_ ChooseFont \_ SetFlags

Um aplicativo envia a mensagem do **WM \_ ChooseFont \_ SetFlags** para uma caixa de diálogo de **fonte** para definir as opções de exibição para a caixa de diálogo.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETFLAGS        (WM_USER + 102)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) que contém novas configurações no membro **flags** .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) cria uma caixa de diálogo de **fonte** e usa uma estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para especificar os valores iniciais para o membro **flags** . Use a mensagem do **WM \_ ChooseFont \_ SetFlags** para especificar valores diferentes para o membro **flags** enquanto a caixa de diálogo **fonte** estiver aberta.

Normalmente, você deve enviar a mensagem do **WM \_ ChooseFont \_ SetFlags** de um procedimento de gancho de [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Biblioteca de caixa de diálogo comum](common-dialog-box-library.md)
</dt> </dl>

 

