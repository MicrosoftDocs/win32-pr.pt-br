---
description: 'Etapa 1: criar o Windows Framework'
ms.assetid: 678c6261-cbd0-4865-a1dd-03de55eca996
title: 'Etapa 1: criar o Windows Framework'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ff1712f631db520ff30065e8943d13b280f3d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768625"
---
# <a name="step-1-create-the-windows-framework"></a><span data-ttu-id="76749-103">Etapa 1: criar o Windows Framework</span><span class="sxs-lookup"><span data-stu-id="76749-103">Step 1: Create the Windows Framework</span></span>

<span data-ttu-id="76749-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="76749-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="76749-105">Comece criando a estrutura básica de um aplicativo do Windows, incluindo WinMain e um procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="76749-105">Start by creating the basic framework of a Windows application, including WinMain and a window procedure.</span></span> <span data-ttu-id="76749-106">A função WinMain não é mostrada aqui; Chame o [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) antes do loop de mensagem para inicializar a biblioteca com e [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) depois que o loop de mensagem for encerrado.</span><span class="sxs-lookup"><span data-stu-id="76749-106">The WinMain function is not shown here; call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) before the message loop to initialize the COM library, and [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) after the message loop exits.</span></span> <span data-ttu-id="76749-107">Comece com o seguinte procedimento mínimo de janela:</span><span class="sxs-lookup"><span data-stu-id="76749-107">Start with the following minimal window procedure:</span></span>


```C++
LRESULT CALLBACK MainWndProc(HWND hwnd, UINT msg, WPARAM wparam, LPARAM lparam)
{
    static BITMAPINFOHEADER *pbmi = NULL;
    static BYTE *pBuffer = NULL;
    switch (msg)
    {
    case WM_CLOSE:
        DestroyWindow(hwnd);
        break;
    case WM_DESTROY:
        if (pbmi) delete [] pbmi;
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hwnd, msg, wparam, lparam);
    }
    return 0;
}
```



<span data-ttu-id="76749-108">Quando você recupera um quadro de pôster do detector de mídia, ele retorna um buffer que contém uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguida pelos bits de imagem.</span><span class="sxs-lookup"><span data-stu-id="76749-108">When you retrieve a poster frame from the Media Detector, it returns a buffer that contains a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure followed by the image bits.</span></span> <span data-ttu-id="76749-109">Portanto, defina duas variáveis estáticas no procedimento de janela: *pbmi* manterá um ponteiro para a estrutura **BITMAPINFOHEADER** e *pBuffer* manterá um ponteiro para o bitmap.</span><span class="sxs-lookup"><span data-stu-id="76749-109">Therefore, define two static variables in the window procedure: *pbmi* will hold a pointer to the **BITMAPINFOHEADER** structure, and *pBuffer* will hold a pointer to the bitmap.</span></span> <span data-ttu-id="76749-110">O aplicativo irá alocar o buffer no *pbmi* usando `new` , portanto, ele deve excluir o buffer antes que a janela seja destruída.</span><span class="sxs-lookup"><span data-stu-id="76749-110">The application will allocate the buffer in *pbmi* using `new`, so it must delete the buffer before the window is destroyed.</span></span> <span data-ttu-id="76749-111">O ponteiro *pBuffer* é calculado como um deslocamento de *pbmi*, portanto, não é necessário excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="76749-111">The *pBuffer* pointer is calculated as an offset from *pbmi*, so there is no need to delete it.</span></span>

<span data-ttu-id="76749-112">Próximo: [etapa 2: adicionar um comando de menu para pegar um quadro de cartaz](step-2--add-a-menu-command-to-grab-a-poster-frame.md)</span><span class="sxs-lookup"><span data-stu-id="76749-112">Next: [Step 2: Add a Menu Command to Grab a Poster Frame](step-2--add-a-menu-command-to-grab-a-poster-frame.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="76749-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="76749-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76749-114">Capturando um quadro de cartaz</span><span class="sxs-lookup"><span data-stu-id="76749-114">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
