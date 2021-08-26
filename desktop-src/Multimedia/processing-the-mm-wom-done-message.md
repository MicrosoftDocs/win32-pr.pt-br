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
ms.openlocfilehash: c6aca93f23ed74a4a4974633d8345f2e897535e156ccc03f46eb0da92a2d2fdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037855"
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



 

 




