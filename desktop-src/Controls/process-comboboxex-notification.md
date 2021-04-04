---
title: Como processar notificações do ComboBoxEx
description: Este tópico demonstra como processar mensagens de notificação ComboBoxEx.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9787e22aa01d51478ca55f0dde5d7ac944decb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917825"
---
# <a name="how-to-process-comboboxex-notifications"></a><span data-ttu-id="29a12-103">Como processar notificações do ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="29a12-103">How to Process ComboBoxEx Notifications</span></span>

<span data-ttu-id="29a12-104">Este tópico demonstra como processar mensagens de notificação ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="29a12-104">This topic demonstrates how to process ComboBoxEx notification messages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="29a12-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="29a12-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="29a12-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="29a12-106">Technologies</span></span>

-   [<span data-ttu-id="29a12-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="29a12-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="29a12-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="29a12-108">Prerequisites</span></span>

-   <span data-ttu-id="29a12-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="29a12-109">C/C++</span></span>
-   <span data-ttu-id="29a12-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="29a12-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="29a12-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="29a12-111">Instructions</span></span>


<span data-ttu-id="29a12-112">Um controle ComboBoxEx notifica sua janela pai de eventos enviando mensagens de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="29a12-112">A ComboBoxEx control notifies its parent window of events by sending [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="29a12-113">Ele também passa as mensagens de notificação do [**\_ comando do WM**](/windows/desktop/menurc/wm-command) recebidas da caixa de combinação contida nela para a janela pai a ser processada.</span><span class="sxs-lookup"><span data-stu-id="29a12-113">It also passes the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) notification messages that it receives from the combo box contained within it to the parent window to be processed.</span></span> <span data-ttu-id="29a12-114">Portanto, seu aplicativo deve estar preparado para processar mensagens de **\_ notificação do WM** nas mensagens **de \_ comando** ComboBoxEx e WM que são encaminhadas do controle da caixa de combinação filho ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="29a12-114">Therefore, your application must be prepared to process **WM\_NOTIFY** messages from the ComboBoxEx and **WM\_COMMAND** messages that are forwarded from the ComboBoxEx child combo box control.</span></span>

<span data-ttu-id="29a12-115">O exemplo nesta seção manipula as mensagens de [**\_ comando**](/windows/desktop/menurc/wm-command) do WM [**\_ Notify**](wm-notify.md) e do WM de um controle ComboBoxEx chamando uma função definida pelo aplicativo correspondente para processar essas mensagens.</span><span class="sxs-lookup"><span data-stu-id="29a12-115">The example in this section handles the [**WM\_NOTIFY**](wm-notify.md) and [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages from a ComboBoxEx control by calling a corresponding application-defined function to process these messages.</span></span>

## <a name="complete-example"></a><span data-ttu-id="29a12-116">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="29a12-116">Complete example</span></span>


```C++
LRESULT CALLBACK WndProc (HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch(msg){

        case WM_COMMAND: // notification from the child ComboBox within the ComboBoxEx control.
            if((HWND)lParam == g_hwndCB)
                DoOldNotify(hwnd,  wParam);  
            break;

        case WM_NOTIFY: // notification from the ComboBoxEx control
            return (DoCBEXNotify(hwnd, lParam));

        case WM_PAINT:
            hdc = BeginPaint(hwnd, &ps);
            EndPaint(hwnd, &ps);
            break;

        case WM_DESTROY:
            PostQuitMessage(0);
            break;

        default:
            return DefWindowProc(hwnd, msg, wParam, lParam);
            break;
    }

    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="29a12-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29a12-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29a12-118">Sobre controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="29a12-118">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="29a12-119">Referência de controle ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="29a12-119">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="29a12-120">Usando controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="29a12-120">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="29a12-121">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="29a12-121">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 