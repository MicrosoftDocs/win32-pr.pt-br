---
title: Limitações
description: Limitações
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- OpenGL no Windows, limitações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478a139326f74c236ca0109fddbbc3d4ffb46e1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635643"
---
# <a name="limitations"></a><span data-ttu-id="a3ec1-104">Limitações</span><span class="sxs-lookup"><span data-stu-id="a3ec1-104">Limitations</span></span>

<span data-ttu-id="a3ec1-105">A implementação genérica tem as seguintes limitações:</span><span class="sxs-lookup"><span data-stu-id="a3ec1-105">The generic implementation has the following limitations:</span></span>

-   <span data-ttu-id="a3ec1-106">Imprimindo.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-106">Printing.</span></span>

    <span data-ttu-id="a3ec1-107">Você pode imprimir uma imagem OpenGL diretamente em uma impressora usando apenas os metaarquivos.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-107">You can print an OpenGL image directly to a printer using metafiles only.</span></span> <span data-ttu-id="a3ec1-108">Para obter mais informações, consulte [imprimindo uma imagem OpenGL](printing-an-opengl-image.md).</span><span class="sxs-lookup"><span data-stu-id="a3ec1-108">For more information, see [Printing an OpenGL Image](printing-an-opengl-image.md).</span></span>

-   <span data-ttu-id="a3ec1-109">Os elementos gráficos OpenGL e GDI não podem ser misturados em uma janela com buffer duplo.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-109">OpenGL and GDI graphics cannot be mixed in a double-buffered window.</span></span>

    <span data-ttu-id="a3ec1-110">Um aplicativo pode desenhar diretamente elementos gráficos OpenGL e GDI em uma janela de buffer único, mas não em uma janela com buffer duplo.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-110">An application can directly draw both OpenGL graphics and GDI graphics into a single-buffered window, but not into a double-buffered window.</span></span>

-   <span data-ttu-id="a3ec1-111">Não há paletas de cores de hardware por janela.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-111">There are no per-window hardware color palettes.</span></span>

    <span data-ttu-id="a3ec1-112">O Windows tem uma paleta de cores de hardware de sistema único, que se aplica à tela inteira.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-112">Windows has a single system hardware color palette, which applies to the whole screen.</span></span> <span data-ttu-id="a3ec1-113">Uma janela OpenGL não pode ter sua própria paleta de hardware, mas pode ter sua própria paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-113">An OpenGL window cannot have its own hardware palette, but can have its own logical palette.</span></span> <span data-ttu-id="a3ec1-114">Para fazer isso, ele deve se tornar um aplicativo com reconhecimento de paleta.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-114">To do so, it must become a palette-aware application.</span></span> <span data-ttu-id="a3ec1-115">Para obter mais informações, consulte [OpenGL Color Modes e Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).</span><span class="sxs-lookup"><span data-stu-id="a3ec1-115">For more information, see [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).</span></span>

-   <span data-ttu-id="a3ec1-116">Não há suporte direto para a área de transferência, DDE (Dynamic Data Exchange) ou OLE.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-116">There is no direct support for the Clipboard, dynamic data exchange (DDE), or OLE.</span></span>

    <span data-ttu-id="a3ec1-117">Uma janela com gráficos OpenGL não dá suporte diretamente a esses recursos do Windows.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-117">A window with OpenGL graphics does not directly support these Windows capabilities.</span></span> <span data-ttu-id="a3ec1-118">No entanto, há soluções alternativas para o uso da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-118">There are workarounds, however, for using the Clipboard.</span></span> <span data-ttu-id="a3ec1-119">Para obter mais informações, consulte [copiando uma imagem OpenGL para a área de transferência](copying-an-opengl-image-to-the-clipboard.md).</span><span class="sxs-lookup"><span data-stu-id="a3ec1-119">For more information, see [Copying an OpenGL Image to the Clipboard](copying-an-opengl-image-to-the-clipboard.md).</span></span>

-   <span data-ttu-id="a3ec1-120">A biblioteca de classes C++ do inventário 2,0 não está incluída.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-120">The Inventor 2.0 C++ class library is not included.</span></span>

    <span data-ttu-id="a3ec1-121">A biblioteca de classes de inventário, criada com base no OpenGL, fornece construções de nível superior para programação de gráficos 3-D.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-121">The Inventor class library, built on top of OpenGL, provides higher-level constructs for programming 3-D graphics.</span></span> <span data-ttu-id="a3ec1-122">Ele não está incluído na versão atual da implementação do OpenGL para Windows da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-122">It is not included in the current version of Microsoft's implementation of OpenGL for Windows.</span></span>

-   <span data-ttu-id="a3ec1-123">Não há suporte para os seguintes recursos de formato de pixel: imagens estereoscópico, Alpha bitplanes e buffers auxiliares.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-123">There is no support for the following pixel format features: stereoscopic images, alpha bitplanes, and auxiliary buffers.</span></span>

    <span data-ttu-id="a3ec1-124">Há, no entanto, suporte para vários buffers auxiliares, incluindo: buffer de estêncil, buffer de acumulação, buffer de fundo (buffer duplo), sobreposição e buffer de plano underlay e buffer de profundidade (eixo z).</span><span class="sxs-lookup"><span data-stu-id="a3ec1-124">There is, however, support for several ancillary buffers including: stencil buffer, accumulation buffer, back buffer (double buffering), overlay and underlay plane buffer, and depth (z-axis) buffer.</span></span>

 

 




