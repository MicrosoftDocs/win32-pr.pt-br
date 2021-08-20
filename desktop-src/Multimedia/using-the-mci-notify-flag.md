---
title: Usando o sinalizador de MCI_NOTIFY
description: Usando o \_ sinalizador de notificação MCI
ms.assetid: 1d1803c8-f315-463e-ae0d-a258aa3af3c9
keywords:
- Sinalizador de MCI_NOTIFY
- MCI_PLAY comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b0e7269ee7d80dd47372d9210fbdbc1332b3a88a96e2a17d6719c9945ab30aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136134"
---
# <a name="using-the-mci_notify-flag"></a>Usando o \_ sinalizador de notificação MCI

O exemplo a seguir mostra como o \_ sinalizador de notificação MCI é usado com o comando [**MCI \_ Play**](mci-play.md) . O identificador para o procedimento de janela que processará a mensagem [**mm \_ MCINOTIFY**](mm-mcinotify.md) é especificado em *hWnd*.


```C++
MCI_DGV_PLAY_PARMS mciPlay; 
DWORD dwFlags; 
 
mciPlay.dwCallback = MAKELONG(hwnd, 0); 
dwFlags = MCI_NOTIFY; 
 
mciSendCommand(wMCIDeviceID, MCI_PLAY, dwFlags, (DWORD)(LPSTR)&mciPlay); 
```



 

 




