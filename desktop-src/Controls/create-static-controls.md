---
title: Como criar controles estáticos
description: O exemplo nesta seção demonstra como criar um controle estático animado.
ms.assetid: D2DA38CB-360C-49EC-90BC-9AFA88C4B751
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217135a6590fcee60286d21f00233916c4eba967
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104453893"
---
# <a name="how-to-create-static-controls"></a><span data-ttu-id="947ec-103">Como criar controles estáticos</span><span class="sxs-lookup"><span data-stu-id="947ec-103">How to Create Static Controls</span></span>

<span data-ttu-id="947ec-104">O exemplo nesta seção demonstra como criar um controle estático animado.</span><span class="sxs-lookup"><span data-stu-id="947ec-104">The example in this section demonstrates how to create an animated static control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="947ec-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="947ec-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="947ec-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="947ec-106">Technologies</span></span>

-   [<span data-ttu-id="947ec-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="947ec-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="947ec-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="947ec-108">Prerequisites</span></span>

-   <span data-ttu-id="947ec-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="947ec-109">C/C++</span></span>
-   <span data-ttu-id="947ec-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="947ec-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="947ec-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="947ec-111">Instructions</span></span>

### <a name="create-a-static-control"></a><span data-ttu-id="947ec-112">Criar um controle estático</span><span class="sxs-lookup"><span data-stu-id="947ec-112">Create a Static Control</span></span>

<span data-ttu-id="947ec-113">O exemplo de código a seguir usa um temporizador e a mensagem do [**\_ ícone STM**](stm-seticon.md) para animar um controle de ícone estático em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="947ec-113">The following code example uses a timer and the [**STM\_SETICON**](stm-seticon.md) message to animate a static icon control in a dialog box.</span></span>


```C++
#define MAXICONS 3 
#define HALF_SECOND 500

INT_PTR CALLBACK StaticDlgProc(HWND hDlg, UINT message, WPARAM wParam, 
    LPARAM lParam) 
{ 
    static HICON aIcons[MAXICONS]; 
    static UINT i = 0; 
    static UINT idTimer = 1; 

    switch (message) 
    { 
        case WM_INITDIALOG: 

            // Load the icon resources. g_hInst is the global instance handle.
            aIcons[i]   = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ICON1)); 
            aIcons[++i] = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ICON2)); 
            aIcons[++i] = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ICON3)); 
            
            // Reset the array index.
            i = 0;
 
            // Set a timer. 
            SetTimer(hDlg, idTimer, HALF_SECOND, (TIMERPROC) NULL); 
            return TRUE; 

        case WM_TIMER: 

            // Use STM_SETICON to associate a new icon with the static icon
            // control whenever a WM_TIMER message is received. 
            SendDlgItemMessage(hDlg, IDC_STATIC_ICON, STM_SETICON, 
                (WPARAM) aIcons[i], 0);                    

            // Reset the array index, if necessary.
            if (++i == MAXICONS)
                i = 0;

            return 0; 

        case WM_COMMAND: 
            if (wParam == IDOK 
                || wParam == IDCANCEL) 
            { 
                EndDialog(hDlg, TRUE); 
            } 
            return TRUE; 
 
        case WM_DESTROY: 
            KillTimer(hDlg, idTimer); 

            // Note that it is not necessary to call DestroyIcon here. LoadIcon
            // obtains a shared icon, which is valid as long as the module from 
            // which it was loaded is in memory. 
 
            return 0; 
    } 
    return FALSE; 

    UNREFERENCED_PARAMETER(lParam); 
} 
```



## <a name="remarks"></a><span data-ttu-id="947ec-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="947ec-114">Remarks</span></span>

<span data-ttu-id="947ec-115">O identificador do controle de ícone estático ( \_ ícone estático IDI \_ ) é definido em um arquivo de cabeçalho global e os ícones são carregados dos recursos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="947ec-115">The identifier of the static icon control (IDI\_STATIC\_ICON) is defined in a global header file, and the icons are loaded from the application resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="947ec-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="947ec-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="947ec-117">Usando controles estáticos</span><span class="sxs-lookup"><span data-stu-id="947ec-117">Using Static Controls</span></span>](using-static-controls.md)
</dt> <dt>

<span data-ttu-id="947ec-118">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="947ec-118">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




