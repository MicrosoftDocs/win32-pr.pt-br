---
title: Como processar a notificação de DTN_WMKEYDOWN
description: Este tópico demonstra como processar uma notificação DTN \_ WMKEYDOWN. Manipular esse código de notificação permite que o proprietário do controle forneça respostas específicas para pressionamentos de teclas dentro dos campos de retorno de chamada do controle.
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec97ffc5853743c357081b974d155ee0e0977d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103824075"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a><span data-ttu-id="8a430-104">Como processar a notificação DTN \_ WMKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="8a430-104">How to Process the DTN\_WMKEYDOWN Notification</span></span>

<span data-ttu-id="8a430-105">Este tópico demonstra como processar uma notificação [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) .</span><span class="sxs-lookup"><span data-stu-id="8a430-105">This topic demonstrates how to process a [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification.</span></span> <span data-ttu-id="8a430-106">Manipular esse código de notificação permite que o proprietário do controle forneça respostas específicas para pressionamentos de teclas dentro dos campos de retorno de chamada do controle.</span><span class="sxs-lookup"><span data-stu-id="8a430-106">Handling this notification code allows the owner of the control to provide specific responses to keystrokes within the callback fields of the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="8a430-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="8a430-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8a430-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="8a430-108">Technologies</span></span>

-   [<span data-ttu-id="8a430-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="8a430-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8a430-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="8a430-110">Prerequisites</span></span>

-   <span data-ttu-id="8a430-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="8a430-111">C/C++</span></span>
-   <span data-ttu-id="8a430-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="8a430-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8a430-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="8a430-113">Instructions</span></span>


<span data-ttu-id="8a430-114">Os controles do seletor de data e hora (DTP) enviam a mensagem [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) para relatar que o usuário digitou entrada em um campo de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8a430-114">Date and time picker (DTP) controls send the [DTN\_WMKEYDOWN](dtn-wmkeydown.md) message to report that the user has typed input in a callback field.</span></span> <span data-ttu-id="8a430-115">Se você quiser emular as mesmas respostas de teclado com suporte para campos DTP padrão ou fornecer respostas personalizadas, seu aplicativo deverá incluir o código para lidar com essa notificação.</span><span class="sxs-lookup"><span data-stu-id="8a430-115">If you want to emulate the same keyboard responses that are supported for standard DTP fields or provide custom responses, your application must include code to handle this notification.</span></span>

<span data-ttu-id="8a430-116">O exemplo de código C++ a seguir é uma função definida pelo aplicativo que processa a notificação [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) .</span><span class="sxs-lookup"><span data-stu-id="8a430-116">The following C++ code example is an application-defined function that processes the [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification.</span></span>

<span data-ttu-id="8a430-117">**Aviso de segurança:** O uso incorreto do **lstrcmp** pode comprometer a segurança do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8a430-117">**Security Warning:** Using **lstrcmp** incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="8a430-118">Por exemplo, antes de chamar **lstrcmp** no exemplo de código a seguir, você deve verificar se as duas cadeias de caracteres são terminadas em nulo.</span><span class="sxs-lookup"><span data-stu-id="8a430-118">For example, before calling **lstrcmp** in the following code example, you should make sure the two strings are null-terminated.</span></span> <span data-ttu-id="8a430-119">Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="8a430-119">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>



```C++
//  DoWMKeydown increments or decrements the day of month according 
//  to user keyboard input.

void WINAPI DoWMKeydown(
 HWND hwndDP,
 LPNMDATETIMEWMKEYDOWN lpDTKeystroke)
{
    int delta =1;
    if(!lstrcmp(lpDTKeystroke->pszFormat,L"XX")){
        switch(lpDTKeystroke->nVirtKey){
            case VK_DOWN:
            case VK_SUBTRACT:
                delta = -1;  // fall through

            case VK_UP:
            case VK_ADD:
                lpDTKeystroke->st.wDay += (WORD) delta;
                break;
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="8a430-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a430-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a430-121">Usando controles de seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="8a430-121">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="8a430-122">Referência de controle do seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="8a430-122">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="8a430-123">Seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="8a430-123">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




