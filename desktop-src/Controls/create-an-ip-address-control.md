---
title: Como criar um controle de endereço IP
description: Este tópico demonstra como criar uma instância de um controle de endereço IP.
ms.assetid: E4DBECA6-B3F2-405F-8D95-32FA2334114D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8427a5695c0b9c79c19d328f4abc2ab0ffb2e5a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104085008"
---
# <a name="how-to-create-an-ip-address-control"></a><span data-ttu-id="7cdf6-103">Como criar um controle de endereço IP</span><span class="sxs-lookup"><span data-stu-id="7cdf6-103">How to Create an IP Address Control</span></span>

<span data-ttu-id="7cdf6-104">Este tópico demonstra como criar uma instância de um controle de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="7cdf6-104">This topic demonstrates how to create an instance of an IP address control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7cdf6-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="7cdf6-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7cdf6-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="7cdf6-106">Technologies</span></span>

-   [<span data-ttu-id="7cdf6-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="7cdf6-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7cdf6-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="7cdf6-108">Prerequisites</span></span>

-   <span data-ttu-id="7cdf6-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="7cdf6-109">C/C++</span></span>
-   <span data-ttu-id="7cdf6-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="7cdf6-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7cdf6-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="7cdf6-111">Instructions</span></span>


<span data-ttu-id="7cdf6-112">Antes de criar um controle de endereço IP, carregue a DLL de controles comuns chamando [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span><span class="sxs-lookup"><span data-stu-id="7cdf6-112">Before creating an IP address control, load the common controls DLL by calling [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span></span> <span data-ttu-id="7cdf6-113">Em seguida, use a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar um controle de endereço IP de instância.</span><span class="sxs-lookup"><span data-stu-id="7cdf6-113">Then use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create an instance IP address control.</span></span> <span data-ttu-id="7cdf6-114">O nome da classe para o controle é [**WC \_ IPAddress**](common-control-window-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7cdf6-114">The class name for the control is [**WC\_IPADDRESS**](common-control-window-classes.md).</span></span> <span data-ttu-id="7cdf6-115">Use o [**estilo \_ filho WS**](/windows/desktop/winmsg/window-styles) , porque não há uma constante de estilo específica associada ao controle de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="7cdf6-115">Use the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style, because there is no specific style constant associated with the IP address control.</span></span>

<span data-ttu-id="7cdf6-116">No exemplo de código C++ a seguir, a função definida pelo aplicativo primeiro chama [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) e define o membro **DwICC** da estrutura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) para [**\_ \_ classes de Internet ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), que especifica a classe de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="7cdf6-116">In the following C++ code example, the application-defined function first calls [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) and sets the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure to [**ICC\_INTERNET\_CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), which specifies the IP address class.</span></span> <span data-ttu-id="7cdf6-117">Em seguida, ele chama [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar uma instância do controle de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="7cdf6-117">It then calls [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) to create an instance of the IP address control.</span></span>


```C++
// CreateIPAdressFld - creates a IPAddress control.
// Returns the handle to the new control
// TO DO:  calling procedure needs to check whether the handle is NULL, in case 
// of an error in creation.
// int xcoord, ycoord the coordinates of location of the control in the parent window
// HINST hInst is the global handle to the application instance.
// HWND  hWndParent is the handle to the control's parent window. 
//
//
HWND CreateIPAddressFld (HWND hwndParent, int xcoord, int ycoord) 
{     
     
    INITCOMMONCONTROLSEX icex;
    
    // Ensure that the common control DLL is loaded. 
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC  = ICC_INTERNET_CLASSES ;
    InitCommonControlsEx(&icex); 
    
    // Create the IPAddress control.        
    HWND hWndIPAddressFld = CreateWindow(WC_IPADDRESS, 
                                L"", 
                                WS_CHILD | WS_OVERLAPPED | WS_VISIBLE, 
                                xcoord, 
                                ycoord,
                                150, 
                                20,  
                                hwndParent, 
                                NULL, 
                                hInst, 
                                NULL); 
                                
    return (hWndIPAddressFld);
}
```



## <a name="related-topics"></a><span data-ttu-id="7cdf6-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cdf6-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cdf6-119">Referência de controle de endereço IP</span><span class="sxs-lookup"><span data-stu-id="7cdf6-119">IP Address Control Reference</span></span>](bumper-ip-address-control-ip-address-control-reference.md)
</dt> <dt>

[<span data-ttu-id="7cdf6-120">Sobre controles de endereço IP</span><span class="sxs-lookup"><span data-stu-id="7cdf6-120">About IP Address Controls</span></span>](ip-address-controls.md)
</dt> <dt>

[<span data-ttu-id="7cdf6-121">Usando controles de endereço IP</span><span class="sxs-lookup"><span data-stu-id="7cdf6-121">Using IP Address Controls</span></span>](using-ip-address-controls.md)
</dt> </dl>

 

 