---
title: Definindo o escopo de reprodução
description: Definindo o escopo de reprodução
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- Macro MCIWndPlayFrom
- Macro MCIWndPlayTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518fc80588147c4ccbbca619452b714333a8a34d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916245"
---
# <a name="defining-playback-scope"></a><span data-ttu-id="2f720-105">Definindo o escopo de reprodução</span><span class="sxs-lookup"><span data-stu-id="2f720-105">Defining Playback Scope</span></span>

<span data-ttu-id="2f720-106">O MCIWnd fornece macros que permitem que você defina o *escopo* de reprodução.</span><span class="sxs-lookup"><span data-stu-id="2f720-106">MCIWnd provides macros that allow you to define the playback *scope*.</span></span> <span data-ttu-id="2f720-107">O escopo é a parte da reprodução que você deseja reproduzir.</span><span class="sxs-lookup"><span data-stu-id="2f720-107">The scope is the portion of the playback you want to play.</span></span> <span data-ttu-id="2f720-108">Por exemplo, você pode reproduzir o conteúdo de uma posição diferente da posição inicial usando a macro [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) .</span><span class="sxs-lookup"><span data-stu-id="2f720-108">For example, you can play the content from a position other than the beginning position by using the [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) macro.</span></span> <span data-ttu-id="2f720-109">Essa macro passa para a posição especificada, começa a reprodução e continua até o final do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2f720-109">This macro moves to the specified position, begins playback, and continues to the end of the content.</span></span> <span data-ttu-id="2f720-110">Da mesma forma, você pode reproduzir o conteúdo para um ponto de extremidade especificado usando a macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) .</span><span class="sxs-lookup"><span data-stu-id="2f720-110">Similarly, you can play the content to a specified end point by using the [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macro.</span></span> <span data-ttu-id="2f720-111">Essa macro começa na posição de reprodução atual e é reproduzida até atingir a posição especificada ou o final do conteúdo é atingido, o que vier primeiro.</span><span class="sxs-lookup"><span data-stu-id="2f720-111">This macro starts at the current playback position and plays until it reaches the specified position or the end of the content is reached, whichever comes first.</span></span>

<span data-ttu-id="2f720-112">Além disso, você pode definir as posições inicial e final usando a macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .</span><span class="sxs-lookup"><span data-stu-id="2f720-112">Also, you can define both the beginning and ending positions by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span> <span data-ttu-id="2f720-113">Essa macro é movida para a posição inicial especificada e é reproduzida até que a posição final especificada ou o final do conteúdo seja atingido.</span><span class="sxs-lookup"><span data-stu-id="2f720-113">This macro moves to the specified starting position and plays until the specified ending position or the end of the content is reached.</span></span>

 

 




