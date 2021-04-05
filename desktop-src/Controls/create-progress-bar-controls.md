---
title: Como usar controles de barra de progresso
description: Este tópico explica como usar uma barra de progresso para indicar o progresso de uma operação de análise de arquivo demorada.
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c71ff33a14f2d2af5fa8735c5197c50acaa948b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917730"
---
# <a name="how-to-use-progress-bar-controls"></a><span data-ttu-id="1bea4-103">Como usar controles de barra de progresso</span><span class="sxs-lookup"><span data-stu-id="1bea4-103">How to Use Progress Bar Controls</span></span>

<span data-ttu-id="1bea4-104">Este tópico explica como usar uma barra de progresso para indicar o progresso de uma operação de análise de arquivo demorada.</span><span class="sxs-lookup"><span data-stu-id="1bea4-104">This topic explains how to use a progress bar to indicate the progress of a lengthy file-parsing operation.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1bea4-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="1bea4-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1bea4-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="1bea4-106">Technologies</span></span>

-   [<span data-ttu-id="1bea4-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="1bea4-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1bea4-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="1bea4-108">Prerequisites</span></span>

-   <span data-ttu-id="1bea4-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="1bea4-109">C/C++</span></span>
-   <span data-ttu-id="1bea4-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="1bea4-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1bea4-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="1bea4-111">Instructions</span></span>

### <a name="create-a-progress-bar-control"></a><span data-ttu-id="1bea4-112">Criar um controle de barra de progresso</span><span class="sxs-lookup"><span data-stu-id="1bea4-112">Create a Progress Bar Control</span></span>

<span data-ttu-id="1bea4-113">O código de exemplo a seguir cria uma barra de progresso e a posiciona ao longo da parte inferior da área do cliente da janela pai.</span><span class="sxs-lookup"><span data-stu-id="1bea4-113">The following example code creates a progress bar and positions it along the bottom of the parent window's client area.</span></span> <span data-ttu-id="1bea4-114">A altura da barra de progresso baseia-se na altura do bitmap de seta usado em uma barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="1bea4-114">The height of the progress bar is based on the height of the arrow bitmap used in a scroll bar.</span></span> <span data-ttu-id="1bea4-115">O intervalo é baseado no tamanho do arquivo dividido por 2.048, que é o tamanho de cada "parte" dos dados lidos a partir do arquivo.</span><span class="sxs-lookup"><span data-stu-id="1bea4-115">The range is based on the size of the file divided by 2,048, which is the size of each "chunk" of data that is read from the file.</span></span> <span data-ttu-id="1bea4-116">O exemplo também define um incremento e avança a posição atual da barra de progresso pelo incremento após a análise de cada parte.</span><span class="sxs-lookup"><span data-stu-id="1bea4-116">The example also sets an increment and advances the current position of the progress bar by the increment after parsing each chunk.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="1bea4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bea4-117">Remarks</span></span>

<span data-ttu-id="1bea4-118">Você deve se certificar de usar a função [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) corretamente para garantir a segurança do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1bea4-118">You must make sure to use the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) function correctly, to ensure the security of your application.</span></span> <span data-ttu-id="1bea4-119">Por exemplo, no código de exemplo, você deve verificar para ter certeza de que `ReadFile` realmente lê todos os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="1bea4-119">For instance, in the example code, you should check to make sure that `ReadFile` actually reads all of the requested data.</span></span>

<span data-ttu-id="1bea4-120">Observe também que o quarto parâmetro de [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)— ( \_ atributos LPSECURITY)**NULL**— define valores de segurança padrão.</span><span class="sxs-lookup"><span data-stu-id="1bea4-120">Also notice that the fourth parameter of [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)—(LPSECURITY\_ATTRIBUTES)**NULL**—sets default security values.</span></span> <span data-ttu-id="1bea4-121">Se você precisar de configurações de segurança específicas, deverá definir os valores apropriados nos membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="1bea4-121">If you need specific security settings, you must set the appropriate values in the structure's members.</span></span> <span data-ttu-id="1bea4-122">Chame **sizeof** para definir o tamanho correto da estrutura **de \_ atributos LPSECURITY** .</span><span class="sxs-lookup"><span data-stu-id="1bea4-122">Call **sizeof** to set the correct size of the **LPSECURITY\_ATTRIBUTES** structure.</span></span>

<span data-ttu-id="1bea4-123">Para obter mais informações, consulte [considerações de segurança: controles do Microsoft Windows](sec-comctls.md).</span><span class="sxs-lookup"><span data-stu-id="1bea4-123">For more information, see [Security Considerations: Microsoft Windows Controls](sec-comctls.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bea4-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bea4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bea4-125">Usando controles de barra de progresso</span><span class="sxs-lookup"><span data-stu-id="1bea4-125">Using Progress Bar Controls</span></span>](using-progress-bar-controls.md)
</dt> <dt>

[<span data-ttu-id="1bea4-126">Considerações de segurança: controles do Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="1bea4-126">Security Considerations: Microsoft Windows Controls</span></span>](sec-comctls.md)
</dt> </dl>

 

 