---
title: A funcionalidade do aplicativo de desktop será afetada se não for executada no modo de janela
description: No Windows 10, os aplicativos do Windows não estão mais em tela inteira por padrão – em vez disso, eles são janelas e operações como minimizar, restaurar, maximizar, redimensionar (e qualquer outra operação que você sempre conseguiu fazer em qualquer outra janela de aplicativo do Windows clássica) agora é possível.
ms.assetid: 435E85DA-008B-437E-92CB-AC105855760A
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aae44fda5847e5b86616b40ab1bf4ab8cbd206b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364282"
---
# <a name="desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode"></a><span data-ttu-id="33274-103">A funcionalidade do aplicativo de desktop será afetada se não for executada no modo de janela</span><span class="sxs-lookup"><span data-stu-id="33274-103">Desktop App functionality is impacted if not run in Windowed Mode</span></span>

<span data-ttu-id="33274-104">No Windows 10, os aplicativos do Windows não estão mais em tela inteira por padrão – em vez disso, eles são janelas e operações como minimizar, restaurar, maximizar, redimensionar (e qualquer outra operação que você sempre conseguiu fazer em qualquer outra janela de aplicativo do Windows clássica) agora é possível.</span><span class="sxs-lookup"><span data-stu-id="33274-104">In Windows 10, Windows apps are no longer full-screen by default – instead, they are windowed and operations like minimizing, restoring, maximizing, resizing (and any other operation that you’ve always been able to do to any other Classic Windows application window) is now possible.</span></span>

## <a name="manifestations"></a><span data-ttu-id="33274-105">Manifestações</span><span class="sxs-lookup"><span data-stu-id="33274-105">Manifestations</span></span>

<span data-ttu-id="33274-106">A alteração mais perceptível agora é que você pode ser dimensionado para tamanhos arbitrários que não são apenas o tamanho da tela/altura da tela.</span><span class="sxs-lookup"><span data-stu-id="33274-106">The most noticeable change now is that you can get sized to arbitrary sizes that are not just the size of the screen/height of the screen.</span></span> <span data-ttu-id="33274-107">Um usuário pode redimensionar continuamente a janela do aplicativo para sua preferência (até o tamanho mínimo da janela do aplicativo).</span><span class="sxs-lookup"><span data-stu-id="33274-107">A user can continuously resize the app window to their liking (down to the app’s minimal window size).</span></span> <span data-ttu-id="33274-108">Isso é diferente do Windows 8,0 ou Windows 8.1, em que o ato de redimensionar uma janela era uma ação discreta (os usuários redimensionaram uma miniatura da janela, o que, em seguida, fazia com que a janela fosse redimensionada quando o usuário confirmou a ação).</span><span class="sxs-lookup"><span data-stu-id="33274-108">This is different from Windows 8.0 or Windows 8.1, where the act of resizing a window was a discrete action (users resized a thumbnail of the window, which then caused the window to resize once the user committed the action).</span></span> <span data-ttu-id="33274-109">Hoje em diante, quando o usuário arrasta a janela pelo canto inferior (ou outro local de borda), ele é um redimensionamento contínuo e o aplicativo recebe as mensagens de redimensionamento em uma linha, em vez da alteração de tamanho.</span><span class="sxs-lookup"><span data-stu-id="33274-109">Today instead when the user drags the window by the bottom corner (or other border location) it is a continuous resize, and the app receives resize messages in a row, rather than size change.</span></span>

## <a name="mitigations"></a><span data-ttu-id="33274-110">Atenuações</span><span class="sxs-lookup"><span data-stu-id="33274-110">Mitigations</span></span>

<span data-ttu-id="33274-111">Para mitigar isso para aplicativos do Windows 8,0 e 8,1:</span><span class="sxs-lookup"><span data-stu-id="33274-111">To mitigate this for Windows 8.0 and 8.1 apps:</span></span>

-   <span data-ttu-id="33274-112">Se o recurso esperado dentro da funcionalidade do aplicativo for interrompido, a mitigação do usuário será posicionar o aplicativo no modo de tela inteira (usando o botão "ir para a tela inteira" no canto superior direito da barra de título).</span><span class="sxs-lookup"><span data-stu-id="33274-112">If the expected feature within the app functionality is broken, then the user mitigation is to place the app into full screen mode (by using the “go full screen button” in the upper right corner of the title bar).</span></span>
-   <span data-ttu-id="33274-113">Se a inicialização do aplicativo for afetada de que ele não é aberto conforme o esperado, o usuário ainda deverá ser capaz de alternar para o modo tablet para forçar o aplicativo a ser iniciado no modo de tela inteira sem intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="33274-113">If app start-up is impacted that it does not open as expected, then the user should still be able to switch to Tablet Mode to force the app to start in full-screen mode without user intervention.</span></span>

<span data-ttu-id="33274-114">A melhor maneira de lidar com isso é alterar o aplicativo para estar ciente do fato de que ele pode ser dimensionado para locais/alturas de tamanho não-monitor (ou seja, não ter uma tabela codificada de altura/largura e esperar apenas aquelas, ou esperar também taxas codificadas).</span><span class="sxs-lookup"><span data-stu-id="33274-114">The best way to handle this is to change the app to be aware of the fact that it can be sized to non-monitor sized places/heights (i.e. don’t have a hardcoded table of height/widths and only expect those, or expect hardcoded ratios as well).</span></span> <span data-ttu-id="33274-115">Os desenvolvedores de aplicativos devem esperar que, à medida que o aplicativo é redimensionado, que outra mensagem de redimensionamento possa ocorrer logo após a entrega da mensagem de redimensionamento atual – como resultado, se o aplicativo iniciar animações durante o redimensionamento, é possível que o aplicativo receba outra mensagem de redimensionamento logo após (portanto, é importante garantir que esse tipo de situação não cause</span><span class="sxs-lookup"><span data-stu-id="33274-115">App developers should expect that as the app is being resized, that another resizing message can happen right after the current resize message gets delivered – as a result, if the app starts animations during resize, it’s possible that the app may receive another resize message right after (so it’s important to ensure that this type of situation doesn’t lead to the app crashing).</span></span>

 

 




