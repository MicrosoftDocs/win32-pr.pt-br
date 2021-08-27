---
title: Obtendo o status de uma janela de captura
description: Obtendo o status de uma janela de captura
ms.assetid: 5095dbd2-7cd4-48b6-bbb4-1f0bddfcfd06
keywords:
- macro capGetStatus
- Estrutura CAPSTATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8effedac3950f0f57aaa6e57ccd5a93fe3044982c3d6ec6d6bb69b56024a1255
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038366"
---
# <a name="obtaining-the-status-of-a-capture-window"></a>Obtendo o status de uma janela de captura

O exemplo a seguir usa a função [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) para definir o tamanho da janela de captura para as dimensões gerais do fluxo de vídeo de entrada com base nas informações retornadas pela macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) na estrutura [**CAPSTATUS.**](/windows/win32/api/vfw/ns-vfw-capstatus)


```C++
CAPSTATUS CapStatus;

capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS)); 

SetWindowPos(hWndC, NULL, 0, 0, CapStatus.uiImageWidth, 
    CapStatus.uiImageHeight, SWP_NOZORDER | SWP_NOMOVE); 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a Captura de Vídeo](using-video-capture.md)
</dt> </dl>

 

 