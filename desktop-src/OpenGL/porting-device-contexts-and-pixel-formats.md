---
title: Portando contextos de dispositivo e formatos de pixel
description: Portando contextos de dispositivo e formatos de pixel
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- portando para OpenGL, pixels
- Portabilidade do OpenGL, pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d793c139c6d7a0a0fc85b2e2c36f30176ce9ab6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105753150"
---
# <a name="porting-device-contexts-and-pixel-formats"></a><span data-ttu-id="47e60-105">Portando contextos de dispositivo e formatos de pixel</span><span class="sxs-lookup"><span data-stu-id="47e60-105">Porting Device Contexts and Pixel Formats</span></span>

<span data-ttu-id="47e60-106">Cada janela na implementação da Microsoft do OpenGL para Windows tem seu próprio formato de pixel atual.</span><span class="sxs-lookup"><span data-stu-id="47e60-106">Each window in the Microsoft implementation of OpenGL for Windows has its own current pixel format.</span></span> <span data-ttu-id="47e60-107">Um formato de pixel é definido por uma estrutura de dados [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="47e60-107">A pixel format is defined by a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure.</span></span> <span data-ttu-id="47e60-108">Como cada janela tem seu próprio formato de pixel, você obtém um contexto de dispositivo, define o formato de pixel do contexto do dispositivo e, em seguida, cria um contexto de renderização OpenGL para o contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47e60-108">Because each window has its own pixel format, you obtain a device context, set the pixel format of the device context, and then create an OpenGL rendering context for the device context.</span></span> <span data-ttu-id="47e60-109">O contexto de renderização usa automaticamente o formato de pixel de seu contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47e60-109">The rendering context automatically uses the pixel format of its device context.</span></span>

<span data-ttu-id="47e60-110">O sistema de janelas X também usa uma estrutura de dados, **XVisualInfo**, para especificar as propriedades de pixels em uma janela.</span><span class="sxs-lookup"><span data-stu-id="47e60-110">The X Window System also uses a data structure, **XVisualInfo**, to specify the properties of pixels in a window.</span></span> <span data-ttu-id="47e60-111">Estruturas **XVisualInfo** contêm uma estrutura de dados **visuais** que descreve como os recursos de cores são usados em uma tela específica.</span><span class="sxs-lookup"><span data-stu-id="47e60-111">**XVisualInfo** structures contain a **Visual** data structure that describes how color resources are used in a specific screen.</span></span>

<span data-ttu-id="47e60-112">No sistema X Window, **XVisualInfo** é usado para criar uma janela definindo a janela como o formato de pixel desejado.</span><span class="sxs-lookup"><span data-stu-id="47e60-112">In the X Window System, **XVisualInfo** is used to create a window by setting the window to the pixel format you want.</span></span> <span data-ttu-id="47e60-113">A estrutura retornada é usada para criar a janela e um contexto de renderização.</span><span class="sxs-lookup"><span data-stu-id="47e60-113">The returned structure is used to create the window and a rendering context.</span></span> <span data-ttu-id="47e60-114">No Windows, você primeiro cria uma janela e Obtém um identificador para um contexto de dispositivo (HDC) da janela.</span><span class="sxs-lookup"><span data-stu-id="47e60-114">In Windows, you first create a window and get a handle to a device context (HDC) of the window.</span></span> <span data-ttu-id="47e60-115">Em seguida, o HDC é usado para definir o formato de pixel para a janela.</span><span class="sxs-lookup"><span data-stu-id="47e60-115">The HDC is then used to set the pixel format for the window.</span></span> <span data-ttu-id="47e60-116">O contexto de renderização usa o formato de pixel da janela.</span><span class="sxs-lookup"><span data-stu-id="47e60-116">The rendering context uses the pixel format of the window.</span></span>

<span data-ttu-id="47e60-117">A tabela a seguir compara o sistema de janelas X e as funções visuais GLX com suas funções de formato de pixel equivalentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="47e60-117">The following table compares the X Window System and GLX visual functions with their equivalent Windows pixel format functions.</span></span>



| <span data-ttu-id="47e60-118">Função X Window/GLX Visual</span><span class="sxs-lookup"><span data-stu-id="47e60-118">X window/GLX visual function</span></span>                                                                                     | <span data-ttu-id="47e60-119">Função de formato de pixel do Windows</span><span class="sxs-lookup"><span data-stu-id="47e60-119">Windows pixel format function</span></span>                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47e60-120">XVisualInfo \* **glXChooseVisual**(exibição *\* dpy*, *tela* int, *\* atributo* intlist)</span><span class="sxs-lookup"><span data-stu-id="47e60-120">XVisualInfo\***glXChooseVisual**( Display *\*dpy*,int *screen*,int *\*attribList*)</span></span>                               | <span data-ttu-id="47e60-121">int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)(HDC *HDC*, PIXELFORMATDESCRIPTOR *\* PPFD*)</span><span class="sxs-lookup"><span data-stu-id="47e60-121">int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)( HDC *hdc*,PIXELFORMATDESCRIPTOR *\*ppfd*)</span></span>                                      |
| <span data-ttu-id="47e60-122">int **glXGetConfig**(exibição *\* dpy*, XVisualInfo *\* vis*, int *\* atriblist*, *\* valor* int)</span><span class="sxs-lookup"><span data-stu-id="47e60-122">int **glXGetConfig**( Display *\*dpy*,XVisualInfo *\*vis*,int *\*attribList*,int *\*value*)</span></span>                      | <span data-ttu-id="47e60-123">int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)(HDC *HDC*, int *iPixelFormat*, uint *nbytes*, LPPIXELFORMATDESCRIPTOR *PPFD*)</span><span class="sxs-lookup"><span data-stu-id="47e60-123">int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)( HDC *hdc*,int *iPixelFormat*,UINT *nBytes*,LPPIXELFORMATDESCRIPTOR *ppfd*)</span></span> |
| <span data-ttu-id="47e60-124">XVisualInfo \* **XGetVisualInfo**( *\* dpy* de exibição, *\_ máscara de vinfo* longa, XVisualInfo *\* vinfo \_ Templ*, int *\* nItems*)</span><span class="sxs-lookup"><span data-stu-id="47e60-124">XVisualInfo\***XGetVisualInfo**( Display *\*dpy*,long *vinfo\_mask*,XVisualInfo *\*vinfo\_templ*,int *\*nitems*)</span></span> | <span data-ttu-id="47e60-125">int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)(HDC *HDC*)</span><span class="sxs-lookup"><span data-stu-id="47e60-125">int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)( HDC *hdc*)</span></span>                                                                           |
| <span data-ttu-id="47e60-126">O *Visual* retornado por **glxChooseVisual** é usado quando uma janela é criada.</span><span class="sxs-lookup"><span data-stu-id="47e60-126">The *visual* returned by **glxChooseVisual** is used when a window is created.</span></span>                                   | <span data-ttu-id="47e60-127">BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)(HDC *HDC*, int *iPixelFormat*, PIXELFORMATDESCRIPTOR *\* PPFD*)</span><span class="sxs-lookup"><span data-stu-id="47e60-127">BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)( HDC *hdc*,int *iPixelFormat*,PIXELFORMATDESCRIPTOR *\*ppfd*)</span></span>                        |



 

<span data-ttu-id="47e60-128">As seções a seguir fornecem exemplos de fragmentos de código de formato de pixel para um programa de sistema X Window e o mesmo código após ele ter sido transportado para o Windows.</span><span class="sxs-lookup"><span data-stu-id="47e60-128">The following sections give examples of pixel format code fragments for an X Window System program, and the same code after it has been ported to Windows.</span></span>

-   [<span data-ttu-id="47e60-129">Exemplo de código de formato de pixel GLX</span><span class="sxs-lookup"><span data-stu-id="47e60-129">GLX Pixel Format Code Sample</span></span>](glx-pixel-format-code-sample.md)
-   [<span data-ttu-id="47e60-130">Exemplo de código de formato de pixel do Windows</span><span class="sxs-lookup"><span data-stu-id="47e60-130">Windows Pixel Format Code Sample</span></span>](win32-pixel-format-code-sample.md)

<span data-ttu-id="47e60-131">Para obter mais informações sobre formatos de pixel, consulte [formatos de pixel](pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="47e60-131">For more information on pixel formats, see [Pixel Formats](pixel-formats.md).</span></span>

 

 




