---
title: Formatos de pixel
description: Formatos de pixel
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- OpenGL no Windows, pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16f9f78edc0cf935fb602de8d88792091588ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755972"
---
# <a name="pixel-formats"></a><span data-ttu-id="7d868-104">Formatos de pixel</span><span class="sxs-lookup"><span data-stu-id="7d868-104">Pixel Formats</span></span>

<span data-ttu-id="7d868-105">Um *formato de pixel* especifica várias propriedades de uma superfície de desenho OpenGL.</span><span class="sxs-lookup"><span data-stu-id="7d868-105">A *pixel format* specifies several properties of an OpenGL drawing surface.</span></span> <span data-ttu-id="7d868-106">Algumas das propriedades especificadas por um formato de pixel são:</span><span class="sxs-lookup"><span data-stu-id="7d868-106">Some of the properties specified by a pixel format are:</span></span>

-   <span data-ttu-id="7d868-107">Se o buffer de pixel é de buffer único ou duplo.</span><span class="sxs-lookup"><span data-stu-id="7d868-107">Whether the pixel buffer is single- or double-buffered.</span></span>
-   <span data-ttu-id="7d868-108">Se os dados de pixel estão em um formato RGBA ou de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="7d868-108">Whether the pixel data is in RGBA or color-index form.</span></span>
-   <span data-ttu-id="7d868-109">O número de bits usados para armazenar dados de cores.</span><span class="sxs-lookup"><span data-stu-id="7d868-109">The number of bits used to store color data.</span></span>
-   <span data-ttu-id="7d868-110">O número de bits usados para o buffer de profundidade (eixo z).</span><span class="sxs-lookup"><span data-stu-id="7d868-110">The number of bits used for the depth (z-axis) buffer.</span></span>
-   <span data-ttu-id="7d868-111">O número de bits usados para o buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="7d868-111">The number of bits used for the stencil buffer.</span></span>
-   <span data-ttu-id="7d868-112">O número de planos de sobreposição e Underlay.</span><span class="sxs-lookup"><span data-stu-id="7d868-112">The number of overlay and underlay planes.</span></span>
-   <span data-ttu-id="7d868-113">Várias máscaras de visibilidade.</span><span class="sxs-lookup"><span data-stu-id="7d868-113">Various visibility masks.</span></span>

<span data-ttu-id="7d868-114">A implementação da Microsoft do OpenGL para Windows usa a estrutura de dados [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) para transmitir dados de formato de pixel.</span><span class="sxs-lookup"><span data-stu-id="7d868-114">Microsoft's implementation of OpenGL for Windows uses the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure to convey pixel format data.</span></span> <span data-ttu-id="7d868-115">Os membros da estrutura especificam as propriedades anteriores e várias outras.</span><span class="sxs-lookup"><span data-stu-id="7d868-115">The structure's members specify the preceding properties and several others.</span></span>

<span data-ttu-id="7d868-116">Um determinado contexto de dispositivo pode dar suporte A vários formatos de pixel.</span><span class="sxs-lookup"><span data-stu-id="7d868-116">A given device context can support several pixel formats.</span></span> <span data-ttu-id="7d868-117">O Windows identifica os formatos de pixel para os quais um contexto de dispositivo dá suporte com valores de índice baseados em um consecutivos (1, 2, 3, 4 e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="7d868-117">Windows identifies the pixel formats that a device context supports with consecutive one-based index values (1, 2, 3, 4, and so on).</span></span> <span data-ttu-id="7d868-118">Um contexto de dispositivo pode ter apenas um formato de pixel atual, escolhido do conjunto de formatos de pixel com suporte.</span><span class="sxs-lookup"><span data-stu-id="7d868-118">A device context can have just one current pixel format, chosen from the set of pixel formats it supports.</span></span>

<span data-ttu-id="7d868-119">Cada janela tem seu próprio formato de pixel atual no OpenGL no Windows.</span><span class="sxs-lookup"><span data-stu-id="7d868-119">Each window has its own current pixel format in OpenGL in Windows.</span></span> <span data-ttu-id="7d868-120">Isso significa, por exemplo, que um aplicativo pode exibir simultaneamente o RGBA e o índice de cores OpenGL do Windows, ou janelas OpenGL de buffer único e duplo.</span><span class="sxs-lookup"><span data-stu-id="7d868-120">This means, for example, that an application can simultaneously display RGBA and color-index OpenGL windows, or single- and double-buffered OpenGL windows.</span></span> <span data-ttu-id="7d868-121">Esse recurso de formato de pixel por janela é limitado a janelas OpenGL.</span><span class="sxs-lookup"><span data-stu-id="7d868-121">This per-window pixel format capability is limited to OpenGL windows.</span></span>

<span data-ttu-id="7d868-122">Normalmente, você obtém um contexto de dispositivo, define o formato de pixel do contexto do dispositivo e, em seguida, cria um contexto de renderização OpenGL adequado para esse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7d868-122">Typically, you obtain a device context, set the device context's pixel format, and then create an OpenGL rendering context suitable for that device.</span></span>

> [!Note]  
> <span data-ttu-id="7d868-123">Você define o formato de pixel antes de criar um contexto de renderização porque o contexto de renderização herda o formato de pixel do contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7d868-123">You set the pixel format before creating a rendering context because the rendering context inherits the device context's pixel format.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7d868-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d868-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d868-125">Funções de formato de pixel</span><span class="sxs-lookup"><span data-stu-id="7d868-125">Pixel Format Functions</span></span>](pixel-format-functions.md)
</dt> </dl>

 

 




