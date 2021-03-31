---
title: WM_POINTERDOWN mensagem
description: Postado quando um ponteiro faz contato sobre a área do cliente de uma janela.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac000
keywords:
- Mensagens de entrada e notificações de WM_POINTERDOWN mensagem
topic_type:
- apiref
api_name:
- WM_POINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 051e7f0aa08305e4c38d7eefec94483fd11f3bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085948"
---
# <a name="wm_pointerdown-message"></a>WM_POINTERDOWN mensagem

Postado quando um ponteiro faz contato sobre a área do cliente de uma janela. Essa mensagem de entrada é direcionada para a janela sobre a qual o ponteiro faz contato, e o ponteiro é capturado implicitamente na janela para que a janela continue a receber entrada para o ponteiro até que ele interrompa o contato.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Fundamental\]  
> Os aplicativos da área de trabalho devem ter reconhecimento de DPI. Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI. A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo). Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERDOWN                   0x0246
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contém informações sobre o ponteiro. Use as macros a seguir para recuperar informações do parâmetro wParam.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): o identificador do ponteiro.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se essa mensagem representa a primeira entrada gerada por um novo ponteiro.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se esta mensagem foi gerada por um ponteiro durante seu tempo de vida. Esse sinalizador não é definido em mensagens que indicam que o ponteiro tem um intervalo de detecção à esquerda
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se esta mensagem foi gerada por um ponteiro que está em contato com a superfície da janela. Esse sinalizador não é definido em mensagens que indicam um ponteiro de focalização.
-   [**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica que esse ponteiro foi designado como primário.
-   [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se há uma ação primária.
    -   Isso é análogo a um botão esquerdo do mouse para baixo.
    -   Um ponteiro de toque terá esse conjunto quando estiver em contato com a superfície digitalizadora.
    -   Um ponteiro de caneta terá esse conjunto quando estiver em contato com a superfície digitalizadora sem botões pressionados.
-   [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se há uma ação secundária.
    -   Isso é análogo a um botão direito do mouse para baixo.
    -   Um ponteiro de caneta terá esse conjunto quando estiver em contato com a superfície digitalizadora com o botão de rosca de caneta pressionado.
-   [**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se há uma ou mais ações de terciário com base no tipo de ponteiro; os aplicativos que desejam responder às ações de terciário devem recuperar informações específicas ao tipo de ponteiro para determinar quais botões terciários são pressionados. Por exemplo, um aplicativo pode determinar os Estados de botões de uma caneta chamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) e examinando os sinalizadores que especificam Estados de botão.
-   [**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se o ponteiro especificado levou a quarta ação. Os aplicativos que desejam responder às quartas ações devem recuperar informações específicas do tipo de ponteiro para determinar se o primeiro botão do mouse estendido (XButton1) é pressionado.
-   [**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um [**sinalizador**](pointer-flags-contants.md) que indica se o ponteiro especificado levou a quinta ação. Os aplicativos que desejam responder às quinta ações devem recuperar informações específicas do tipo de ponteiro para determinar se o segundo botão de mouse estendido (XButton2) é pressionado.

    Consulte [**sinalizadores de ponteiro**](pointer-flags-contants.md) para obter mais detalhes.

    > [!Note]  
    > Um ponteiro em foco não tem nenhum dos sinalizadores de botão definidos. Isso é análogo a um movimento de mouse sem botões de mouse para baixo. Um aplicativo pode determinar os Estados dos botões de uma caneta em foco, por exemplo, chamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) e examinando os sinalizadores que especificam Estados de botão.

     

</dd> <dt>

*lParam* 
</dt> <dd>

Contém o local do ponto do ponteiro.

> [!Note]  
> Como o ponteiro pode fazer contato com o dispositivo em uma área não trivial, esse local de ponto pode ser uma simplificação de uma área de ponteiro mais complexa. Sempre que possível, um aplicativo deve usar as informações completas da área do ponteiro em vez do local do ponto.

 

Use as macros a seguir para recuperar as coordenadas de tela física do ponto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): a coordenada X (ponto horizontal).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): a coordenada Y (ponto vertical).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Comentários

> \[! Fundamental\]  
> Quando uma janela perde a captura de um ponteiro e recebe a notificação de [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , ela normalmente não receberá notificações adicionais. Por esse motivo, é importante que você não faça nenhuma suposição com base em WM_POINTERDOWN igualmente emparelhadas  / [**WM_POINTERUP**](wm-pointerup.md) ou [**WM_POINTERENTER**](wm-pointerenter.md) / notificações de [**WM_POINTERLEAVE**](wm-pointerleave.md) .

 

Cada ponteiro tem um identificador de ponteiro exclusivo durante seu tempo de vida. O tempo de vida de um ponteiro começa quando é detectado pela primeira vez.

Uma mensagem de [**WM_POINTERENTER**](wm-pointerenter.md) será gerada se um ponteiro em foco for detectado. Uma mensagem de **WM_POINTERDOWN** seguida por uma mensagem de **WM_POINTERENTER** será gerada se um ponteiro sem foco for detectado.

Durante seu tempo de vida, um ponteiro pode gerar uma série de [**WM_POINTERUPDATE**](wm-pointerupdate.md) mensagens enquanto está focalizando ou em contato.

O tempo de vida de um ponteiro termina quando ele não é mais detectado. Isso gera uma mensagem de [**WM_POINTERLEAVE**](wm-pointerleave.md) .

Quando um ponteiro é anulado, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) é definido.

Uma mensagem de [**WM_POINTERLEAVE**](wm-pointerleave.md) também pode ser gerada quando um ponteiro não capturado é movido para fora dos limites de uma janela.

Para obter a posição horizontal e vertical de um ponteiro, use o seguinte:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Para converter o parâmetro lParam em uma estrutura [**Points**](/previous-versions//dd162808(v=vs.85)) , use a macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) .

Para recuperar mais informações associadas à mensagem, use a função [**GetPointerInfo**](/previous-versions/windows/desktop/api) .

Para determinar os Estados de chave de modificador de teclado associados a essa mensagem, use a função [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) . Por exemplo, para detectar que a tecla ALT foi pressionada, verifique se GetKeyState (VK_MENU) &lt; 0.

Observe que, se o aplicativo não processar essa mensagem, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) poderá gerar uma ou mais mensagens de [**WM_GESTURE**](../wintouch/wm-gesture.md) se a sequência de entrada desse e, possivelmente, outros ponteiros for reconhecida como um gesto. Se um gesto não for reconhecido, **DefWindowProc** poderá gerar a entrada do mouse.

Se um aplicativo consumir seletivamente alguma entrada de ponteiro e passar o resto para [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), o comportamento resultante será indefinido.

Quando uma janela perde a captura de um ponteiro e recebe a notificação de [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , ela normalmente não receberá notificações adicionais. Portanto, é importante que uma janela não faça suposições de seu status de ponteiro, independentemente de receber as notificações uniformemente emparelhadas ou inativas ou de entrada/saída.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como usar [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)e [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)para recuperar as informações relevantes associadas à mensagem de **WM_POINTERDOWN** .


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

if (IS_POINTER_PRIMARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse left button down
}
else if (IS_POINTER_SECONDARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse right button down
}
```



O exemplo de código a seguir mostra como usar [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) para recuperar a ID do ponteiro da mensagem de **WM_POINTERDOWN** .


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &amp;pointerInfo))
{
    // failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}
```



O exemplo de código a seguir mostra como lidar com diferentes tipos de ponteiro, como toque, caneta ou dispositivos apontadores padrão.


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO         pointerInfo;
UINT32               pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE         pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &amp;pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &amp;touchInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process touchInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
case PT_PEN:
    // Retrieve pen information
    if (!GetPointerPenInfo(pointerId, &amp;penInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process penInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
default:
    if (!GetPointerInfo(pointerId, &amp;pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&amp;pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> <dt>

**Referência**
</dt> <dt>

[**Sinalizadores de ponteiro**](pointer-flags-contants.md)
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

