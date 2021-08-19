---
title: O método OnCreate
description: O método OnCreate
ms.assetid: b23546b3-968f-41d8-ba07-3d694152c3ed
keywords:
- Windows Media Player plug-ins, método OnCreate
- plug-ins, método OnCreate
- plug-ins de interface do usuário, método OnCreate
- Plug-ins de interface do usuário, método OnCreate
- Método OnCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac52b1c58c6799f89d29fb1ee24c09767fee26729e760b2b454f1a359bd57596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118104"
---
# <a name="the-oncreate-method"></a>O método OnCreate

O método OnCreate é chamado quando a janela de plug-in é criada pela primeira vez.

O código a seguir é usado para implementar esse método:


```C++
LRESULT OnCreate(UINT uMsg, WPARAM wParam, LPARAM lParam, BOOL& bHandled)
{
    HWND hCtrl = ::CreateWindowEx(0L, _T("BUTTON"), _T("Search"),
        WS_CHILD | BS_PUSHBUTTON, 10, 10, 100, 30, m_hWnd, 
        (HMENU)IDC_SEARCH, _Module.GetResourceInstance(), NULL);
    ::ShowWindow(hCtrl, SW_SHOW );
    return 0;
}

```



Esse método cria o **botão Pesquisar** e o associa à ID do comando SEARCH do IDC, que é definida no início \_ do arquivo:


```C++
#define IDC_SEARCH 2000

```



Essa ID de comando é mapeada para o método OnSearch na seção mapa de mensagens descrita anteriormente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




