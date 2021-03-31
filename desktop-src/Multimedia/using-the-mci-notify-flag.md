---
title: Usando o sinalizador de MCI_NOTIFY
description: Usando o \_ sinalizador de notificação MCI
ms.assetid: 1d1803c8-f315-463e-ae0d-a258aa3af3c9
keywords:
- Sinalizador de MCI_NOTIFY
- MCI_PLAY comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472613d2e6efcd6b30c88ed64dfa7875b4742527
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822403"
---
# <a name="using-the-mci_notify-flag"></a><span data-ttu-id="f7d06-105">Usando o \_ sinalizador de notificação MCI</span><span class="sxs-lookup"><span data-stu-id="f7d06-105">Using the MCI\_NOTIFY Flag</span></span>

<span data-ttu-id="f7d06-106">O exemplo a seguir mostra como o \_ sinalizador de notificação MCI é usado com o comando [**MCI \_ Play**](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="f7d06-106">The following example shows how the MCI\_NOTIFY flag is used with the [**MCI\_PLAY**](mci-play.md) command.</span></span> <span data-ttu-id="f7d06-107">O identificador para o procedimento de janela que processará a mensagem [**mm \_ MCINOTIFY**](mm-mcinotify.md) é especificado em *hWnd*.</span><span class="sxs-lookup"><span data-stu-id="f7d06-107">The handle to the window procedure that will process the [**MM\_MCINOTIFY**](mm-mcinotify.md) message is specified in *hwnd*.</span></span>


```C++
MCI_DGV_PLAY_PARMS mciPlay; 
DWORD dwFlags; 
 
mciPlay.dwCallback = MAKELONG(hwnd, 0); 
dwFlags = MCI_NOTIFY; 
 
mciSendCommand(wMCIDeviceID, MCI_PLAY, dwFlags, (DWORD)(LPSTR)&mciPlay); 
```



 

 




