---
title: Criando uma tabela de função virtual para um manipulador de fluxo
description: Criando uma tabela de função virtual para um manipulador de fluxo
ms.assetid: 8f43b0d4-6710-4175-8da0-aafd6b6d753a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8281cee5a385a6a37e03e657facf4790fed504b18e38fb7b1825a2dce5690fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144719"
---
# <a name="creating-a-virtual-function-table-for-a-stream-handler"></a>Criando uma tabela de função virtual para um manipulador de fluxo

O exemplo a seguir (escrito em C) mostra como um aplicativo (AVIBall) cria a tabela de funções virtuais usada para referenciar seus serviços.


```C++
HRESULT STDMETHODCALLTYPE AVIBallQueryInterface (PAVISTREAM ps, 
    REFIID riid, LPVOID FAR* ppvObj); 
HRESULT STDMETHODCALLTYPE AVIBallCreate (PAVISTREAM ps, 
    LONG lParam1, LONG lParam2); 
ULONG STDMETHODCALLTYPE AVIBallAddRef (PAVISTREAM ps); 
ULONG STDMETHODCALLTYPE AVIBallRelease (PAVISTREAM ps); 
HRESULT STDMETHODCALLTYPE AVIBallInfo (PAVISTREAM ps, 
    AVIStreamHeader FAR * psi, LONG lSize); 
LONG STDMETHODCALLTYPE AVIBallFindSample (PAVISTREAM ps, 
    LONG lPos, LONG lFlags); 
HRESULT STDMETHODCALLTYPE AVIBallReadFormat (PAVISTREAM ps, 
    LONG lPos, LPVOID lpFormat, LONG FAR *lpcbFormat); 
HRESULT STDMETHODCALLTYPE AVIBallSetFormat (PAVISTREAM ps, 
    LONG lPos, LPVOID lpFormat, LONG cbFormat); 
HRESULT STDMETHODCALLTYPE AVIBallRead (PAVISTREAM ps, 
    LONG lStart, LONG lSamples, LPVOID lpBuffer, LONG cbBuffer, 
    LONG FAR * plBytes,LONG FAR * plSamples); 
HRESULT STDMETHODCALLTYPE AVIBallWrite (PAVISTREAM ps, LONG lStart, 
    LONG lSamples, LPVOID lpBuffer, LONG cbBuffer, DWORD dwFlags); 
HRESULT STDMETHODCALLTYPE AVIBallDelete (PAVISTREAM ps, 
    LONG lStart, LONG lSamples); 
HRESULT STDMETHODCALLTYPE AVIBallReadData (PAVISTREAM ps, 
    DWORD fcc, LPVOID lp,LONG FAR *lpcb); 
HRESULT STDMETHODCALLTYPE AVIBallWriteData (PAVISTREAM ps, 
    DWORD fcc, LPVOID lp,LONG cb); 
 
IAVIStreamVtbl AVIBallHandler = { 
    AVIBallQueryInterface,  // Function pointer for ::QueryInterface 
    AVIBallAddRef,          // Function pointer for ::AddRef 
    AVIBallRelease,         // Function pointer for ::Release 
    AVIBallCreate,          // Function pointer for ::Create 
    AVIBallInfo,            // Function pointer for ::Info 
    AVIBallFindSample,      // Function pointer for ::FindSample 
    AVIBallReadFormat,      // Function pointer for ::ReadFormat 
    AVIBallSetFormat,       // Function pointer for ::SetFormat 
    AVIBallRead,            // Function pointer for ::Read 
    AVIBallWrite,           // Function pointer for ::Write 
    AVIBallDelete,          // Function pointer for ::Delete 
    AVIBallReadData,        // Function pointer for ::ReadData 
    AVIBallWriteData        // Function pointer for ::WriteData 
}; 
```



Os manipuladores de arquivo usam um procedimento semelhante, exceto que usam uma definição diferente para a tabela de funções virtuais.

 

 




