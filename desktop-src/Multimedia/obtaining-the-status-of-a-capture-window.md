---
title: Obtendo o status de uma janela de captura
description: Obtendo o status de uma janela de captura
ms.assetid: 5095dbd2-7cd4-48b6-bbb4-1f0bddfcfd06
keywords:
- macro capGetStatus
- Estrutura CAPSTATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f848898247ad8ea2ddbb0dde7a13c08b6a7274
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917215"
---
# <a name="obtaining-the-status-of-a-capture-window"></a>Obtendo o status de uma janela de captura

O exemplo a seguir usa a função [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) para definir o tamanho da janela de captura para as dimensões gerais do fluxo de vídeo de entrada com base nas informações retornadas pela macro [**CapGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) na estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) .


```C++
CAPSTATUS CapStatus;

capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS)); 

SetWindowPos(hWndC, NULL, 0, 0, CapStatus.uiImageWidth, 
    CapStatus.uiImageHeight, SWP_NOZORDER | SWP_NOMOVE); 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 