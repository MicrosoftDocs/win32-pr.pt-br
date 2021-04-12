---
title: Buffers frontal, traseiro e outros
description: O OpenGL armazena e manipula dados de pixel em um framebuffer.
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- OpenGL no Windows, buffers
- framebuffers OpenGL
- buffers de cores OpenGL
- buffers de profundidade OpenGL
- buffers de acumulação OpenGL
- buffers de estêncil OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea487b73af356853bee2054db292cdfe740bd16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364133"
---
# <a name="front-back-and-other-buffers"></a><span data-ttu-id="9ffbc-109">Buffers frontal, traseiro e outros</span><span class="sxs-lookup"><span data-stu-id="9ffbc-109">Front, Back, and Other Buffers</span></span>

<span data-ttu-id="9ffbc-110">O OpenGL armazena e manipula dados de pixel em um framebuffer.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-110">OpenGL stores and manipulates pixel data in a framebuffer.</span></span> <span data-ttu-id="9ffbc-111">O framebuffer consiste em um conjunto de buffers lógicos: cor, profundidade, acumulação e buffers de estêncil.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-111">The framebuffer consists of a set of logical buffers: color, depth, accumulation, and stencil buffers.</span></span> <span data-ttu-id="9ffbc-112">O buffer de cores em si consiste em um conjunto de buffers lógicos; Esse conjunto pode incluir um front-Left, um front-Right, um back-Left, um back-Right e um número de buffers auxiliares.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-112">The color buffer itself consists of a set of logical buffers; this set can include a front-left, a front-right, a back-left, a back-right, and some number of auxiliary buffers.</span></span> <span data-ttu-id="9ffbc-113">Um formato de pixel específico ou implementação OpenGL pode não fornecer todos esses buffers.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-113">A particular pixel format or OpenGL implementation may not supply all of these buffers.</span></span> <span data-ttu-id="9ffbc-114">Por exemplo, a versão atual da implementação da Microsoft do OpenGL no Windows não oferece suporte a imagens estereoscópico; portanto, um formato de pixel não pode ter buffers de cores esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-114">For example, the current version of Microsoft's implementation of OpenGL in Windows does not support stereoscopic images, so a pixel format cannot have left and right color buffers.</span></span> <span data-ttu-id="9ffbc-115">Além disso, a versão atual não oferece suporte a buffers auxiliares.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-115">In addition, the current version does not support auxiliary buffers.</span></span> <span data-ttu-id="9ffbc-116">Para obter mais informações sobre buffers OpenGL e as funções OpenGL que operam neles, consulte o *manual de referência OpenGL* e o *Guia de programação OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-116">For more information on OpenGL buffers and the OpenGL functions that operate on them, see the *OpenGL Reference Manual* and the *OpenGL Programming Guide*.</span></span>

<span data-ttu-id="9ffbc-117">A implementação da Microsoft do OpenGL no Windows dá suporte ao buffer duplo de imagens.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-117">Microsoft's implementation of OpenGL in Windows supports double buffering of images.</span></span> <span data-ttu-id="9ffbc-118">Essa é uma técnica na qual um aplicativo desenha pixels para um buffer fora da tela e, em seguida, quando essa imagem está pronta para exibição, o copia o conteúdo do buffer fora da tela para um buffer na tela.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-118">This is a technique in which an application draws pixels to an off-screen buffer, and then, when that image is ready for display, copies the contents of the off-screen buffer to an on-screen buffer.</span></span> <span data-ttu-id="9ffbc-119">O buffer duplo permite alterações de imagem suaves, que são especialmente importantes para imagens animadas.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-119">Double buffering enables smooth image changes, which are especially important for animated images.</span></span>

<span data-ttu-id="9ffbc-120">Dois buffers de cores estão disponíveis para aplicativos que usam buffer duplo: um buffer frontal e um buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-120">Two color buffers are available to applications that use double buffering: a front buffer and a back buffer.</span></span> <span data-ttu-id="9ffbc-121">Por padrão, os comandos de desenho são direcionados para o buffer de fundo (o buffer fora da tela), enquanto o buffer frontal é exibido na tela.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-121">By default, drawing commands are directed to the back buffer (the off-screen buffer), while the front buffer is displayed on the screen.</span></span> <span data-ttu-id="9ffbc-122">Quando o buffer fora da tela estiver pronto para exibição, você chamará [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)e o Windows copiará o conteúdo do buffer fora da tela para o buffer na tela.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-122">When the off-screen buffer is ready for display, you call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers), and Windows copies the contents of the off-screen buffer to the on-screen buffer.</span></span>

<span data-ttu-id="9ffbc-123">A implementação genérica usa um DIB (bitmap independente de dispositivo) como o buffer de fundo e a tela são exibidos como o buffer frontal.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-123">The generic implementation uses a device-independent bitmap (DIB) as the back buffer and the screen display as the front buffer.</span></span> <span data-ttu-id="9ffbc-124">Os dispositivos de hardware e seus drivers podem usar abordagens diferentes.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-124">Hardware devices and their drivers may use different approaches.</span></span>

<span data-ttu-id="9ffbc-125">O buffer duplo é uma propriedade de formato de pixel.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-125">Double buffering is a pixel-format property.</span></span> <span data-ttu-id="9ffbc-126">Para solicitar um buffer duplo para um formato de pixel, defina o \_ sinalizador PFD DOUBLEBUFFER na estrutura de dados [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) em uma chamada para [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span><span class="sxs-lookup"><span data-stu-id="9ffbc-126">To request double buffering for a pixel format, set the PFD\_DOUBLEBUFFER flag in the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure in a call to [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span>

<span data-ttu-id="9ffbc-127">A função principal OpenGL, [**glDrawBuffer**](gldrawbuffer.md), seleciona buffers para gravação e limpeza.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-127">The OpenGL core function, [**glDrawBuffer**](gldrawbuffer.md), selects buffers for writing and clearing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ffbc-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ffbc-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ffbc-129">Funções de buffer</span><span class="sxs-lookup"><span data-stu-id="9ffbc-129">Buffer Functions</span></span>](buffer-functions.md)
</dt> </dl>

 

 




