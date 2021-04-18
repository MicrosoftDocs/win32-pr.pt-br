---
title: WM_POINTERACTIVATE mensagem
description: Enviado a uma janela inativa quando um ponteiro principal gera uma WM_POINTERDOWN sobre a janela.
ms.assetid: 4eec37da-227c-4be1-bf0b-99704caa1322
keywords:
- Mensagens de entrada e notificações de WM_POINTERACTIVATE mensagem
topic_type:
- apiref
api_name:
- WM_POINTERACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: b9bda11b5cb7a27f7744df6e20890a125a66bd88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105816046"
---
# <a name="wm_pointeractivate-message"></a>WM_POINTERACTIVATE mensagem

Enviado a uma janela inativa quando um ponteiro principal gera uma [**WM_POINTERDOWN**](wm-pointerdown.md) sobre a janela. Desde que a mensagem permaneça sem tratamento, ela viaja para a cadeia de janelas pai até atingir a janela de nível superior. Os aplicativos podem responder a essa mensagem para especificar se desejam ser ativados.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_POINTERACTIVATE             0x024B
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contém o identificador de ponteiro e informações adicionais. Use as macros a seguir para recuperar essas informações.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador de ponteiro

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): valor de teste de sucesso retornado pelo processamento da mensagem de [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .

</dd> <dt>

*lParam* 
</dt> <dd>

Contém o identificador para a janela de nível superior da janela que está sendo ativada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar um dos valores descritos na seção comentários.

Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Comentários

Um aplicativo pode manipular essa mensagem e retornar um dos seguintes valores para determinar como o sistema processa a ativação e a entrada de ativação:

-   PA_ACTIVATE
-   PA_NOACTIVATE

É importante observar que, quando o usuário está interagindo com o sistema com vários ponteiros simultâneos, a oportunidade de ativação que a **WM_POINTERACTIVATE** mensagem representa está disponível para aplicativos somente para o primeiro desses ponteiros. Os aplicativos devem, portanto, estar cientes de que eles ainda podem receber entradas de ponteiros enquanto estiverem inativos.

Se o aplicativo não tratar essa mensagem, o [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) passará a mensagem para a janela pai.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> </dl>

 

