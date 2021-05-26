---
title: Como processar notificações de selador de data e hora
description: Esta seção demonstra como processar notificações do se picker de data e hora.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa1214ebd671b4ae222990bde4b44586e6d7b11
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424176"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a><span data-ttu-id="f62c8-103">Como processar notificações de selador de data e hora</span><span class="sxs-lookup"><span data-stu-id="f62c8-103">How to Process Date and Time Picker Notifications</span></span>

<span data-ttu-id="f62c8-104">Esta seção demonstra como processar notificações do se picker de data e hora.</span><span class="sxs-lookup"><span data-stu-id="f62c8-104">This section demonstrates how to process date and time picker notifications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f62c8-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="f62c8-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f62c8-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="f62c8-106">Technologies</span></span>

-   [<span data-ttu-id="f62c8-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="f62c8-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f62c8-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="f62c8-108">Prerequisites</span></span>

-   <span data-ttu-id="f62c8-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="f62c8-109">C/C++</span></span>
-   <span data-ttu-id="f62c8-110">Programação Interface do Usuário Windows</span><span class="sxs-lookup"><span data-stu-id="f62c8-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f62c8-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="f62c8-111">Instructions</span></span>


<span data-ttu-id="f62c8-112">Um controle DTP (selador de data e hora) envia mensagens de notificação para a janela pai quando eventos, geralmente disparados pela entrada do usuário, ocorrem no controle .</span><span class="sxs-lookup"><span data-stu-id="f62c8-112">A date and time picker (DTP) control sends notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="f62c8-113">Seu aplicativo deve incluir código para determinar o tipo de mensagem de notificação e responder adequadamente.</span><span class="sxs-lookup"><span data-stu-id="f62c8-113">Your application must include code to determine the type of notification message and respond appropriately.</span></span>

<span data-ttu-id="f62c8-114">Se você planeja usar campos de retorno de chamada com os controles DTP em seu aplicativo, deve estar preparado para lidar com códigos de notificação [DTN \_ FORMATQUERY,](dtn-formatquery.md) [DTN \_ FORMAT](dtn-format.md)e [DTN \_ WMKEYDOWN.](dtn-wmkeydown.md)</span><span class="sxs-lookup"><span data-stu-id="f62c8-114">If you plan to use callback fields with the DTP controls in your application, you must be prepared to handle [DTN\_FORMATQUERY](dtn-formatquery.md), [DTN\_FORMAT](dtn-format.md), and [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification codes.</span></span> <span data-ttu-id="f62c8-115">Para obter informações adicionais sobre campos de retorno de chamada, consulte [Campos de retorno de chamada](date-and-time-picker-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f62c8-115">For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).</span></span>

<span data-ttu-id="f62c8-116">O exemplo de código C++ a seguir identifica a mensagem de notificação enviada por um controle DTP e chama a função apropriada definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f62c8-116">The following C++ code example identifies the notification message sent by a DTP control and calls the appropriate application-defined function.</span></span> <span data-ttu-id="f62c8-117">Consulte os tópicos a seguir para ver exemplos de código que ilustram como processar as notificações que aparecem neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="f62c8-117">Refer to the following topics for code examples that illustrate how to process the notifications that appear in this example.</span></span>

|   <span data-ttu-id="f62c8-118">Tópicos</span><span class="sxs-lookup"><span data-stu-id="f62c8-118">Topics</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f62c8-119">Como processar a notificação DTN \_ DATETIMECHANGE</span><span class="sxs-lookup"><span data-stu-id="f62c8-119">How to Process the DTN\_DATETIMECHANGE Notification</span></span>](process-the-dtn-datetimechange-notification.md) |
| [<span data-ttu-id="f62c8-120">Como processar a notificação DTN \_ FORMATQUERY</span><span class="sxs-lookup"><span data-stu-id="f62c8-120">How to Process the DTN\_FORMATQUERY Notification</span></span>](process-the-dtn-formatquery-notification.md)       |
| [<span data-ttu-id="f62c8-121">Como processar a notificação de formato \_ DTN</span><span class="sxs-lookup"><span data-stu-id="f62c8-121">How to Process the DTN\_FORMAT Notification</span></span>](process-the-dtn-format-notfication.md)                  |
| [<span data-ttu-id="f62c8-122">Como processar a notificação wmkeydown de DTN \_</span><span class="sxs-lookup"><span data-stu-id="f62c8-122">How to Process the DTN\_WMKEYDOWN Notification</span></span>](process-the-dtn-wmkeydown-notification.md)           |



 



```C++
BOOL WINAPI DoNotify(HWND hwnd, WPARAM wParam, LPARAM lParam)
{
    LPNMHDR hdr = (LPNMHDR)lParam;

    switch(hdr->code){

        case DTN_DATETIMECHANGE:{
            LPNMDATETIMECHANGE lpChange = (LPNMDATETIMECHANGE)lParam;
            DoDateTimeChange(lpChange);
        }
        break;

        case DTN_FORMATQUERY:{
            LPNMDATETIMEFORMATQUERY lpDTFQuery = (LPNMDATETIMEFORMATQUERY)lParam;

            // Process DTN_FORMATQUERY to ensure that the control
            // displays callback information properly.
            DoFormatQuery(hdr->hwndFrom, lpDTFQuery);
        }
        break;

        case DTN_FORMAT:{
            LPNMDATETIMEFORMAT lpNMFormat = (LPNMDATETIMEFORMAT) lParam;

            // Process DTN_FORMAT to supply information about callback
            // fields (fields) in the DTP control.
            DoFormat(hdr->hwndFrom, lpNMFormat);
        }
        break;

        case DTN_WMKEYDOWN:{
            LPNMDATETIMEWMKEYDOWN lpDTKeystroke = 
                            (LPNMDATETIMEWMKEYDOWN)lParam;

            // Process DTN_WMKEYDOWN to respond to a user's keystroke in
            // a callback field.
            DoWMKeydown(hdr->hwndFrom, lpDTKeystroke);
        }
        break;
    }

    // All of the above notifications require the owner to return zero.
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="f62c8-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f62c8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f62c8-124">Notificações de selador de data e hora</span><span class="sxs-lookup"><span data-stu-id="f62c8-124">Date and Time Picker Notifications</span></span>](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[<span data-ttu-id="f62c8-125">Referência de controle do selador de data e hora</span><span class="sxs-lookup"><span data-stu-id="f62c8-125">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f62c8-126">Usando controles de selador de data e hora</span><span class="sxs-lookup"><span data-stu-id="f62c8-126">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="f62c8-127">Selador de data e hora</span><span class="sxs-lookup"><span data-stu-id="f62c8-127">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




