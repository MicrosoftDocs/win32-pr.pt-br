---
title: O mapa de mensagens
description: O mapa de mensagens
ms.assetid: 4640b0f5-625e-4a9e-86f5-3e75d0afb40d
keywords:
- Plug-ins do Windows Media Player, mapa de mensagens
- plug-ins, mapa de mensagens
- plug-ins de interface do usuário, mapa de mensagens
- Plug-ins de interface do usuário, mapa de mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea7fc04caf752383368ab6e51ae19c82e8c3515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005628"
---
# <a name="the-message-map"></a><span data-ttu-id="93466-107">O mapa de mensagens</span><span class="sxs-lookup"><span data-stu-id="93466-107">The Message Map</span></span>

<span data-ttu-id="93466-108">A janela de plug-in responde a vários eventos chamando métodos mapeados para as mensagens de evento correspondentes.</span><span class="sxs-lookup"><span data-stu-id="93466-108">The plug-in window responds to various events by calling methods that are mapped to corresponding event messages.</span></span> <span data-ttu-id="93466-109">O assistente fornece um mapeamento para que OnPaint e OnEraseBackground sejam chamados nos horários apropriados.</span><span class="sxs-lookup"><span data-stu-id="93466-109">The wizard provides a mapping so that OnPaint and OnEraseBackground will be called at the appropriate times.</span></span> <span data-ttu-id="93466-110">Para criar o botão de **pesquisa** e para responder a cliques dele, a seção mapa de mensagens é modificada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="93466-110">To create the **Search** button and to respond to clicks from it, the message map section is modified as follows:</span></span>


```C++
BEGIN_MSG_MAP(CPluginWindow)
    MESSAGE_HANDLER(WM_PAINT, OnPaint)
    MESSAGE_HANDLER(WM_ERASEBKGND, OnEraseBackground)
    MESSAGE_HANDLER(WM_CREATE, OnCreate)
    COMMAND_ID_HANDLER(IDC_SEARCH, OnSearch)
END_MSG_MAP()

```



## <a name="related-topics"></a><span data-ttu-id="93466-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="93466-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93466-112">**Implementando CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="93466-112">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




