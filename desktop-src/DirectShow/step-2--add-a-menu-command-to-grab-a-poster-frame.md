---
description: 'Etapa 2: adicionar um comando de menu para pegar um quadro de cartaz'
ms.assetid: 9a0f807b-5543-41d4-ad2a-030a4346131c
title: 'Etapa 2: adicionar um comando de menu para pegar um quadro de cartaz'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d049dc4e79197cfbe0a86b065eaf67a5ea567a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091741"
---
# <a name="step-2-add-a-menu-command-to-grab-a-poster-frame"></a><span data-ttu-id="97b49-103">Etapa 2: adicionar um comando de menu para pegar um quadro de cartaz</span><span class="sxs-lookup"><span data-stu-id="97b49-103">Step 2: Add a Menu Command to Grab a Poster Frame</span></span>

<span data-ttu-id="97b49-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="97b49-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="97b49-105">Este tópico é a etapa 2 da [captura de um quadro de cartaz](grabbing-a-poster-frame.md).</span><span class="sxs-lookup"><span data-stu-id="97b49-105">This topic is Step 2 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="97b49-106">Em seguida, adicione um comando para que o usuário pegue um quadro de pôster de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="97b49-106">Next, add a command for the user to grab a poster frame from a file.</span></span> <span data-ttu-id="97b49-107">Crie um item de menu com uma ID de recurso do bitmap de IDM \_ e adicione a seguinte instrução case ao procedimento de janela:</span><span class="sxs-lookup"><span data-stu-id="97b49-107">Create a menu item with a resource ID of IDM\_BITMAP, and add the following case statement to the window procedure:</span></span>


```C++
case WM_COMMAND:
    switch (LOWORD(wparam))
    {
    case IDM_BITMAP:
        {
            HRESULT hr = DoShowBitmap(hwnd, &pbmi);
            if (SUCCEEDED(hr))
            {
                pBuffer = reinterpret_cast<BYTE*>(pbmi) + 
                    sizeof(BITMAPINFOHEADER);
                InvalidateRect(hwnd, NULL, TRUE);
            }
            else
            {
                MessageBox(hwnd, TEXT("Cannot display the image."),
                    TEXT("Error"), MB_OK | MB_ICONERROR);
            }
        }
        break;  // IDM_BITMAP
    }
    break;  // WM_COMMAND
```



<span data-ttu-id="97b49-108">A função DoShowBitmap retornará o buffer alocado em *pbmi*.</span><span class="sxs-lookup"><span data-stu-id="97b49-108">The DoShowBitmap function will return the allocated buffer in *pbmi*.</span></span> <span data-ttu-id="97b49-109">Supondo que a função tenha sucesso, o endereço do bitmap (</span><span class="sxs-lookup"><span data-stu-id="97b49-109">Assuming the function succeeds, the address of the bitmap (</span></span>


```C++
pBuffer
```



<span data-ttu-id="97b49-110">) pode ser calculado como um deslocamento de *pbmi*.</span><span class="sxs-lookup"><span data-stu-id="97b49-110">) can be calculated as an offset from *pbmi*.</span></span> <span data-ttu-id="97b49-111">Na função DoShowBitmap, exiba uma caixa de diálogo **Abrir arquivo** para que o usuário escolha um arquivo e, em seguida, chame a função getbitmap definida pelo aplicativo, que irá recuperar o bitmap:</span><span class="sxs-lookup"><span data-stu-id="97b49-111">In the DoShowBitmap function, display an **Open File** dialog box for the user to choose a file, and then call the application-defined GetBitmap function, which will retrieve the bitmap:</span></span>


```C++
HRESULT DoShowBitmap(HWND hwnd, BITMAPINFOHEADER** ppbmih)
{
    OPENFILENAME ofn;       // common dialog box structure
    // Initialize OPENFILENAME (not shown).
    // Display the Open File dialog box.  
    if (GetOpenFileName(&ofn) != TRUE) // failed to open file
    {
        return E_FAIL;
    }
    return GetBitmap(ofn.lpstrFile, ppbmih);
}
```



<span data-ttu-id="97b49-112">Em seguida: [etapa 3: implementar a função Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)</span><span class="sxs-lookup"><span data-stu-id="97b49-112">Next: [Step 3: Implement the Frame-Grabbing Function](step-3--implement-the-frame-grabbing-function.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="97b49-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97b49-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97b49-114">Capturando um quadro de cartaz</span><span class="sxs-lookup"><span data-stu-id="97b49-114">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 



