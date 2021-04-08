---
title: O método OnCreate
description: O método OnCreate
ms.assetid: b23546b3-968f-41d8-ba07-3d694152c3ed
keywords:
- Plug-ins do Windows Media Player, método OnCreate
- plug-ins, método OnCreate
- plug-ins de interface do usuário, método OnCreate
- Plug-ins de interface do usuário, método OnCreate
- Método OnCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d896ed9ebc6e9dc2bff9ff24ad23d50f7905c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822315"
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



Esse método cria o botão de **pesquisa** e o associa com a \_ ID de comando de pesquisa da IDC, que é definida no início do arquivo:


```C++
#define IDC_SEARCH 2000

```



Essa ID de comando é mapeada para o método onsearch na seção de mapa de mensagens descrita anteriormente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




