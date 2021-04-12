---
title: Introdução com mensagens de toque do Windows
description: Esta seção explica as tarefas associadas à obtenção do Windows Touch input para funcionar em seu aplicativo.
ms.assetid: cd4e140e-a0b8-494f-82d9-bc0bfba55ecd
keywords:
- Windows Touch, mensagens
- Windows Touch, registro para entrada por toque
- Windows Touch, testando digitalizadores de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39048a4f9d643026396328093ae554c0eaa5d08
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366152"
---
# <a name="getting-started-with-windows-touch-messages"></a>Introdução com mensagens de toque do Windows

Esta seção explica as tarefas associadas à obtenção do Windows Touch input para funcionar em seu aplicativo.

As etapas a seguir normalmente são executadas ao trabalhar com mensagens do Windows Touch:

1.  Teste os recursos do digitalizador de entrada.
2.  Registre-se para receber mensagens do Windows Touch.
3.  Manipule as mensagens.

A mensagem usada para o Windows Touch é o [**WM \_ Touch**](wm-touchdown.md). Essa mensagem indica os vários Estados de contato com um digitalizador.

## <a name="testing-the-capabilities-of-the-input-digitizer"></a>Testando os recursos do digitalizador de entrada

A função [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) pode ser usada para consultar os recursos do digitalizador de entrada passando o valor de *nIndex* do **\_ digitalizador SM**. [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) retorna um campo de bits que indica se o dispositivo está pronto, se o dispositivo dá suporte à caneta ou ao toque, se o dispositivo de entrada está integrado ou externo e se o dispositivo dá suporte a várias entradas (Windows Touch). A tabela a seguir mostra os bits para os vários campos.



| bit   | 8           | 7           | 6        | 5        | 4            | 3              | 2              | 1                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| Valor | Pronto para pilha | Várias entradas | Reservado | Reservado | Caneta externa | Caneta integrada | Toque externo | Toque integrado |



 

Para testar o resultado a partir do comando para um recurso específico, você pode usar o operador de & bits e o bit específico que está testando. Por exemplo, para testar o Windows Touch, você testará que o bit de sétima ordem está definido (0x40 em Hex). O exemplo de código a seguir mostra como esses valores podem ser testados.


```C++
#include <windows.h>
```




```C++
// test for touch
int value = GetSystemMetrics(SM_DIGITIZER);
if (value & NID_READY){ /* stack ready */}
if (value  & NID_MULTI_INPUT){
    /* digitizer is multitouch */ 
    MessageBoxW(hWnd, L"Multitouch found", L"IsMulti!", MB_OK);
}
if (value & NID_INTEGRATED_TOUCH){ /* Integrated touch */}
```



A tabela a seguir lista as constantes definidas no Windows. h para testar os recursos de toque do digitalizador de entrada.



| Nome                   | Valor      | Descrição                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| configuração do TABLET \_ \_ None   | 0x00000000 | O digitalizador de entrada não tem recursos de toque.                                                                                                                                         |
| \_toque integrado do NID \_ | 0x00000001 | Um digitalizador de toque integrado é usado para entrada.                                                                                                                                              |
| \_toque externo \_ NID   | 0x00000002 | Um digitalizador de toque externo é usado para entrada.                                                                                                                                                |
| \_caneta integrada do NID \_   | 0x00000004 | Um digitalizador de caneta integrado é usado para entrada.                                                                                                                                                |
| \_caneta externa \_ NID     | 0x00000008 | Um digitalizador de caneta externa é usado para entrada.                                                                                                                                                  |
| NID \_ várias \_ entradas      | 0x00000040 | Um digitalizador de entrada com suporte para várias entradas é usado para entrada.                                                                                                                        |
| NID \_ pronto             | 0x00000080 | O digitalizador de entrada está pronto para entrada. Se esse valor for indefinido, isso pode significar que o serviço do Tablet está parado, o digitalizador não tem suporte ou os drivers do digitalizador não foram instalados. |



 

Verificar os valores de NID \_ \* é uma maneira útil de verificar os recursos do computador de um usuário para configurar seu aplicativo para entrada de toque, caneta ou não Tablet. Por exemplo, se você tiver uma interface do usuário dinâmica e quiser configurar automaticamente uma parte dela, poderá verificar se há NID de \_ \_ toque integrado, NID \_ multitoque e obter o número máximo de toques na primeira vez que um usuário executar o aplicativo.

> [!Note]  
> Há algumas limitações inerentes para o SM \_ GETSYSTEMMETRICS. Por exemplo, não há suporte para plug and Play. Por esse motivo, tenha cuidado ao usar essa função como meio de configuração permanente.

 

## <a name="registering-to-receive-windows-touch-input"></a>Registrando para receber a entrada do Windows Touch

Antes de receber a entrada do Windows Touch, os aplicativos devem primeiro se registrar para receber a entrada do Windows Touch. Ao registrar a janela do aplicativo, o aplicativo indica que ele é compatível com toque. Depois que o aplicativo registra sua janela, as notificações do Windows Touch driver são encaminhadas para o aplicativo quando a entrada é feita na janela. Quando o aplicativo é desligado, ele cancela o registro de sua janela para desabilitar as notificações.

> [!Note]  
> [**WM \_**](wm-touchdown.md) As mensagens de toque são atualmente "ávidos". Depois que a primeira mensagem de toque for recebida em uma janela, todas as mensagens de toque serão enviadas para essa janela até que outra janela receba o foco.

 

> [!Note]  
> Por padrão, você recebe mensagens de [**\_ gesto do WM**](wm-gesture.md) em vez de mensagens do [**WM \_ Touch**](wm-touchdown.md) . Se você chamar [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), você deixará de receber mensagens de **\_ gesto do WM** .

 

O código a seguir demonstra como um aplicativo pode se registrar para receber mensagens de toque do Windows em um aplicativo Win32.


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a>Manipulando mensagens de toque do Windows

Você pode lidar com as mensagens de toque do Windows de aplicativos em sistemas operacionais Windows de várias maneiras. Se você estiver programando um aplicativo de GUI, adicione o código dentro da `WndProc` função para lidar com as mensagens de interesse. Se você estiver programando uma MFC (Microsoft Foundation Class) ou um aplicativo gerenciado, adicione manipuladores para as mensagens de interesse. O exemplo de código a seguir mostra como as mensagens de toque podem ser tratadas do WndProc em um aplicativo baseado no Windows.


```C++
  LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam ){
    BOOL bHandled = FALSE;
    UINT cInputs = LOWORD(wParam);
    PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
    if (pInputs){
        if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
            for (UINT i=0; i < cInputs; i++){
                TOUCHINPUT ti = pInputs[i];
                //do something with each touch input entry
            }            
            bHandled = TRUE;
        }else{
             /* handle the error here */
        }
        delete [] pInputs;
    }else{
        /* handle the error here, probably out of memory */
    }
    if (bHandled){
        // if you handled the message, close the touch input handle and return
        CloseTouchInputHandle((HTOUCHINPUT)lParam);
        return 0;
    }else{
        // if you didn't handle the message, let DefWindowProc handle it
        return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
    }
  }


LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
      // pass touch messages to the touch handler 
      case WM_TOUCH:
        OnTouch(hWnd, wParam, lParam);
        break;
```





O código a seguir mostra como você pode implementar o mapa de mensagens e um manipulador de mensagens. Observe que as mensagens devem ser declaradas no mapa da mensagem e, em seguida, o manipulador para a mensagem deve ser implementado. Por exemplo, em um aplicativo MFC, isso pode ser declarado no código da caixa de diálogo. Observe também que a `OnInitDialog` função da janela da caixa de diálogo teria que incluir uma chamada para [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) , como `RegisterTouchWindow(m_hWnd, 0)` .


```C++
  // Class implementations within a dialog
  LRESULT TestDlg::OnTouch( WPARAM wParam, LPARAM lParam ){
    //Insert handler code here to do something with the message or uncomment the following line to test
    //MessageBox(L"touch!", L"touch!", MB_OK);
    return 0;
  }
  // The message map
  BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
    ... ... ...
    ON_MESSAGE(WM_TOUCH, OnTouch)
  END_MESSAGE_MAP()  
 
  BOOL TestDlg::OnInitDialog()
  {
    CDialog::OnInitDialog();    

    RegisterTouchWindow(m_hWnd, 0);
     ... ... ...
  }  
  
```



Tocar na janela indicará os toques de uma janela pop-up.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Entrada por toque do Windows](guide-multi-touch-input.md)
</dt> </dl>

 

 