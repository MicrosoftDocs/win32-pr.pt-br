---
title: Paletas e o Gerenciador de paleta
description: O Gerenciador de paleta do Windows, que faz parte da GDI, destina-se especificamente a adaptadores de vídeo de 8 bits com uma paleta de hardware de 256 entradas de cor.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL no Windows, Gerenciador de paleta
- OpenGL no Windows, paletas de hardware
- Gerenciador de paleta OpenGL
- paletas de hardware OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dac7d122ec36201e0156a141efc3291a87c7150
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105750787"
---
# <a name="palettes-and-the-palette-manager"></a><span data-ttu-id="0a263-107">Paletas e o Gerenciador de paleta</span><span class="sxs-lookup"><span data-stu-id="0a263-107">Palettes and the Palette Manager</span></span>

<span data-ttu-id="0a263-108">O Gerenciador de paleta do Windows, que faz parte da GDI, destina-se especificamente a adaptadores de vídeo de 8 bits com uma *paleta de hardware* de 256 entradas de cor.</span><span class="sxs-lookup"><span data-stu-id="0a263-108">The Windows Palette Manager, which is part of the GDI, specifically targets 8-bit display adapters with a *hardware palette* of 256 color entries.</span></span> <span data-ttu-id="0a263-109">Os pixels na tela são armazenados como um índice de 8 bits na paleta de hardware.</span><span class="sxs-lookup"><span data-stu-id="0a263-109">Pixels on the screen are stored as an 8-bit index into the hardware palette.</span></span> <span data-ttu-id="0a263-110">Cada entrada na paleta de hardware geralmente define uma cor de 24 bits (8 cada vermelho, verde e azul).</span><span class="sxs-lookup"><span data-stu-id="0a263-110">Each entry in the hardware palette usually defines a 24-bit color (8 each of red, green, and blue).</span></span>

<span data-ttu-id="0a263-111">O Gerenciador de paleta mantém uma *paleta do sistema* que é uma cópia da paleta de hardware.</span><span class="sxs-lookup"><span data-stu-id="0a263-111">The Palette Manager maintains a *system palette* that is a copy of the hardware palette.</span></span> <span data-ttu-id="0a263-112">A paleta do sistema é dividida em duas seções: 20 cores reservadas e as 236 cores restantes, que você pode definir usando o Gerenciador de paleta.</span><span class="sxs-lookup"><span data-stu-id="0a263-112">The system palette is divided into two sections: 20 reserved colors and the remaining 236 colors, which you can set using the Palette Manager.</span></span>

<span data-ttu-id="0a263-113">Uma *paleta lógica* padrão de 20 cores é selecionada e realizada em um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a263-113">A default 20-color *logical palette* is selected and realized into a device context.</span></span> <span data-ttu-id="0a263-114">Você pode criar e usar uma nova paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="0a263-114">You can create and use a new logical palette.</span></span> <span data-ttu-id="0a263-115">Para alterar a paleta do sistema, selecione e perceba a paleta lógica que você criou.</span><span class="sxs-lookup"><span data-stu-id="0a263-115">To change the system palette, select and realize the logical palette you created.</span></span>

<span data-ttu-id="0a263-116">Você provavelmente criará uma paleta lógica para especificar as cores que deseja exibir em seu aplicativo OpenGL.</span><span class="sxs-lookup"><span data-stu-id="0a263-116">You'll probably create a logical palette to specify the colors you want displayed in your OpenGL application.</span></span> <span data-ttu-id="0a263-117">Usando determinadas chamadas GDI, você pode substituir temporariamente a maior parte da paleta do sistema por uma paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="0a263-117">Using certain GDI calls, you can temporarily replace most of the system palette with a logical palette.</span></span> <span data-ttu-id="0a263-118">Usando uma paleta lógica, você pode definir cores de pixel para a GDI usando o modo RGBA ou de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="0a263-118">Using a logical palette, you can define pixel colors for the GDI using either the RGBA or the color-index mode.</span></span> <span data-ttu-id="0a263-119">O tamanho máximo de uma paleta lógica é de 256 cores para dispositivos de 8 bits e 4.096 cores em um dispositivo de cor real (16, 24 e 32 bits).</span><span class="sxs-lookup"><span data-stu-id="0a263-119">The maximum size of a logical palette is 256 colors for 8-bit devices and 4,096 colors on a true-color device (16, 24, and 32 bits).</span></span>

<span data-ttu-id="0a263-120">Para obter mais informações sobre os modos RGBA e de índice de cor, consulte [modo RGBA e gerenciamento de paleta do Windows](rgba-mode-and-windows-palette-management.md) e [modos de cores OpenGL e gerenciamento de paleta do Windows](opengl-color-modes-and-windows-palette-management.md).</span><span class="sxs-lookup"><span data-stu-id="0a263-120">For more information on the RGBA and color-index modes, see [RGBA Mode and Windows Palette Management](rgba-mode-and-windows-palette-management.md) and [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).</span></span>

 

 




