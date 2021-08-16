---
title: Criando uma função de retorno de chamada de erro
description: Criando uma função de retorno de chamada de erro
ms.assetid: a489ec94-c566-44b1-aa93-9b43f23de744
keywords:
- Macro capSetCallbackOnError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86b2c3445bdd4d93db36307827e648fe804e82ac8dfb06011bd7a920ab7c8e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144689"
---
# <a name="creating-an-error-callback-function"></a>Criando uma função de retorno de chamada de erro

O exemplo a seguir é uma função de retorno de chamada de erro simples. Registre esse retorno de chamada usando a [**macro capSetCallbackOnError.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror)


```
TCHAR gachBuffer[100]; // Global buffer.

// ErrorCallbackProc: error callback function. 
// hWnd:              capture window handle. 
// nErrID:            error code for the encountered error. 
// lpErrorText:       error text string for the encountered error. 
// 
LRESULT PASCAL ErrorCallbackProc(HWND hWnd, int nErrID,
    LPTSTR lpErrorText) 
{ 
 
    if (!hWnd) 
        return FALSE; 
 
    if (nErrID == 0)            // Starting a new major function. 
        return TRUE;            // Clear out old errors. 
 
    // Show the error identifier and text. 
    _stprintf_s(gachBuffer, TEXT("Error# %d"), nErrID); 
 
    MessageBox(hWnd, lpErrorText, gachBuffer, 
        MB_OK | MB_ICONEXCLAMATION); 
 
    return (LRESULT) TRUE; 
} 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a Captura de Vídeo](using-video-capture.md)
</dt> </dl>

 

 




