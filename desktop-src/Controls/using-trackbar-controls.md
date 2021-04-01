---
title: Usando controles TrackBar
description: Esta seção fornece detalhes de implementação e exemplos para controles TrackBar.
ms.assetid: 28078f3e-a3d1-4bb5-96c6-2191ff9f8d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 296d667a495dce918bdcfcf0391638eef8a3c6e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635742"
---
# <a name="using-trackbar-controls"></a><span data-ttu-id="ce8c0-103">Usando controles TrackBar</span><span class="sxs-lookup"><span data-stu-id="ce8c0-103">Using Trackbar Controls</span></span>

<span data-ttu-id="ce8c0-104">Esta seção fornece detalhes de implementação e exemplos para controles TrackBar.</span><span class="sxs-lookup"><span data-stu-id="ce8c0-104">This section provides implementation details and examples for Trackbar controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ce8c0-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ce8c0-105">In this section</span></span>



| <span data-ttu-id="ce8c0-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="ce8c0-106">Topic</span></span>                                                                                                  | <span data-ttu-id="ce8c0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce8c0-107">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce8c0-108">Como criar um TrackBar</span><span class="sxs-lookup"><span data-stu-id="ce8c0-108">How to Create a Trackbar</span></span>](create-a-trackbar.md)<br/>                                           | <span data-ttu-id="ce8c0-109">Quando o TrackBar é criado, seu intervalo e seu intervalo de seleção são inicializados.</span><span class="sxs-lookup"><span data-stu-id="ce8c0-109">When the trackbar is created, both its range and its selection range are initialized.</span></span> <span data-ttu-id="ce8c0-110">O tamanho da página também é definido neste momento.</span><span class="sxs-lookup"><span data-stu-id="ce8c0-110">The page size is also set at this time.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="ce8c0-111">Como processar mensagens de notificação TrackBar</span><span class="sxs-lookup"><span data-stu-id="ce8c0-111">How to Process Trackbar Notification Messages</span></span>](process-trackbar-notification-messages.md)<br/> | <span data-ttu-id="ce8c0-112">Trackbars Notifique a janela pai das ações do usuário enviando a mensagem pai a [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="ce8c0-112">Trackbars notify their parent window of user actions by sending the parent a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span> <br/>                                                                                                            |
| [<span data-ttu-id="ce8c0-113">Como limitar o movimento do controle deslizante</span><span class="sxs-lookup"><span data-stu-id="ce8c0-113">How to Limit Slider Movement</span></span>](limit-slider-movement.md)<br/>                                   | <span data-ttu-id="ce8c0-114">Conforme descrito em [sobre controles TrackBar](trackbar-controls.md), é possível definir parte do intervalo TrackBar como um intervalo de seleção.</span><span class="sxs-lookup"><span data-stu-id="ce8c0-114">As described in [About Trackbar Controls](trackbar-controls.md), it is possible to set off part of the trackbar range as a selection range.</span></span> <span data-ttu-id="ce8c0-115">Uma finalidade de um intervalo de seleção pode ser limitar a movimentação do controle deslizante, tornando algumas partes dos limites completos do intervalo.</span><span class="sxs-lookup"><span data-stu-id="ce8c0-115">One purpose of a selection range might be to limit movement of the slider, making some parts of the full range off limits.</span></span> <br/> |
| [<span data-ttu-id="ce8c0-116">Como usar o Buddy Windows</span><span class="sxs-lookup"><span data-stu-id="ce8c0-116">How to Use Buddy Windows</span></span>](use-buddy-windows.md)<br/>                                           | <span data-ttu-id="ce8c0-117">Ao definir outros controles como Buddy Windows para um TrackBar, você pode posicionar automaticamente esses controles nas extremidades do TrackBar como rótulos.</span><span class="sxs-lookup"><span data-stu-id="ce8c0-117">By setting other controls as buddy windows for a trackbar, you can automatically position those controls at the ends of the trackbar as labels.</span></span><br/>                                                                                                                          |



 

 

 





