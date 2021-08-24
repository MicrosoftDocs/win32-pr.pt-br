---
title: Mensagem de WM_TOUCH (WinUser. h)
description: Notifica a janela quando um ou mais pontos de toque, como um dedo ou uma caneta, toca uma superfície digitalizadora sensível ao toque.
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- WM_TOUCH Windows toque de mensagem
topic_type:
- apiref
api_name:
- WM_TOUCH
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1034a229dbb1f3895726fcb3c1551e2dd0f390be0fd7bc2eb81d8331e582eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810096"
---
# <a name="wm_touch-message"></a>Mensagem de toque do WM \_

Notifica a janela quando um ou mais pontos de toque, como um dedo ou uma caneta, toca uma superfície digitalizadora sensível ao toque.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A palavra de ordem inferior contém o número de pontos de toque associados a esta mensagem. A palavra de ordem superior é reservada para uso futuro.

</dd> <dt>

*lParam* 
</dt> <dd>

Contém um identificador de entrada por toque que pode ser usado em uma chamada para [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) para recuperar informações detalhadas sobre os pontos de toque associados a essa mensagem.

Esse identificador é válido somente dentro do processo atual e não deve passar por processo cruzado, exceto como **lParam** em uma chamada **SendMessage** ou de **mensagem** .

Quando o aplicativo não requer mais esse identificador, o aplicativo deve chamar **CloseTouchInputHandle** para liberar a memória de processo associada a esse identificador. A falha ao fazer isso pode resultar em um vazamento de memória do aplicativo.

Observe que o identificador de entrada por toque nesse parâmetro não é mais válido depois que a mensagem foi passada para [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) fechará e invalidará esse identificador.

Observe também que o identificador de entrada por toque nesse parâmetro não é mais válido depois que a mensagem foi encaminhada [**usando a mensagem,**](sendmessage--postmessage--and-related-functions.md) **SendMessage** ou uma de suas variantes. Essas funções serão fechadas e invalidarão esse identificador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

Se o aplicativo não processar a mensagem, ele deverá chamar [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Não fazer isso faz com que o aplicativo vazasse memória porque o identificador de entrada por toque não está fechado e a memória de processo associada não é liberada.

## <a name="remarks"></a>Comentários

**WM \_** As mensagens de toque não respeitam regiões **HTTRANSPARENTs** do Windows. Se uma janela retornar **HTTRANSPARENT** em resposta a uma mensagem do **WM \_ NCHITTEST** , as mensagens do mouse vão para o pai e as mensagens do **WM \_ Touch** vão diretamente para a janela.

## <a name="examples"></a>Exemplos

O código a seguir é um exemplo de como obter informações detalhadas de entrada de toque associadas a esta mensagem.


```C++
UINT cInputs = LOWORD(wParam);
PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
if (NULL != pInputs)
{
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
                          cInputs,
                          pInputs,
                          sizeof(TOUCHINPUT)))
    {
        // process pInputs
        if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
        {
            // error handling
        }
    }
    else
    {
        // GetLastError() and error handling
    }
    delete [] pInputs;
}
else
{
    // error handling, presumably out of memory
}
return DefWindowProc(hWnd, message, wParam, lParam);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                                  |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> <dt>

[Manipulações e guia de programação inércia](manipulation-and-inertia.md)
</dt> <dt>

[Windows Guia de programação de entrada por toque](guide-multi-touch-input.md)
</dt> </dl>

 

