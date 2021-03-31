---
title: Exibindo interfaces de usuário modais
description: Exibindo interfaces de usuário modais
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Plug-ins do Windows Media Player, exibindo caixas de diálogo e de mensagens
- plug-ins, exibindo caixas de diálogo e de mensagem
- plug-ins de interface do usuário, exibindo caixas de diálogo e de mensagem
- Plug-ins de interface do usuário, exibindo caixas de diálogo e de mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d96387ca46864064c7b6ff7b9cd3dba8187eed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637244"
---
# <a name="displaying-modal-user-interfaces"></a><span data-ttu-id="e7e0c-107">Exibindo interfaces de usuário modais</span><span class="sxs-lookup"><span data-stu-id="e7e0c-107">Displaying Modal User Interfaces</span></span>

<span data-ttu-id="e7e0c-108">Plug-ins de interface do usuário não devem exibir caixas de diálogo modais ou caixas de mensagem em resposta a chamadas de método do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e7e0c-108">UI plug-ins should not display modal dialog boxes or message boxes in response to method calls from Windows Media Player.</span></span> <span data-ttu-id="e7e0c-109">Por exemplo, não exiba uma caixa de mensagem de sua implementação de **IWMPPluginUI:: Create**.</span><span class="sxs-lookup"><span data-stu-id="e7e0c-109">For example, do not display a message box from your implementation of **IWMPPluginUI::Create**.</span></span>

<span data-ttu-id="e7e0c-110">Se for necessário exibir uma caixa de diálogo ou caixa de mensagem de uma implementação de método de plug-in de interface do usuário chamada pelo Player, você deverá seguir estas etapas:</span><span class="sxs-lookup"><span data-stu-id="e7e0c-110">If you must display a dialog box or message box from a UI plug-in method implementation that is called by the Player, you must follow these steps:</span></span>

1.  <span data-ttu-id="e7e0c-111">Registre uma nova mensagem de janela usando **RegisterWindowMessage**.</span><span class="sxs-lookup"><span data-stu-id="e7e0c-111">Register a new window message using **RegisterWindowMessage**.</span></span>
2.  <span data-ttu-id="e7e0c-112">Envie a mensagem de janela que você registrou para a janela de plug-in da interface do usuário usando a **mensagem de ismessage**.</span><span class="sxs-lookup"><span data-stu-id="e7e0c-112">Send the window message you registered to your UI plug-in window using **PostMessage**.</span></span>
3.  <span data-ttu-id="e7e0c-113">Mostre a caixa de diálogo ou a caixa de mensagem do manipulador de mensagens para sua nova mensagem de janela.</span><span class="sxs-lookup"><span data-stu-id="e7e0c-113">Show the dialog box or message box from the message handler for your new window message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7e0c-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7e0c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7e0c-115">**Visão geral do plug-in da interface do usuário**</span><span class="sxs-lookup"><span data-stu-id="e7e0c-115">**UI Plug-in Overview**</span></span>](ui-plug-in-overview.md)
</dt> </dl>

 

 




