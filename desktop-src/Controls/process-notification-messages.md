---
title: Como processar mensagens de notificação
description: Uma folha de propriedades envia \_ mensagens de notificação do WM para recuperar informações das páginas e notificar as páginas de ações do usuário.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c544910e44e0c865e738427285d7488147b9c1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103640343"
---
# <a name="how-to-process-notification-messages"></a><span data-ttu-id="6af51-103">Como processar mensagens de notificação</span><span class="sxs-lookup"><span data-stu-id="6af51-103">How to Process Notification Messages</span></span>

<span data-ttu-id="6af51-104">Uma folha de propriedades envia mensagens de [**\_ notificação do WM**](wm-notify.md) para recuperar informações das páginas e notificar as páginas de ações do usuário.</span><span class="sxs-lookup"><span data-stu-id="6af51-104">A property sheet sends [**WM\_NOTIFY**](wm-notify.md) messages to retrieve information from the pages and to notify the pages of user actions.</span></span>

<span data-ttu-id="6af51-105">O parâmetro *lParam* da mensagem é o endereço de uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , que contém o identificador para a caixa de diálogo da folha de propriedades, o identificador para a caixa de diálogo página e um código de notificação.</span><span class="sxs-lookup"><span data-stu-id="6af51-105">The *lParam* parameter of the message is the address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure, which contains the handle to the property sheet dialog box, the handle to the page dialog box, and a notification code.</span></span> <span data-ttu-id="6af51-106">A página deve responder a algumas mensagens de notificação definindo o \_ valor DWL MSGRESULT da página como **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="6af51-106">The page must respond to some notification messages by setting the DWL\_MSGRESULT value of the page to either **TRUE** or **FALSE**.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="6af51-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="6af51-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6af51-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="6af51-108">Technologies</span></span>

-   [<span data-ttu-id="6af51-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="6af51-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="6af51-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="6af51-110">Prerequisites</span></span>

-   <span data-ttu-id="6af51-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="6af51-111">C/C++</span></span>
-   <span data-ttu-id="6af51-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="6af51-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="6af51-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="6af51-113">Instructions</span></span>

### <a name="process-notification-messages"></a><span data-ttu-id="6af51-114">Processar mensagens de notificação</span><span class="sxs-lookup"><span data-stu-id="6af51-114">Process Notification Messages</span></span>

<span data-ttu-id="6af51-115">O exemplo a seguir é um fragmento de código do procedimento da caixa de diálogo para uma página.</span><span class="sxs-lookup"><span data-stu-id="6af51-115">The following example is a code fragment from the dialog box procedure for a page.</span></span> <span data-ttu-id="6af51-116">Ele mostra como processar o código de notificação da [ \_ ajuda do PSN](psn-help.md) .</span><span class="sxs-lookup"><span data-stu-id="6af51-116">It shows how to process the [PSN\_HELP](psn-help.md) notification code.</span></span>


```C++
case WM_NOTIFY:

    switch (((NMHDR FAR *) lParam)->code) 
    {
    case PSN_HELP:
        {
         
        char szBuf[FILE_LEN]; // Buffer for name of Help file

        // Display Help for the font properties page.
        LoadString(g_hinst, IDS_HELPFILE, &szBuf, sizeof(szBuf)/sizeof(szBuf[0]));
        WinHelp(((NMHDR FAR *)lParam)->hwndFrom, &szBuf, HELP_CONTEXT, IDH_FONT_PROPERTIES);                
        
        break;
        
         }
         
        // Process other property sheet notifications here.
    }
    
```



## <a name="related-topics"></a><span data-ttu-id="6af51-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6af51-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6af51-118">Usando folhas de propriedades</span><span class="sxs-lookup"><span data-stu-id="6af51-118">Using Property Sheets</span></span>](using-property-sheets.md)
</dt> <dt>

<span data-ttu-id="6af51-119">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="6af51-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




