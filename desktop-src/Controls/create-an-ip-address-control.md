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
# <a name="how-to-create-an-ip-address-control"></a>Como criar um controle de endereço IP

Este tópico demonstra como criar uma instância de um controle de endereço IP.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Antes de criar um controle de endereço IP, carregue a DLL de controles comuns chamando [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex). Em seguida, use a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar um controle de endereço IP de instância. O nome da classe para o controle é [**WC \_ IPAddress**](common-control-window-classes.md). Use o [**estilo \_ filho WS**](/windows/desktop/winmsg/window-styles) , porque não há uma constante de estilo específica associada ao controle de endereço IP.

No exemplo de código C++ a seguir, a função definida pelo aplicativo primeiro chama [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) e define o membro **DwICC** da estrutura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) para [**\_ \_ classes de Internet ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), que especifica a classe de endereço IP. Em seguida, ele chama [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar uma instância do controle de endereço IP.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle de endereço IP](bumper-ip-address-control-ip-address-control-reference.md)
</dt> <dt>

[Sobre controles de endereço IP](ip-address-controls.md)
</dt> <dt>

[Usando controles de endereço IP](using-ip-address-controls.md)
</dt> </dl>

 

 