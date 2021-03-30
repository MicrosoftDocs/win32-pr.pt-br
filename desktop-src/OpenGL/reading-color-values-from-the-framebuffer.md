---
title: Lendo valores de cor do framebuffer
description: Ao usar funções que lêem valores de cor de framebuffer, esteja atento às diferenças entre ler valores RGBA e valores de índice de cor em dispositivos true-color e em dispositivos baseados em paleta.
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- OpenGL no Windows, lendo valores de cor de framebuffers
- lendo valores de cor do framebuffers OpenGL
- framebuffers, lendo valores de cor OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4df14690b68f7e93949d26ee50ac562ebd667be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635521"
---
# <a name="reading-color-values-from-the-framebuffer"></a><span data-ttu-id="c040f-106">Lendo valores de cor do framebuffer</span><span class="sxs-lookup"><span data-stu-id="c040f-106">Reading Color Values from the Framebuffer</span></span>

<span data-ttu-id="c040f-107">Ao usar funções que lêem valores de cor de framebuffer, esteja atento às diferenças entre ler valores RGBA e valores de índice de cor em dispositivos true-color e em dispositivos baseados em paleta.</span><span class="sxs-lookup"><span data-stu-id="c040f-107">When using functions that read back color values from the framebuffer, be aware of the differences between reading RGBA values and color-index values on true-color devices and on palette-based devices.</span></span>

<span data-ttu-id="c040f-108">Em um dispositivo true-color:</span><span class="sxs-lookup"><span data-stu-id="c040f-108">On a true-color device:</span></span>

-   <span data-ttu-id="c040f-109">Os valores RGBA são limitados ao canal no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c040f-109">RGBA values are limited to the channel in the device.</span></span>
-   <span data-ttu-id="c040f-110">Os valores de índice de cor são armazenados como valores RGBA no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="c040f-110">Color-index values are stored as RGBA values in the framebuffer.</span></span> <span data-ttu-id="c040f-111">Ao usar esses valores, você deve executar uma conversão inversa de RGBA para o índice lógico de paleta.</span><span class="sxs-lookup"><span data-stu-id="c040f-111">When using these values, you must perform an inverse translation from RGBA to the logical palette index.</span></span> <span data-ttu-id="c040f-112">Se dois índices lógicos tiverem os mesmos valores RGBA, o índice incorreto poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="c040f-112">If two logical indexes have the same RGBA values, the wrong index can be returned.</span></span>

<span data-ttu-id="c040f-113">Em um dispositivo baseado em paleta:</span><span class="sxs-lookup"><span data-stu-id="c040f-113">On a palette-based device:</span></span>

-   <span data-ttu-id="c040f-114">Os valores RGBA são lidos de um índice na paleta do sistema.</span><span class="sxs-lookup"><span data-stu-id="c040f-114">RGBA values are read from an index in the system palette.</span></span> <span data-ttu-id="c040f-115">O índice lógico é obtido de uma tabela inversa e os componentes RGBA são extraídos.</span><span class="sxs-lookup"><span data-stu-id="c040f-115">The logical index is obtained from an inverse table, and the RGBA components are extracted.</span></span>
-   <span data-ttu-id="c040f-116">Os valores de índice de cor são lidos de um índice para a paleta do sistema e uma tabela inversa é usada para obter o índice lógico da paleta.</span><span class="sxs-lookup"><span data-stu-id="c040f-116">Color-index values are read from an index into the system palette and an inverse table is used to get the logical palette index.</span></span>

 

 




