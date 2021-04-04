---
title: Como usar fluxos
description: Você pode usar fluxos para transferir dados para dentro ou para fora de um controle de edição rico. Um fluxo é definido por uma estrutura EDITSTREAM, que especifica um buffer e uma função de retorno de chamada definida pelo aplicativo.
ms.assetid: A7ED47F1-968C-4E41-B1E2-4449072D2FC4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89a9cc2a8caa157f9c65220fc5cead7564bc555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104084415"
---
# <a name="how-to-use-streams"></a><span data-ttu-id="bf0db-104">Como usar fluxos</span><span class="sxs-lookup"><span data-stu-id="bf0db-104">How to Use Streams</span></span>

<span data-ttu-id="bf0db-105">Você pode usar fluxos para transferir dados para dentro ou para fora de um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="bf0db-105">You can use streams to transfer data into or out of a rich edit control.</span></span> <span data-ttu-id="bf0db-106">Um fluxo é definido por uma estrutura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) , que especifica um buffer e uma função de retorno de chamada definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bf0db-106">A stream is defined by an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure, which specifies a buffer and an application-defined callback function.</span></span>

<span data-ttu-id="bf0db-107">Para ler dados em um controle de edição rico (ou seja, transmitir nos dados), use a mensagem de [**\_ fluxo**](em-streamin.md) em em.</span><span class="sxs-lookup"><span data-stu-id="bf0db-107">To read data into a rich edit control (that is, stream in the data), use the [**EM\_STREAMIN**](em-streamin.md) message.</span></span> <span data-ttu-id="bf0db-108">O controle chama repetidamente a função de retorno de chamada do aplicativo, que transfere uma parte dos dados para o buffer a cada vez.</span><span class="sxs-lookup"><span data-stu-id="bf0db-108">The control repeatedly calls the application's callback function, which transfers a portion of the data into the buffer each time.</span></span>

<span data-ttu-id="bf0db-109">Para salvar o conteúdo de um controle de edição rico (ou seja, transmitir os dados), você pode usar a mensagem em [**\_ fluxo**](em-streamout.md) em em diante.</span><span class="sxs-lookup"><span data-stu-id="bf0db-109">To save the contents of a rich edit control (that is, stream out the data), you can use the [**EM\_STREAMOUT**](em-streamout.md) message.</span></span> <span data-ttu-id="bf0db-110">O controle grava repetidamente no buffer e, em seguida, chama a função de retorno de chamada do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bf0db-110">The control repeatedly writes to the buffer and then calls the application's callback function.</span></span> <span data-ttu-id="bf0db-111">Para cada chamada, a função de chamada de retorno salva o conteúdo do buffer.</span><span class="sxs-lookup"><span data-stu-id="bf0db-111">For each call, the callback function saves the contents of the buffer.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bf0db-112">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="bf0db-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bf0db-113">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="bf0db-113">Technologies</span></span>

-   [<span data-ttu-id="bf0db-114">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="bf0db-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bf0db-115">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="bf0db-115">Prerequisites</span></span>

-   <span data-ttu-id="bf0db-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="bf0db-116">C/C++</span></span>
-   <span data-ttu-id="bf0db-117">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="bf0db-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bf0db-118">Instruções</span><span class="sxs-lookup"><span data-stu-id="bf0db-118">Instructions</span></span>

### <a name="use-a-stream"></a><span data-ttu-id="bf0db-119">Usar um fluxo</span><span class="sxs-lookup"><span data-stu-id="bf0db-119">Use a Stream</span></span>

<span data-ttu-id="bf0db-120">O exemplo de código a seguir mostra como ler um arquivo. rtf em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="bf0db-120">The following code example shows how to read an .rtf file into a rich edit control.</span></span> <span data-ttu-id="bf0db-121">O identificador de arquivo é passado para a função de retorno de chamada por meio do membro **dwCookie** da estrutura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="bf0db-121">The file handle is passed to the callback function through the **dwCookie** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span>


```C++
DWORD CALLBACK EditStreamCallback(DWORD_PTR dwCookie, 
                                  LPBYTE lpBuff,
                                  LONG cb, 
                                  PLONG pcb)
{
    HANDLE hFile = (HANDLE)dwCookie;
    
    if (ReadFile(hFile, lpBuff, cb, (DWORD *)pcb, NULL)) 
    {
        return 0;
    }
    
    return -1;
}

BOOL FillRichEditFromFile(HWND hwnd, LPCTSTR pszFile)
{
    BOOL fSuccess = FALSE;
    
    HANDLE hFile = CreateFile(pszFile, GENERIC_READ, 
                              FILE_SHARE_READ, 0, OPEN_EXISTING,
                              FILE_FLAG_SEQUENTIAL_SCAN, NULL);
        
    if (hFile != INVALID_HANDLE_VALUE) 
    {
        EDITSTREAM es = { 0 };
        
        es.pfnCallback = EditStreamCallback;
        es.dwCookie    = (DWORD_PTR)hFile;
        
        if (SendMessage(hwnd, EM_STREAMIN, SF_RTF, (LPARAM)&es) && es.dwError == 0) 
        {
                fSuccess = TRUE;
        }
        
        CloseHandle(hFile);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="bf0db-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf0db-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf0db-123">Usando controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="bf0db-123">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="bf0db-124">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="bf0db-124">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




