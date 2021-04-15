---
title: Processando a mensagem de MM_WOM_DONE
description: Processando a \_ mensagem mm wom \_ concluído
ms.assetid: 215167d0-3020-453d-b6b3-cee5803836c9
keywords:
- áudio de onda, mensagens
- áudio auxiliar, mensagens
- áudio de forma de onda, mensagem de MM_WOM_DONE
- áudio auxiliar, mensagem de MM_WOM_DONE
- MM_WOM_DONE mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e909777c115b6b10500e081a08bde6cfe24b00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453598"
---
# <a name="processing-the-mm_wom_done-message"></a>Processando a \_ mensagem mm wom \_ concluído

O exemplo a seguir mostra como processar a mensagem [**mm \_ wom \_ concluído**](mm-wom-done.md) . Este exemplo supõe que o aplicativo não reproduza vários blocos de dados, portanto, pode fechar o dispositivo de saída depois de reproduzir um único bloco de dados.


```C++
// WndProc--Main window procedure. 
LRESULT FAR PASCAL WndProc(HWND hWnd, UINT msg, WPARAM wParam, 
    LPARAM lParam) 
{ 
switch (msg) 
{ 
    case MM_WOM_DONE: 
 
    // A waveform-audio data block has been played and 
    // can now be freed. 
    waveOutUnprepareHeader((HWAVEOUT) wParam, 
        (LPWAVEHDR) lParam, sizeof(WAVEHDR) ); 
    
    // Free hData memory. 
    
    waveOutClose((HWAVEOUT) wParam); 
    break; 
    } 
    return DefWindowProc(hWnd, msg, wParam, lParam); 
} 
```



 

 




