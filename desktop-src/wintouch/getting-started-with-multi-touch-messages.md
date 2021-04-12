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
# <a name="getting-started-with-windows-touch-messages"></a><span data-ttu-id="15315-106">Introdução com mensagens de toque do Windows</span><span class="sxs-lookup"><span data-stu-id="15315-106">Getting Started with Windows Touch Messages</span></span>

<span data-ttu-id="15315-107">Esta seção explica as tarefas associadas à obtenção do Windows Touch input para funcionar em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15315-107">This section explains the tasks associated with getting Windows Touch input to function in your application.</span></span>

<span data-ttu-id="15315-108">As etapas a seguir normalmente são executadas ao trabalhar com mensagens do Windows Touch:</span><span class="sxs-lookup"><span data-stu-id="15315-108">The following steps are typically performed when working with Windows Touch messages:</span></span>

1.  <span data-ttu-id="15315-109">Teste os recursos do digitalizador de entrada.</span><span class="sxs-lookup"><span data-stu-id="15315-109">Test the capabilities of the input digitizer.</span></span>
2.  <span data-ttu-id="15315-110">Registre-se para receber mensagens do Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="15315-110">Register to receive Windows Touch messages.</span></span>
3.  <span data-ttu-id="15315-111">Manipule as mensagens.</span><span class="sxs-lookup"><span data-stu-id="15315-111">Handle the messages.</span></span>

<span data-ttu-id="15315-112">A mensagem usada para o Windows Touch é o [**WM \_ Touch**](wm-touchdown.md).</span><span class="sxs-lookup"><span data-stu-id="15315-112">The message used for Windows Touch is [**WM\_TOUCH**](wm-touchdown.md).</span></span> <span data-ttu-id="15315-113">Essa mensagem indica os vários Estados de contato com um digitalizador.</span><span class="sxs-lookup"><span data-stu-id="15315-113">This message indicates the various states of contact with a digitizer.</span></span>

## <a name="testing-the-capabilities-of-the-input-digitizer"></a><span data-ttu-id="15315-114">Testando os recursos do digitalizador de entrada</span><span class="sxs-lookup"><span data-stu-id="15315-114">Testing the Capabilities of the Input Digitizer</span></span>

<span data-ttu-id="15315-115">A função [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) pode ser usada para consultar os recursos do digitalizador de entrada passando o valor de *nIndex* do **\_ digitalizador SM**.</span><span class="sxs-lookup"><span data-stu-id="15315-115">The [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function can be used to query the capabilities of the input digitizer by passing in the *nIndex* value of **SM\_DIGITIZER**.</span></span> <span data-ttu-id="15315-116">[GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) retorna um campo de bits que indica se o dispositivo está pronto, se o dispositivo dá suporte à caneta ou ao toque, se o dispositivo de entrada está integrado ou externo e se o dispositivo dá suporte a várias entradas (Windows Touch).</span><span class="sxs-lookup"><span data-stu-id="15315-116">[GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) returns a bit field that indicates whether the device is ready, whether the device supports pen or touch, whether the input device is integrated or external, and whether the device supports multiple inputs (Windows Touch).</span></span> <span data-ttu-id="15315-117">A tabela a seguir mostra os bits para os vários campos.</span><span class="sxs-lookup"><span data-stu-id="15315-117">The following table shows the bits for the various fields.</span></span>



| <span data-ttu-id="15315-118">bit</span><span class="sxs-lookup"><span data-stu-id="15315-118">Bit</span></span>   | <span data-ttu-id="15315-119">8</span><span class="sxs-lookup"><span data-stu-id="15315-119">8</span></span>           | <span data-ttu-id="15315-120">7</span><span class="sxs-lookup"><span data-stu-id="15315-120">7</span></span>           | <span data-ttu-id="15315-121">6</span><span class="sxs-lookup"><span data-stu-id="15315-121">6</span></span>        | <span data-ttu-id="15315-122">5</span><span class="sxs-lookup"><span data-stu-id="15315-122">5</span></span>        | <span data-ttu-id="15315-123">4</span><span class="sxs-lookup"><span data-stu-id="15315-123">4</span></span>            | <span data-ttu-id="15315-124">3</span><span class="sxs-lookup"><span data-stu-id="15315-124">3</span></span>              | <span data-ttu-id="15315-125">2</span><span class="sxs-lookup"><span data-stu-id="15315-125">2</span></span>              | <span data-ttu-id="15315-126">1</span><span class="sxs-lookup"><span data-stu-id="15315-126">1</span></span>                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| <span data-ttu-id="15315-127">Valor</span><span class="sxs-lookup"><span data-stu-id="15315-127">Value</span></span> | <span data-ttu-id="15315-128">Pronto para pilha</span><span class="sxs-lookup"><span data-stu-id="15315-128">Stack Ready</span></span> | <span data-ttu-id="15315-129">Várias entradas</span><span class="sxs-lookup"><span data-stu-id="15315-129">Multi-input</span></span> | <span data-ttu-id="15315-130">Reservado</span><span class="sxs-lookup"><span data-stu-id="15315-130">Reserved</span></span> | <span data-ttu-id="15315-131">Reservado</span><span class="sxs-lookup"><span data-stu-id="15315-131">Reserved</span></span> | <span data-ttu-id="15315-132">Caneta externa</span><span class="sxs-lookup"><span data-stu-id="15315-132">External Pen</span></span> | <span data-ttu-id="15315-133">Caneta integrada</span><span class="sxs-lookup"><span data-stu-id="15315-133">Integrated Pen</span></span> | <span data-ttu-id="15315-134">Toque externo</span><span class="sxs-lookup"><span data-stu-id="15315-134">External Touch</span></span> | <span data-ttu-id="15315-135">Toque integrado</span><span class="sxs-lookup"><span data-stu-id="15315-135">Integrated Touch</span></span> |



 

<span data-ttu-id="15315-136">Para testar o resultado a partir do comando para um recurso específico, você pode usar o operador de & bits e o bit específico que está testando.</span><span class="sxs-lookup"><span data-stu-id="15315-136">To test the result from the command for a particular feature, you can use the bitwise & operator and the particular bit you are testing.</span></span> <span data-ttu-id="15315-137">Por exemplo, para testar o Windows Touch, você testará que o bit de sétima ordem está definido (0x40 em Hex).</span><span class="sxs-lookup"><span data-stu-id="15315-137">For example, to test for Windows Touch, you would test that the seventh-order bit is set (0x40 in hex).</span></span> <span data-ttu-id="15315-138">O exemplo de código a seguir mostra como esses valores podem ser testados.</span><span class="sxs-lookup"><span data-stu-id="15315-138">The following code example shows how these values could be tested.</span></span>


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



<span data-ttu-id="15315-139">A tabela a seguir lista as constantes definidas no Windows. h para testar os recursos de toque do digitalizador de entrada.</span><span class="sxs-lookup"><span data-stu-id="15315-139">The following table lists the constants defined in windows.h for testing touch capabilities of the input digitizer.</span></span>



| <span data-ttu-id="15315-140">Nome</span><span class="sxs-lookup"><span data-stu-id="15315-140">Name</span></span>                   | <span data-ttu-id="15315-141">Valor</span><span class="sxs-lookup"><span data-stu-id="15315-141">Value</span></span>      | <span data-ttu-id="15315-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="15315-142">Description</span></span>                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15315-143">configuração do TABLET \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="15315-143">TABLET\_CONFIG\_NONE</span></span>   | <span data-ttu-id="15315-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15315-144">0x00000000</span></span> | <span data-ttu-id="15315-145">O digitalizador de entrada não tem recursos de toque.</span><span class="sxs-lookup"><span data-stu-id="15315-145">The input digitizer does not have touch capabilities.</span></span>                                                                                                                                         |
| <span data-ttu-id="15315-146">\_toque integrado do NID \_</span><span class="sxs-lookup"><span data-stu-id="15315-146">NID\_INTEGRATED\_TOUCH</span></span> | <span data-ttu-id="15315-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="15315-147">0x00000001</span></span> | <span data-ttu-id="15315-148">Um digitalizador de toque integrado é usado para entrada.</span><span class="sxs-lookup"><span data-stu-id="15315-148">An integrated touch digitizer is used for input.</span></span>                                                                                                                                              |
| <span data-ttu-id="15315-149">\_toque externo \_ NID</span><span class="sxs-lookup"><span data-stu-id="15315-149">NID\_EXTERNAL\_TOUCH</span></span>   | <span data-ttu-id="15315-150">0x00000002</span><span class="sxs-lookup"><span data-stu-id="15315-150">0x00000002</span></span> | <span data-ttu-id="15315-151">Um digitalizador de toque externo é usado para entrada.</span><span class="sxs-lookup"><span data-stu-id="15315-151">An external touch digitizer is used for input.</span></span>                                                                                                                                                |
| <span data-ttu-id="15315-152">\_caneta integrada do NID \_</span><span class="sxs-lookup"><span data-stu-id="15315-152">NID\_INTEGRATED\_PEN</span></span>   | <span data-ttu-id="15315-153">0x00000004</span><span class="sxs-lookup"><span data-stu-id="15315-153">0x00000004</span></span> | <span data-ttu-id="15315-154">Um digitalizador de caneta integrado é usado para entrada.</span><span class="sxs-lookup"><span data-stu-id="15315-154">An integrated pen digitizer is used for input.</span></span>                                                                                                                                                |
| <span data-ttu-id="15315-155">\_caneta externa \_ NID</span><span class="sxs-lookup"><span data-stu-id="15315-155">NID\_EXTERNAL\_PEN</span></span>     | <span data-ttu-id="15315-156">0x00000008</span><span class="sxs-lookup"><span data-stu-id="15315-156">0x00000008</span></span> | <span data-ttu-id="15315-157">Um digitalizador de caneta externa é usado para entrada.</span><span class="sxs-lookup"><span data-stu-id="15315-157">An external pen digitizer is used for input.</span></span>                                                                                                                                                  |
| <span data-ttu-id="15315-158">NID \_ várias \_ entradas</span><span class="sxs-lookup"><span data-stu-id="15315-158">NID\_MULTI\_INPUT</span></span>      | <span data-ttu-id="15315-159">0x00000040</span><span class="sxs-lookup"><span data-stu-id="15315-159">0x00000040</span></span> | <span data-ttu-id="15315-160">Um digitalizador de entrada com suporte para várias entradas é usado para entrada.</span><span class="sxs-lookup"><span data-stu-id="15315-160">An input digitizer with support for multiple inputs is used for input.</span></span>                                                                                                                        |
| <span data-ttu-id="15315-161">NID \_ pronto</span><span class="sxs-lookup"><span data-stu-id="15315-161">NID\_READY</span></span>             | <span data-ttu-id="15315-162">0x00000080</span><span class="sxs-lookup"><span data-stu-id="15315-162">0x00000080</span></span> | <span data-ttu-id="15315-163">O digitalizador de entrada está pronto para entrada.</span><span class="sxs-lookup"><span data-stu-id="15315-163">The input digitizer is ready for input.</span></span> <span data-ttu-id="15315-164">Se esse valor for indefinido, isso pode significar que o serviço do Tablet está parado, o digitalizador não tem suporte ou os drivers do digitalizador não foram instalados.</span><span class="sxs-lookup"><span data-stu-id="15315-164">If this value is unset, it may mean that the tablet service is stopped, the digitizer is not supported, or digitizer drivers have not been installed.</span></span> |



 

<span data-ttu-id="15315-165">Verificar os valores de NID \_ \* é uma maneira útil de verificar os recursos do computador de um usuário para configurar seu aplicativo para entrada de toque, caneta ou não Tablet.</span><span class="sxs-lookup"><span data-stu-id="15315-165">Checking the NID\_\* values is a useful way of checking the capabilities of a user's computer to configure your application for touch, pen, or non-tablet input.</span></span> <span data-ttu-id="15315-166">Por exemplo, se você tiver uma interface do usuário dinâmica e quiser configurar automaticamente uma parte dela, poderá verificar se há NID de \_ \_ toque integrado, NID \_ multitoque e obter o número máximo de toques na primeira vez que um usuário executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15315-166">For example, if you have a dynamic user interface (UI) and want to automatically configure some of it, you could check for NID\_INTEGRATED\_TOUCH, NID\_MULTITOUCH, and could get the maximum number of touches the first time that a user runs your application.</span></span>

> [!Note]  
> <span data-ttu-id="15315-167">Há algumas limitações inerentes para o SM \_ GETSYSTEMMETRICS.</span><span class="sxs-lookup"><span data-stu-id="15315-167">There are some inherent limitations for SM\_GETSYSTEMMETRICS.</span></span> <span data-ttu-id="15315-168">Por exemplo, não há suporte para plug and Play.</span><span class="sxs-lookup"><span data-stu-id="15315-168">For example, there is no support for plug and play.</span></span> <span data-ttu-id="15315-169">Por esse motivo, tenha cuidado ao usar essa função como meio de configuração permanente.</span><span class="sxs-lookup"><span data-stu-id="15315-169">For this reason, use caution when using this function as a means for permanent configuration.</span></span>

 

## <a name="registering-to-receive-windows-touch-input"></a><span data-ttu-id="15315-170">Registrando para receber a entrada do Windows Touch</span><span class="sxs-lookup"><span data-stu-id="15315-170">Registering to Receive Windows Touch Input</span></span>

<span data-ttu-id="15315-171">Antes de receber a entrada do Windows Touch, os aplicativos devem primeiro se registrar para receber a entrada do Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="15315-171">Before receiving Windows Touch input, applications must first register to receive Windows Touch input.</span></span> <span data-ttu-id="15315-172">Ao registrar a janela do aplicativo, o aplicativo indica que ele é compatível com toque.</span><span class="sxs-lookup"><span data-stu-id="15315-172">By registering the application window, the application indicates that it is touch compatible.</span></span> <span data-ttu-id="15315-173">Depois que o aplicativo registra sua janela, as notificações do Windows Touch driver são encaminhadas para o aplicativo quando a entrada é feita na janela.</span><span class="sxs-lookup"><span data-stu-id="15315-173">After the application registers its window, notifications from the Windows Touch driver are forwarded to the application when input is made on the window.</span></span> <span data-ttu-id="15315-174">Quando o aplicativo é desligado, ele cancela o registro de sua janela para desabilitar as notificações.</span><span class="sxs-lookup"><span data-stu-id="15315-174">When the application shuts down, it unregisters its window to disable notifications.</span></span>

> [!Note]  
> <span data-ttu-id="15315-175">[**WM \_**](wm-touchdown.md) As mensagens de toque são atualmente "ávidos".</span><span class="sxs-lookup"><span data-stu-id="15315-175">[**WM\_TOUCH**](wm-touchdown.md) messages are currently "greedy."</span></span> <span data-ttu-id="15315-176">Depois que a primeira mensagem de toque for recebida em uma janela, todas as mensagens de toque serão enviadas para essa janela até que outra janela receba o foco.</span><span class="sxs-lookup"><span data-stu-id="15315-176">After the first touch message is received on a window, all touch messages are sent to that window until another window receives focus.</span></span>

 

> [!Note]  
> <span data-ttu-id="15315-177">Por padrão, você recebe mensagens de [**\_ gesto do WM**](wm-gesture.md) em vez de mensagens do [**WM \_ Touch**](wm-touchdown.md) .</span><span class="sxs-lookup"><span data-stu-id="15315-177">By default, you receive [**WM\_GESTURE**](wm-gesture.md) messages instead of [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> <span data-ttu-id="15315-178">Se você chamar [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), você deixará de receber mensagens de **\_ gesto do WM** .</span><span class="sxs-lookup"><span data-stu-id="15315-178">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will stop receiving **WM\_GESTURE** messages.</span></span>

 

<span data-ttu-id="15315-179">O código a seguir demonstra como um aplicativo pode se registrar para receber mensagens de toque do Windows em um aplicativo Win32.</span><span class="sxs-lookup"><span data-stu-id="15315-179">The following code demonstrates how an application could register to receive Windows Touch messages in a Win32 application.</span></span>


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a><span data-ttu-id="15315-180">Manipulando mensagens de toque do Windows</span><span class="sxs-lookup"><span data-stu-id="15315-180">Handling Windows Touch Messages</span></span>

<span data-ttu-id="15315-181">Você pode lidar com as mensagens de toque do Windows de aplicativos em sistemas operacionais Windows de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="15315-181">You can handle the Windows Touch messages from applications in Windows operating systems in many ways.</span></span> <span data-ttu-id="15315-182">Se você estiver programando um aplicativo de GUI, adicione o código dentro da `WndProc` função para lidar com as mensagens de interesse.</span><span class="sxs-lookup"><span data-stu-id="15315-182">If you are programming a GUI application, you add code within the `WndProc` function to handle the messages of interest.</span></span> <span data-ttu-id="15315-183">Se você estiver programando uma MFC (Microsoft Foundation Class) ou um aplicativo gerenciado, adicione manipuladores para as mensagens de interesse.</span><span class="sxs-lookup"><span data-stu-id="15315-183">If you are programming a Microsoft Foundation Class (MFC) or managed application, you add handlers for the messages of interest.</span></span> <span data-ttu-id="15315-184">O exemplo de código a seguir mostra como as mensagens de toque podem ser tratadas do WndProc em um aplicativo baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="15315-184">The following code example shows how touch messages could be handled from WndProc in a Windows-based application.</span></span>


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





<span data-ttu-id="15315-185">O código a seguir mostra como você pode implementar o mapa de mensagens e um manipulador de mensagens.</span><span class="sxs-lookup"><span data-stu-id="15315-185">The following code shows how you can implement the message map and a message handler.</span></span> <span data-ttu-id="15315-186">Observe que as mensagens devem ser declaradas no mapa da mensagem e, em seguida, o manipulador para a mensagem deve ser implementado.</span><span class="sxs-lookup"><span data-stu-id="15315-186">Note that the messages must be declared in the message map and then the handler for the message should be implemented.</span></span> <span data-ttu-id="15315-187">Por exemplo, em um aplicativo MFC, isso pode ser declarado no código da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="15315-187">For example, in an MFC application, this could be declared in the dialog code.</span></span> <span data-ttu-id="15315-188">Observe também que a `OnInitDialog` função da janela da caixa de diálogo teria que incluir uma chamada para [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) , como `RegisterTouchWindow(m_hWnd, 0)` .</span><span class="sxs-lookup"><span data-stu-id="15315-188">Note also, that the `OnInitDialog` function for your dialog window would have to include a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) such as `RegisterTouchWindow(m_hWnd, 0)`.</span></span>


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



<span data-ttu-id="15315-189">Tocar na janela indicará os toques de uma janela pop-up.</span><span class="sxs-lookup"><span data-stu-id="15315-189">Touching the window will indicate touches from a pop-up window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15315-190">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15315-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15315-191">Entrada por toque do Windows</span><span class="sxs-lookup"><span data-stu-id="15315-191">Windows Touch Input</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 