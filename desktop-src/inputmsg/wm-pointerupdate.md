---
title: WM_POINTERUPDATE mensagem
description: Postado para fornecer uma atualização em um ponteiro que fez contato sobre a área do cliente de uma janela ou em um ponteiro semcaptura de foco sobre a área do cliente de uma janela.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac222
keywords:
- WM_POINTERUPDATE mensagens de entrada e notificações
topic_type:
- apiref
api_name:
- WM_POINTERUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 40c1decbf3c209a381356c58c901c4cab992fadd28eb9566e55e46b1cf87e3d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829506"
---
# <a name="wm_pointerupdate-message"></a>WM_POINTERUPDATE mensagem

Postado para fornecer uma atualização em um ponteiro que fez contato sobre a área do cliente de uma janela ou em um ponteiro semcaptura de foco sobre a área do cliente de uma janela. Enquanto o ponteiro está passeando, a mensagem tem como alvo qualquer janela em que o ponteiro está acima. Enquanto o ponteiro está em contato com a superfície, o ponteiro é implicitamente capturado para a janela sobre a qual o ponteiro fez contato e essa janela continua recebendo entrada para o ponteiro até que ele interrompe o contato.

> \[! Importante\]  
> Os aplicativos da área de trabalho devem estar cientes de DPI. Se o aplicativo não estiver ciente de DPI, as coordenadas de tela contidas em mensagens de ponteiro e estruturas relacionadas poderão aparecer imprecisas devido à virtualização de DPI. A virtualização de DPI oferece suporte de dimensionamento automático para aplicativos que não têm conhecimento de DPI e estão ativos por padrão (os usuários podem desativar). Para obter mais informações, consulte [Escrevendo aplicativos Win32 de alto DPI.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERUPDATE              0x0245
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
-   [**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se o ponteiro especificado teve a quarta ação. Os aplicativos que desejam responder à quarta ação devem recuperar informações específicas para o tipo de ponteiro para determinar se o primeiro botão estendido do mouse (XButton1) é pressionado.
-   [**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um [**sinalizador que**](pointer-flags-contants.md) indica se o ponteiro especificado fez a quinta ação. Os aplicativos que desejam responder à quinta ação devem recuperar informações específicas para o tipo de ponteiro para determinar se o segundo botão de mouse estendido (XButton2) está pressionado.

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

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar zero.

Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Comentários

Cada ponteiro tem um identificador de ponteiro exclusivo durante seu tempo de vida. O tempo de vida de um ponteiro começa quando ele é detectado pela primeira vez.

Uma [**WM_POINTERENTER**](wm-pointerenter.md) será gerada se um ponteiro de foco for detectado. Uma [**WM_POINTERDOWN**](wm-pointerdown.md) mensagem seguida por **uma WM_POINTERENTER** será gerada se um ponteiro sem foco for detectado.

Durante seu tempo de vida, um ponteiro pode gerar uma série **WM_POINTERUPDATE** mensagens enquanto ele está passe o mouse ou em contato.

O tempo de vida de um ponteiro termina quando ele não é mais detectado. Isso gera uma mensagem [**WM_POINTERLEAVE**](wm-pointerleave.md) dados.

Quando um ponteiro é anulado, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) é definido.

Uma [**WM_POINTERLEAVE**](wm-pointerleave.md) mensagem também pode ser gerada quando um ponteiro não capturado se move para fora dos limites de uma janela.

Para obter a posição horizontal e vertical de um ponteiro, use o seguinte:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



A [**macro MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) também pode ser usada para converter o parâmetro lParam em uma [**estrutura POINTS.**](/previous-versions//dd162808(v=vs.85))

A [**função GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) pode ser usada para determinar os estados de chave do modificador de teclado associados a essa mensagem. Por exemplo, para detectar que a tecla ALT foi pressionada, verifique se **GetKeyState** (VK_MENU) &lt; 0.

Se o aplicativo não processar essa mensagem, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) poderá gerar uma ou mais mensagens WM_GESTURE se [**a**](../wintouch/wm-gesture.md) sequência de entrada desse e, possivelmente, outros ponteiros for reconhecida como um gesto. Se um gesto não for reconhecido, **DefWindowProc** poderá gerar entrada do mouse.

Se um aplicativo consumir seletivamente alguma entrada de ponteiro e passar o restante para [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), o comportamento resultante será indefinido.

Use a [**função GetPointerInfo**](/previous-versions/windows/desktop/api) para recuperar mais informações relacionadas a essa mensagem.

Se o aplicativo não processar essas mensagens tão rápido quanto elas são geradas, algumas movimentações poderão ser coalescadas. O histórico de entradas que foram coalesced nessa mensagem pode ser recuperado usando a [**função GetPointerInfoHistory.**](/previous-versions/windows/desktop/api)

## <a name="examples"></a>Exemplos

O exemplo de código [**a**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)seguir mostra como usar GET_X_LPARAM , [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)e [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api) para recuperar informações relevantes dos parâmetros wParam e lParam da **mensagem WM_POINTERUPDATE.**


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

if (IS_POINTER_PRIMARYBUTTON_WPARAM(wParam))
{
    // process pointer move while down, similar to mouse move with left button down
}
else if (IS_POINTER_SECONDARYBUTTON_WPARAM(wParam))
{
    // process pointer move while down, similar to mouse move with right button down
}
```



O exemplo de código a seguir mostra como usar [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) para recuperar a ID do ponteiro do parâmetro wParam da **mensagem WM_POINTERUPDATE** dados.


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



O exemplo de código a seguir mostra como lidar com diferentes tipos de ponteiro.


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_INPUT_TYPE pointerType = PT_POINTER;

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
        fHandled = HandleGenericPointerInfo(&pointerInfo);
    }
    break;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



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

 

