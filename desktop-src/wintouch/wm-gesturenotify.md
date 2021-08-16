---
title: WM_GESTURENOTIFY mensagem (Winuser.h)
description: Dá a você a oportunidade de definir a configuração do gesto.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- WM_GESTURENOTIFY mensagem Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURENOTIFY
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d474f356310a0d7949cecf36e7af9cb586a76029171dfe27c1679970e481ed1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435232"
---
# <a name="wm_gesturenotify-message"></a>Mensagem WM \_ GESTURENOTIFY

Dá a você a oportunidade de definir a configuração do gesto.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para [**um GESTURENOTIFYSTRUCT.**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um valor deve ser retornado de [DefWindowProc.](/windows/win32/api/winuser/nf-winuser-defwindowproca)

## <a name="remarks"></a>Comentários

Quando a **mensagem WM \_ GESTURENOTIFY** é recebida, o aplicativo pode usar [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) para especificar os gestos a receber. Essa mensagem sempre deve ser em bolhas usando a [função DefWindowProc.](/windows/win32/api/winuser/nf-winuser-defwindowproca)

> [!Note]  
> Manipular a **mensagem WM \_ GESTURENOTIFY** alterará a configuração do gesto durante o tempo de vida da Janela, não apenas para o próximo gesto.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como habilitar todos os gestos. Para obter mais exemplos, [**consulte SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).


```C++
    switch (message)
    {
    case WM_GESTURENOTIFY:
        GESTURECONFIG gc = {0,GC_ALLGESTURES,0};
        BOOL bResult = SetGestureConfig(hWnd,0,1,&gc,sizeof(GESTURECONFIG));
            
        if(!bResult)
        {
            // an error
        }
        return DefWindowProc(hWnd, WM_GESTURENOTIFY, wParam, lParam);
    }
      
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                  |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Notificações](notifications.md)
</dt> <dt>

[Windows Guia de programação de gestos de toque](guide-multi-touch-gestures.md)
</dt> <dt>

[**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 

