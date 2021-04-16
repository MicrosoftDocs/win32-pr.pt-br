---
title: Como usar notificações do SysLink
description: Há duas mensagens de notificação associadas ao controle SysLink \ 8212; uma para o mouse (NM \_ Click (Syslink)) e outra para o teclado (nm \_ Return).
ms.assetid: 77E80EB2-180B-4EDD-9FB5-9930E8886CA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864a2b8942b1244be51f5c284e6ce07d973ed4db
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "105753780"
---
# <a name="how-to-use-syslink-notifications"></a><span data-ttu-id="4d4ab-103">Como usar notificações do SysLink</span><span class="sxs-lookup"><span data-stu-id="4d4ab-103">How to Use SysLink Notifications</span></span>

<span data-ttu-id="4d4ab-104">Há duas mensagens de notificação associadas ao controle SysLink — uma para o mouse ([nm \_ Click (Syslink)](nm-click-syslink.md)) e outra para o teclado ([nm \_ Return](nm-return.md)).</span><span class="sxs-lookup"><span data-stu-id="4d4ab-104">There are two notification messages associated with the SysLink control—one for the mouse ([NM\_CLICK (syslink)](nm-click-syslink.md)), and one for the keyboard ([NM\_RETURN](nm-return.md)).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="4d4ab-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="4d4ab-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="4d4ab-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="4d4ab-106">Technologies</span></span>

-   [<span data-ttu-id="4d4ab-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="4d4ab-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="4d4ab-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="4d4ab-108">Prerequisites</span></span>

-   <span data-ttu-id="4d4ab-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="4d4ab-109">C/C++</span></span>
-   <span data-ttu-id="4d4ab-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="4d4ab-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="4d4ab-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="4d4ab-111">Instructions</span></span>

### <a name="use-syslink-notifications"></a><span data-ttu-id="4d4ab-112">Usar notificações do SysLink</span><span class="sxs-lookup"><span data-stu-id="4d4ab-112">Use SysLink Notifications</span></span>

<span data-ttu-id="4d4ab-113">O código de exemplo a seguir mostra como processar as notificações SysLink que são geradas quando o usuário clica em qualquer um dos dois links no [exemplo anterior](create-syslink-controls.md).</span><span class="sxs-lookup"><span data-stu-id="4d4ab-113">The following example code shows how to process the SysLink notifications that are generated when the user clicks either of the two links in the [previous example](create-syslink-controls.md).</span></span> <span data-ttu-id="4d4ab-114">Quando o usuário clica na URL da Internet, a página da Web associada é aberta no navegador padrão.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-114">When the user clicks the Internet URL, the associated webpage opens in the default browser.</span></span> <span data-ttu-id="4d4ab-115">Quando o usuário clica no hiperlink definido pelo aplicativo, uma caixa de mensagem é exibida.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-115">When the user clicks the application-defined hyperlink, a message box is displayed.</span></span>


```C++
// g_hLink is the handle of the SysLink control.
case WM_NOTIFY:

    switch (((LPNMHDR)lParam)->code)
    {
    
    case NM_CLICK:          // Fall through to the next case.
    
    case NM_RETURN:
        {
            PNMLINK pNMLink = (PNMLINK)lParam;
            LITEM   item    = pNMLink->item;
            
            if ((((LPNMHDR)lParam)->hwndFrom == g_hLink) && (item.iLink == 0))
              {
                ShellExecute(NULL, L"open", item.szUrl, NULL, NULL, SW_SHOW);
              }
            
            else if (wcscmp(item.szID, L"idInfo") == 0)
              {
                MessageBox(hDlg, L"This isn't much help.", L"Example", MB_OK);
              }
            
            break;
        }
    }
    
    break;
```



## <a name="related-topics"></a><span data-ttu-id="4d4ab-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d4ab-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d4ab-117">Usando controles SysLink</span><span class="sxs-lookup"><span data-stu-id="4d4ab-117">Using SysLink Controls</span></span>](using-syslink-controls.md)
</dt> <dt>

<span data-ttu-id="4d4ab-118">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="4d4ab-118">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




