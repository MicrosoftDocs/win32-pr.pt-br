---
title: WM_POINTERDOWN mensagem
description: Postado quando um ponteiro faz contato sobre a área do cliente de uma janela.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac000
keywords:
- WM_POINTERDOWN mensagens de entrada e notificações
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
ms.openlocfilehash: 9f94bf4474e208d0b1d29df7a5e2939d7826ca77
ms.sourcegitcommit: 1f917afc149b5cc449a4a25a87de311e4842734b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113689199"
---
# <a name="wm_pointerdown-message"></a>WM_POINTERDOWN mensagem

Postado quando um ponteiro faz contato sobre a área do cliente de uma janela. Essa mensagem de entrada tem como destino a janela sobre a qual o ponteiro faz contato e o ponteiro é implicitamente capturado para a janela para que a janela continue a receber entrada para o ponteiro até que elebre o contato.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Importante\]  
> Os aplicativos da área de trabalho devem estar cientes de DPI. Se o aplicativo não estiver ciente de DPI, as coordenadas de tela contidas em mensagens de ponteiro e estruturas relacionadas poderão aparecer imprecisas devido à virtualização de DPI. A virtualização de DPI oferece suporte de dimensionamento automático para aplicativos que não têm conhecimento de DPI e estão ativos por padrão (os usuários podem desativar). Para obter mais informações, consulte [Escrevendo aplicativos Win32 de alto DPI.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERDOWN                   0x0246
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contém informações sobre o ponteiro. Use as macros a seguir para recuperar informações do parâmetro wParam.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): o identificador de ponteiro.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se essa mensagem representa a primeira entrada gerada por um novo ponteiro.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se essa mensagem foi gerada por um ponteiro durante seu tempo de vida. Esse sinalizador não está definido em mensagens que indicam que o ponteiro tem intervalo de detecção à esquerda
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se essa mensagem foi gerada por um ponteiro que está em contato com a superfície da janela. Esse sinalizador não é definido em mensagens que indicam um ponteiro de foco.
-   [**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica que esse ponteiro foi designado como primário.
-   [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se há uma ação primária.
    -   Isso é análogo a um botão esquerdo do mouse para baixo.
    -   Um ponteiro de toque terá esse conjunto quando estiver em contato com a superfície do digitalizador.
    -   Um ponteiro de caneta terá esse conjunto quando estiver em contato com a superfície do digitalizador sem botões pressionados.
-   [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se há uma ação secundária.
    -   Isso é análogo a um botão direito do mouse para baixo.
    -   Um ponteiro de caneta terá esse conjunto quando estiver em contato com a superfície do digitalizador com o botão de caneta pressionado.
-   [**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se há uma ou mais ações terciárias com base no tipo de ponteiro; os aplicativos que desejam responder a ações terciárias devem recuperar informações específicas para o tipo de ponteiro para determinar quais botões terciários são pressionados. Por exemplo, um aplicativo pode determinar os estados de botões de uma caneta chamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) e examinando os sinalizadores que especificam os estados do botão.
-   [**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se o ponteiro especificado fez a quarta ação. Os aplicativos que desejam responder à quarta ação devem recuperar informações específicas para o tipo de ponteiro para determinar se o primeiro botão estendido do mouse (XButton1) é pressionado.
-   [**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um [**sinalizador**](pointer-flags-contants.md) que indica se o ponteiro especificado fez a quinta ação. Os aplicativos que desejam responder à quinta ação devem recuperar informações específicas para o tipo de ponteiro para determinar se o segundo botão de mouse estendido (XButton2) está pressionado.

    Consulte [**Sinalizadores de ponteiro**](pointer-flags-contants.md) para obter mais detalhes.

    > [!Note]  
    > Um ponteiro de foco não tem nenhum dos sinalizadores de botão definidos. Isso é análogo a uma movimentação do mouse sem botões do mouse para baixo. Um aplicativo pode determinar os estados de botões de uma caneta de foco, por exemplo, chamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) e examinando os sinalizadores que especificam os estados do botão.

     

</dd> <dt>

*lParam* 
</dt> <dd>

Contém o local do ponto do ponteiro.

> [!Note]  
> Como o ponteiro pode fazer contato com o dispositivo em uma área não trivial, esse local de ponto pode ser uma simplificação de uma área de ponteiro mais complexa. Sempre que possível, um aplicativo deve usar as informações completas da área do ponteiro em vez do local do ponto.

 

Use as macros a seguir para recuperar as coordenadas de tela física do ponto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): a coordenada x (ponto horizontal).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): a coordenada y (ponto vertical).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processa essa mensagem, ele deve retornar zero.

Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Comentários

> \[! Importante\]  
> Quando uma janela perde a captura de um ponteiro e recebe a [**notificação WM_POINTERCAPTURECHANGED,**](wm-pointercapturechanged.md) ela normalmente não receberá nenhuma notificação adicional. Por esse motivo, é importante que você não faça suposições com base em notificações WM_POINTERDOWN  / [**WM_POINTERUP WM_POINTERUP**](wm-pointerup.md) [](wm-pointerenter.md) / [**WM_POINTERENTER WM_POINTERLEAVE**](wm-pointerleave.md) emparelhadas.

 

Cada ponteiro tem um identificador de ponteiro exclusivo durante seu tempo de vida. O tempo de vida de um ponteiro começa quando ele é detectado pela primeira vez.

Uma [**WM_POINTERENTER**](wm-pointerenter.md) será gerada se um ponteiro de foco for detectado. Uma **WM_POINTERDOWN** mensagem de WM_POINTERENTER seguida por **uma** mensagem de WM_POINTERENTER será gerada se um ponteiro sem foco for detectado.

Durante seu tempo de vida, um ponteiro pode gerar uma série [**de WM_POINTERUPDATE**](wm-pointerupdate.md) mensagens enquanto ele está passe o mouse ou em contato.

O tempo de vida de um ponteiro termina quando ele não é mais detectado. Isso gera uma mensagem [**WM_POINTERLEAVE**](wm-pointerleave.md) dados.

Quando um ponteiro é anulado, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) é definido.

Uma [**WM_POINTERLEAVE**](wm-pointerleave.md) mensagem também pode ser gerada quando um ponteiro não capturado se move para fora dos limites de uma janela.

Para obter a posição horizontal e vertical de um ponteiro, use o seguinte:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Para converter o parâmetro lParam em uma [**estrutura POINTS,**](/previous-versions//dd162808(v=vs.85)) use a macro [**MAKEPOINTS.**](/windows/win32/api/wingdi/nf-wingdi-makepoints)

Para recuperar mais informações associadas à mensagem, use a [**função GetPointerInfo.**](/previous-versions/windows/desktop/api)

Para determinar os estados de chave do modificador de teclado associados a essa mensagem, use a [**função GetKeyState.**](/windows/win32/api/winuser/nf-winuser-getkeystate) Por exemplo, para detectar que a tecla ALT foi pressionada, verifique se GetKeyState(VK_MENU) &lt; 0.

Observe que, se o aplicativo não processar essa mensagem, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) poderá gerar uma ou mais mensagens WM_GESTURE se [**a**](../wintouch/wm-gesture.md) sequência de entrada desse e, possivelmente, outros ponteiros for reconhecida como um gesto. Se um gesto não for reconhecido, **DefWindowProc** poderá gerar entrada do mouse.

Se um aplicativo consumir seletivamente alguma entrada de ponteiro e passar o restante para [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), o comportamento resultante será indefinido.

Quando uma janela perde a captura de um ponteiro e recebe a [**WM_POINTERCAPTURECHANGED,**](wm-pointercapturechanged.md) ela normalmente não receberá nenhuma notificação adicional. Portanto, é importante que uma janela não faça suposições de seu status de ponteiro, independentemente de receber notificações DOWN/UP ou ENTER/LEAVE emparelhadas de maneira par.

## <a name="examples"></a>Exemplos

O exemplo de código [**a**](/previous-versions/windows/desktop/api)seguir mostra como usar IS_POINTER_FIRSTBUTTON_WPARAM , [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)e [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)para recuperar as informações relevantes associadas **à WM_POINTERDOWN** mensagem.


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



O exemplo de código a seguir mostra como usar [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) para recuperar a ID do ponteiro da **WM_POINTERDOWN** mensagem.


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &pointerInfo))
{
    // failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}
```



O exemplo de código a seguir mostra como lidar com diferentes tipos de ponteiro, como toque, caneta ou dispositivos de apontamento padrão.


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO         pointerInfo;
UINT32               pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE         pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &touchInfo))
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
    if (!GetPointerPenInfo(pointerId, &penInfo))
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
    if (!GetPointerInfo(pointerId, &pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



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
