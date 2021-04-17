---
title: Imprimindo uma imagem OpenGL
description: Você pode imprimir imagens OpenGL renderizadas em metaarquivos avançados.
ms.assetid: 6099cbe2-82f9-46ec-a3ca-74486c111639
keywords:
- OpenGL no Windows, imprimindo
- Imprimindo imagens OpenGL OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca0c5260a084796915a7564f793f0e252b5228c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105749230"
---
# <a name="printing-an-opengl-image"></a><span data-ttu-id="e1037-105">Imprimindo uma imagem OpenGL</span><span class="sxs-lookup"><span data-stu-id="e1037-105">Printing an OpenGL Image</span></span>

<span data-ttu-id="e1037-106">Você pode imprimir imagens OpenGL renderizadas em metaarquivos avançados.</span><span class="sxs-lookup"><span data-stu-id="e1037-106">You can print OpenGL images rendered in enhanced metafiles.</span></span> <span data-ttu-id="e1037-107">Quando você renderiza para um dispositivo de impressora (HDC), ele deve ser apoiado por um spooler de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="e1037-107">When you render to a printer device (HDC) it must be backed by a metafile spooler.</span></span> <span data-ttu-id="e1037-108">O OpenGL usa memória para profundidade, cor e outros buffers para armazenar a saída de gráficos em uma impressora.</span><span class="sxs-lookup"><span data-stu-id="e1037-108">OpenGL uses memory for depth, color, and other buffers to store graphics output to a printer.</span></span> <span data-ttu-id="e1037-109">Como a resolução de impressora típica requer uma quantidade significativa de memória para armazenar a saída de gráficos, a impressão de uma imagem OpenGL pode exigir mais memória do que está disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="e1037-109">Because typical printer resolution requires a significant amount of memory to store the graphics output, printing an OpenGL image might require more memory than is available in the system.</span></span> <span data-ttu-id="e1037-110">Para superar essa limitação, a implementação atual do OpenGL imprime gráficos OpenGL em bandas.</span><span class="sxs-lookup"><span data-stu-id="e1037-110">To overcome this limitation, the current implementation of OpenGL prints OpenGL graphics in bands.</span></span> <span data-ttu-id="e1037-111">No entanto, isso aumenta o tempo necessário para imprimir imagens OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e1037-111">However, this increases the time it takes to print OpenGL images.</span></span>

<span data-ttu-id="e1037-112">Antes de imprimir uma imagem OpenGL, você deve chamar a função [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) para concluir a inicialização de um DC (contexto de dispositivo de impressora).</span><span class="sxs-lookup"><span data-stu-id="e1037-112">Before you print an OpenGL image, you must call the [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) function to complete the initialization of a printer device context (DC).</span></span> <span data-ttu-id="e1037-113">Depois de chamar **StartDoc**, você pode criar contextos de RENDERIZAÇÃO (HGLRC) para renderizar para o dispositivo de impressora.</span><span class="sxs-lookup"><span data-stu-id="e1037-113">After calling **StartDoc**, you can create rendering contexts (HGLRC) to render to the printer device.</span></span> <span data-ttu-id="e1037-114">Se você criar contextos de renderização antes de chamar **StartDoc**, não será possível determinar se um metarquivo está no spool.</span><span class="sxs-lookup"><span data-stu-id="e1037-114">If you create rendering contexts before calling **StartDoc**, there is no way to determine whether a metafile is spooled.</span></span>

<span data-ttu-id="e1037-115">O exemplo de código a seguir mostra como imprimir uma imagem OpenGL:</span><span class="sxs-lookup"><span data-stu-id="e1037-115">The following code sample shows how to print an OpenGL image:</span></span>

``` syntax
HDC            hDC;
DOCINFO        di;
HGLRC          hglrc;

// Call StartDoc to start the document 
StartDoc( hDC, &di );

// Prepare the printer driver to accept data 
StartPage(hDC);

// Create a rendering context using the metafile DC 
hglrc = wglCreateContext ( hDCmetafile );

// Do OpenGL rendering operations here 
    . . .
wglMakeCurrent(NULL, NULL); // Get rid of rendering context 
    . . .
EndPage(hDC); // Finish writing to the page 
EndDoc(hDC); // End the print job
```

<span data-ttu-id="e1037-116">Para obter mais informações sobre como usar [metarquivos, consulte Enhanced Metafile Operations](/windows/desktop/gdi/enhanced-metafile-operations).</span><span class="sxs-lookup"><span data-stu-id="e1037-116">For more information on using metafiles, see [Enhanced Metafile Operations](/windows/desktop/gdi/enhanced-metafile-operations).</span></span>

 

 