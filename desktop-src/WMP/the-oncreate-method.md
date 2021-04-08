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
# <a name="the-oncreate-method"></a><span data-ttu-id="c0e07-108">O método OnCreate</span><span class="sxs-lookup"><span data-stu-id="c0e07-108">The OnCreate Method</span></span>

<span data-ttu-id="c0e07-109">O método OnCreate é chamado quando a janela de plug-in é criada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="c0e07-109">The OnCreate method is called when the plug-in window is first created.</span></span>

<span data-ttu-id="c0e07-110">O código a seguir é usado para implementar esse método:</span><span class="sxs-lookup"><span data-stu-id="c0e07-110">The following code is used to implement this method:</span></span>


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



<span data-ttu-id="c0e07-111">Esse método cria o botão de **pesquisa** e o associa com a \_ ID de comando de pesquisa da IDC, que é definida no início do arquivo:</span><span class="sxs-lookup"><span data-stu-id="c0e07-111">This method creates the **Search** button and associates it with the IDC\_SEARCH command ID, which is defined at the beginning of the file:</span></span>


```C++
#define IDC_SEARCH 2000

```



<span data-ttu-id="c0e07-112">Essa ID de comando é mapeada para o método onsearch na seção de mapa de mensagens descrita anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c0e07-112">This command ID is mapped to the OnSearch method in the message map section described previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0e07-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0e07-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0e07-114">**Implementando CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="c0e07-114">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




