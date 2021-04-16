---
title: Reprodução de loop para MCIWnd
description: Reprodução de looping (MCIWnd)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d6a22e917cf764b37444bcaf4afb0393e1c1b
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106188007"
---
# <a name="looping-playback-for-mciwnd"></a><span data-ttu-id="066a0-103">Reprodução de loop para MCIWnd</span><span class="sxs-lookup"><span data-stu-id="066a0-103">Looping Playback for MCIWnd</span></span>

<span data-ttu-id="066a0-104">O MCIWnd dá suporte à reprodução como um loop contínuo.</span><span class="sxs-lookup"><span data-stu-id="066a0-104">MCIWnd supports playback as a continuous loop.</span></span> <span data-ttu-id="066a0-105">Você pode reproduzir o conteúdo de um arquivo ou dispositivo repetidamente como um loop usando a macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) em combinação com o botão **reproduzir** na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="066a0-105">You can play the content of a file or device repeatedly as a loop by using the [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) macro in combination with the **Play** button on the toolbar.</span></span> <span data-ttu-id="066a0-106">O dispositivo de reprodução de vídeo, MCIAVI, dá suporte a loops de reprodução.</span><span class="sxs-lookup"><span data-stu-id="066a0-106">The video playback device, MCIAVI, supports playback loops.</span></span> <span data-ttu-id="066a0-107">Para determinar se a reprodução contínua foi ativada, use a macro [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .</span><span class="sxs-lookup"><span data-stu-id="066a0-107">To determine if continuous playback has been activated, use the [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) macro.</span></span>

 

 




