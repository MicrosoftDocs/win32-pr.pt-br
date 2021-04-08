---
title: Como criar um controle de cabeçalho
description: Este tópico demonstra como criar um controle de cabeçalho e posicioná-lo na área cliente da janela pai.
ms.assetid: 094AF70C-2761-439E-A1E3-0FD04212FE87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce9bf9d7b117f5f61766ca326b91b0d19a2c903
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008627"
---
# <a name="how-to-create-a-header-control"></a><span data-ttu-id="61eec-103">Como criar um controle de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="61eec-103">How to Create a Header Control</span></span>

<span data-ttu-id="61eec-104">Este tópico demonstra como criar um controle de cabeçalho e posicioná-lo na área cliente da janela pai.</span><span class="sxs-lookup"><span data-stu-id="61eec-104">This topic demonstrates how to create a header control and position it within the parent window's client area.</span></span> <span data-ttu-id="61eec-105">Você pode criar um controle de cabeçalho usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e especificando a classe da janela de [**\_ cabeçalho WC**](common-control-window-classes.md) e os [estilos de controle de cabeçalho](header-control-styles.md)apropriados.</span><span class="sxs-lookup"><span data-stu-id="61eec-105">You can create a header control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specifying the [**WC\_HEADER**](common-control-window-classes.md) window class and the appropriate [header control styles](header-control-styles.md).</span></span> <span data-ttu-id="61eec-106">Essa classe de janela é registrada quando a DLL de controle comum é carregada.</span><span class="sxs-lookup"><span data-stu-id="61eec-106">This window class is registered when the common control DLL is loaded.</span></span> <span data-ttu-id="61eec-107">Para garantir que essa DLL seja carregada, use a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="61eec-107">To ensure that this DLL is loaded, use the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="61eec-108">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="61eec-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="61eec-109">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="61eec-109">Technologies</span></span>

-   [<span data-ttu-id="61eec-110">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="61eec-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="61eec-111">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="61eec-111">Prerequisites</span></span>

-   <span data-ttu-id="61eec-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="61eec-112">C/C++</span></span>
-   <span data-ttu-id="61eec-113">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="61eec-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="61eec-114">Instruções</span><span class="sxs-lookup"><span data-stu-id="61eec-114">Instructions</span></span>


<span data-ttu-id="61eec-115">O exemplo de código C++ a seguir primeiro chama a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) para carregar a DLL de controle comum.</span><span class="sxs-lookup"><span data-stu-id="61eec-115">The following C++ code example first calls the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function to load the common control DLL.</span></span> <span data-ttu-id="61eec-116">Em seguida, ele chama a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar um controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="61eec-116">It then calls the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create a header control.</span></span> <span data-ttu-id="61eec-117">Inicialmente, o controle é oculto.</span><span class="sxs-lookup"><span data-stu-id="61eec-117">The control is initially hidden.</span></span> <span data-ttu-id="61eec-118">A mensagem de [**\_ layout HDM**](hdm-layout.md) é usada para calcular o tamanho e a posição do controle dentro da janela pai.</span><span class="sxs-lookup"><span data-stu-id="61eec-118">The [**HDM\_LAYOUT**](hdm-layout.md) message is used to calculate the size and position of the control within the parent window.</span></span> <span data-ttu-id="61eec-119">O controle é então reposicionado e torna-se visível.</span><span class="sxs-lookup"><span data-stu-id="61eec-119">The control is then repositioned and made visible.</span></span>



```C++
// DoCreateHeader - creates a header control that is positioned along 
//     the top of the parent window's client area. 
// Returns the handle to the header control. 
// hwndParent - handle to the parent window. 
// 
// Global variable 
//    g_hinst - handle to the application instance 
extern HINSTANCE g_hinst; 
//
// child-window identifier
int ID_HEADER;
//
HWND DoCreateHeader(HWND hwndParent) 
{ 
        HWND hwndHeader; 
        RECT rcParent; 
        HDLAYOUT hdl; 
        WINDOWPOS wp; 
 
        // Ensure that the common control DLL is loaded, and then create 
        // the header control. 
        INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
        icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
        icex.dwICC = ICC_LISTVIEW_CLASSES;   //set dwICC member to ICC_LISTVIEW_CLASSES    
                                             // this loads list-view and header control classes.
    InitCommonControlsEx(&icex); 
 
        if ((hwndHeader = CreateWindowEx(0, WC_HEADER, (LPCTSTR) NULL, 
                WS_CHILD | WS_BORDER | HDS_BUTTONS | HDS_HORZ, 
                0, 0, 0, 0, hwndParent, (HMENU) ID_HEADER, g_hinst, 
                (LPVOID) NULL)) == NULL) 
            return (HWND) NULL; 
 
        // Retrieve the bounding rectangle of the parent window's 
        // client area, and then request size and position values 
        // from the header control. 
        GetClientRect(hwndParent, &rcParent); 
 
        hdl.prc = &rcParent; 
        hdl.pwpos = &wp; 
        if (!SendMessage(hwndHeader, HDM_LAYOUT, 0, (LPARAM) &hdl)) 
            return (HWND) NULL; 
 
        // Set the size, position, and visibility of the header control. 
        SetWindowPos(hwndHeader, wp.hwndInsertAfter, wp.x, wp.y, 
            wp.cx, wp.cy, wp.flags | SWP_SHOWWINDOW); 
 
        return hwndHeader; 
}
```



## <a name="related-topics"></a><span data-ttu-id="61eec-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61eec-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61eec-121">Sobre controles de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="61eec-121">About Header Controls</span></span>](header-controls.md)
</dt> <dt>

[<span data-ttu-id="61eec-122">Referência de controle de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="61eec-122">Header Control Reference</span></span>](bumper-header-control-header-control-reference.md)
</dt> <dt>

[<span data-ttu-id="61eec-123">Usando controles de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="61eec-123">Using Header Controls</span></span>](using-header-controls.md)
</dt> </dl>

 

 