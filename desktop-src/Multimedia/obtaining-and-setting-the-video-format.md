---
title: Obtendo e definindo o formato de vídeo
description: Obtendo e definindo o formato de vídeo
ms.assetid: 0e6baf24-7a79-45ab-9fc7-69334419956d
keywords:
- macro capGetVideoFormat
- macro capGetVideoFormatSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6890c3a1d653d43d24c5baa0790cc0d26040685b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823750"
---
# <a name="obtaining-and-setting-the-video-format"></a><span data-ttu-id="92691-105">Obtendo e definindo o formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="92691-105">Obtaining and Setting the Video Format</span></span>

<span data-ttu-id="92691-106">A estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) é de comprimento variável para acomodar formatos de dados padrão e compactados.</span><span class="sxs-lookup"><span data-stu-id="92691-106">The [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure is of variable length to accommodate standard and compressed data formats.</span></span> <span data-ttu-id="92691-107">Como essa estrutura é de comprimento variável, os aplicativos sempre devem consultar o tamanho da estrutura e alocar memória antes de recuperar o formato de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="92691-107">Because this structure is of variable length, applications must always query the size of the structure and allocate memory before retrieving the current video format.</span></span> <span data-ttu-id="92691-108">O exemplo a seguir usa a macro [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) para recuperar o tamanho do buffer e, em seguida, chama a macro [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) para recuperar o formato de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="92691-108">The following example uses the [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) macro to retrieve the buffer size and then calls the [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) macro to retrieve the current video format.</span></span>


```C++
LPBITMAPINFO lpbi;
DWORD dwSize;

dwSize = capGetVideoFormatSize(hWndC);
lpbi = GlobalAllocPtr (GHND, dwSize);
capGetVideoFormat(hWndC, lpbi, dwSize); 

// Access the video format and then free the allocated memory.
 
```



<span data-ttu-id="92691-109">Os aplicativos podem usar a macro [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) (ou a mensagem do [**VIDEOFORMAT do WM \_ Cap \_ set \_**](wm-cap-set-videoformat.md) ) para enviar uma estrutura de cabeçalho [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) para a janela de captura.</span><span class="sxs-lookup"><span data-stu-id="92691-109">Applications can use the [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) macro (or the [**WM\_CAP\_SET\_VIDEOFORMAT**](wm-cap-set-videoformat.md) message) to send a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) header structure to the capture window.</span></span> <span data-ttu-id="92691-110">Como os formatos de vídeo são específicos do dispositivo, seu aplicativo deve verificar o valor de retorno para determinar se o formato foi aceito.</span><span class="sxs-lookup"><span data-stu-id="92691-110">Because video formats are device specific, your application should check the return value to determine if the format was accepted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92691-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92691-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92691-112">Usando a captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="92691-112">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 