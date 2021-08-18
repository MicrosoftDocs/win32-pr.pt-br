---
title: Como usar controles de barra de progresso
description: Este tópico explica como usar uma barra de progresso para indicar o progresso de uma operação de análise de arquivo demorada.
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e65d47d6b41422853d401a1fb2686e03e3d3f5bc378b78b7ba762b86fc7ffe30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826416"
---
# <a name="how-to-use-progress-bar-controls"></a>Como usar controles de barra de progresso

Este tópico explica como usar uma barra de progresso para indicar o progresso de uma operação de análise de arquivo demorada.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Programação de interface do usuário

## <a name="instructions"></a>Instruções

### <a name="create-a-progress-bar-control"></a>Criar um controle de barra de progresso

O código de exemplo a seguir cria uma barra de progresso e a posiciona ao longo da parte inferior da área do cliente da janela pai. A altura da barra de progresso baseia-se na altura do bitmap de seta usado em uma barra de rolagem. O intervalo é baseado no tamanho do arquivo dividido por 2.048, que é o tamanho de cada "parte" dos dados lidos a partir do arquivo. O exemplo também define um incremento e avança a posição atual da barra de progresso pelo incremento após a análise de cada parte.


```C++
// ParseALargeFile - uses a progress bar to indicate the progress of a parsing operation.
//
// Returns TRUE if successful, or FALSE otherwise.
//
// hwndParent - parent window of the progress bar.
//
// lpszFileName - name of the file to parse. 
// 
// Global variable 
//     g_hinst - instance handle.
//

extern HINSTANCE g_hinst; 

BOOL ParseALargeFile(HWND hwndParent, LPTSTR lpszFileName) 
{ 
    RECT rcClient;  // Client area of parent window.
    int cyVScroll;  // Height of scroll bar arrow.
    HWND hwndPB;    // Handle of progress bar.
    HANDLE hFile;   // Handle of file.
    DWORD cb;       // Size of file and count of bytes read.
    LPCH pch;       // Address of data read from file.
    LPCH pchTmp;    // Temporary pointer.

    // Ensure that the common control DLL is loaded, and create a progress bar 
    // along the bottom of the client area of the parent window. 
    //
    // Base the height of the progress bar on the height of a scroll bar arrow.
    
    InitCommonControls(); 
    
    GetClientRect(hwndParent, &rcClient); 
    
    cyVScroll = GetSystemMetrics(SM_CYVSCROLL); 

    hwndPB = CreateWindowEx(0, PROGRESS_CLASS, (LPTSTR) NULL, 
                            WS_CHILD | WS_VISIBLE, rcClient.left, 
                            rcClient.bottom - cyVScroll, 
                            rcClient.right, cyVScroll, 
                            hwndParent, (HMENU) 0, g_hinst, NULL);

    // Open the file for reading, and retrieve the size of the file. 

    hFile = CreateFile(lpszFileName, GENERIC_READ, FILE_SHARE_READ, 
                       (LPSECURITY_ATTRIBUTES) NULL, OPEN_EXISTING, 
                       FILE_ATTRIBUTE_NORMAL, (HANDLE) NULL); 

    if (hFile == (HANDLE) INVALID_HANDLE_VALUE)
        return FALSE; 

    cb = GetFileSize(hFile, (LPDWORD) NULL); 

    // Set the range and increment of the progress bar. 

    SendMessage(hwndPB, PBM_SETRANGE, 0, MAKELPARAM(0, cb / 2048));
    
    SendMessage(hwndPB, PBM_SETSTEP, (WPARAM) 1, 0); 

    // Parse the file. 
    pch = (LPCH) LocalAlloc(LPTR, sizeof(char) * 2048); 
    
    pchTmp = pch; 
    
    do { 
        ReadFile(hFile, pchTmp, sizeof(char) * 2048, &cb, (LPOVERLAPPED) NULL);
        
        // TODO: Write an error handler to check that all the
        // requested data was read.
        //
        // Include here any code that parses the
        // file. 
        //  
        //  
        //  
        // Advance the current position of the progress bar by the increment.
        
        SendMessage(hwndPB, PBM_STEPIT, 0, 0); 
        
    } while (cb); 

    CloseHandle((HANDLE) hFile);
    
    DestroyWindow(hwndPB);

    return TRUE; 
}
```



## <a name="remarks"></a>Comentários

Você deve se certificar de usar a função [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) corretamente para garantir a segurança do seu aplicativo. Por exemplo, no código de exemplo, você deve verificar para ter certeza de que `ReadFile` realmente lê todos os dados solicitados.

Observe também que o quarto parâmetro de [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)— ( \_ atributos LPSECURITY)**NULL**— define valores de segurança padrão. Se você precisar de configurações de segurança específicas, deverá definir os valores apropriados nos membros da estrutura. Chame **sizeof** para definir o tamanho correto da estrutura **de \_ atributos LPSECURITY** .

para obter mais informações, consulte [considerações de segurança: controles do Microsoft Windows](sec-comctls.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de barra de progresso](using-progress-bar-controls.md)
</dt> <dt>

[considerações de segurança: controles do Microsoft Windows](sec-comctls.md)
</dt> </dl>

 

 