---
description: O Windows dá suporte a cinco modos gráficos que permitem que um aplicativo especifique como as cores são misturadas, onde a saída aparece, como a saída é dimensionada e assim por diante. Esses modos, que são armazenados em um controlador de domínio, são descritos na tabela a seguir.
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: Modos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823c7e25024eafb3b111b96b97907bc9b772006a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502419"
---
# <a name="graphic-modes"></a><span data-ttu-id="ea3aa-104">Modos gráficos</span><span class="sxs-lookup"><span data-stu-id="ea3aa-104">Graphic Modes</span></span>

<span data-ttu-id="ea3aa-105">O Windows dá suporte a cinco modos gráficos que permitem que um aplicativo especifique como as cores são misturadas, onde a saída aparece, como a saída é dimensionada e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="ea3aa-105">Windows supports five graphic modes that allow an application to specify how colors are mixed, where output appears, how the output is scaled, and so on.</span></span> <span data-ttu-id="ea3aa-106">Esses modos, que são armazenados em um controlador de domínio, são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea3aa-106">These modes, which are stored in a DC, are described in the following table.</span></span>



| <span data-ttu-id="ea3aa-107">Modo gráfico</span><span class="sxs-lookup"><span data-stu-id="ea3aa-107">Graphics mode</span></span> | <span data-ttu-id="ea3aa-108">Description</span><span class="sxs-lookup"><span data-stu-id="ea3aa-108">Description</span></span>                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3aa-109">Tela de fundo</span><span class="sxs-lookup"><span data-stu-id="ea3aa-109">Background</span></span>    | <span data-ttu-id="ea3aa-110">Define como as cores do plano de fundo são misturadas com as cores existentes da janela ou da tela para operações de bitmap e texto.</span><span class="sxs-lookup"><span data-stu-id="ea3aa-110">Defines how background colors are mixed with existing window or screen colors for bitmap and text operations.</span></span>              |
| <span data-ttu-id="ea3aa-111">Desenho</span><span class="sxs-lookup"><span data-stu-id="ea3aa-111">Drawing</span></span>       | <span data-ttu-id="ea3aa-112">Define como as cores de primeiro plano são misturadas com as cores existentes da janela ou da tela para as operações de caneta, pincel, bitmap e texto.</span><span class="sxs-lookup"><span data-stu-id="ea3aa-112">Defines how foreground colors are mixed with existing window or screen colors for pen, brush, bitmap, and text operations.</span></span> |
| <span data-ttu-id="ea3aa-113">Mapeamento</span><span class="sxs-lookup"><span data-stu-id="ea3aa-113">Mapping</span></span>       | <span data-ttu-id="ea3aa-114">Define como a saída de gráficos é mapeada do espaço lógico (ou do mundo) na janela, na tela ou no papel da impressora.</span><span class="sxs-lookup"><span data-stu-id="ea3aa-114">Defines how graphics output is mapped from logical (or world) space onto the window, screen, or printer paper.</span></span>             |
| <span data-ttu-id="ea3aa-115">Polígono – preenchimento</span><span class="sxs-lookup"><span data-stu-id="ea3aa-115">Polygon-fill</span></span>  | <span data-ttu-id="ea3aa-116">Define como o padrão de pincel é usado para preencher o interior de regiões complexas.</span><span class="sxs-lookup"><span data-stu-id="ea3aa-116">Defines how the brush pattern is used to fill the interior of complex regions.</span></span>                                             |
| <span data-ttu-id="ea3aa-117">Tira</span><span class="sxs-lookup"><span data-stu-id="ea3aa-117">Stretching</span></span>    | <span data-ttu-id="ea3aa-118">Define como as cores de bitmap são misturadas com as cores existentes da janela ou da tela quando o bitmap é compactado (ou reduzido).</span><span class="sxs-lookup"><span data-stu-id="ea3aa-118">Defines how bitmap colors are mixed with existing window or screen colors when the bitmap is compressed (or scaled down).</span></span>  |



 

<span data-ttu-id="ea3aa-119">Como acontece com objetos gráficos, o sistema inicializa um controlador de domínio com modos gráficos padrão.</span><span class="sxs-lookup"><span data-stu-id="ea3aa-119">As it does with graphic objects, the system initializes a DC with default graphic modes.</span></span> <span data-ttu-id="ea3aa-120">Um aplicativo pode recuperar e examinar esses modos padrão chamando as funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea3aa-120">An application can retrieve and examine these default modes by calling the following functions.</span></span>



| <span data-ttu-id="ea3aa-121">Modo gráfico</span><span class="sxs-lookup"><span data-stu-id="ea3aa-121">Graphics mode</span></span> | <span data-ttu-id="ea3aa-122">Função</span><span class="sxs-lookup"><span data-stu-id="ea3aa-122">Function</span></span>                                       |
|---------------|------------------------------------------------|
| <span data-ttu-id="ea3aa-123">Tela de fundo</span><span class="sxs-lookup"><span data-stu-id="ea3aa-123">Background</span></span>    | [<span data-ttu-id="ea3aa-124">**GetBkMode**</span><span class="sxs-lookup"><span data-stu-id="ea3aa-124">**GetBkMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| <span data-ttu-id="ea3aa-125">Desenho</span><span class="sxs-lookup"><span data-stu-id="ea3aa-125">Drawing</span></span>       | [<span data-ttu-id="ea3aa-126">**GetROP2**</span><span class="sxs-lookup"><span data-stu-id="ea3aa-126">**GetROP2**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| <span data-ttu-id="ea3aa-127">Mapeamento</span><span class="sxs-lookup"><span data-stu-id="ea3aa-127">Mapping</span></span>       | [<span data-ttu-id="ea3aa-128">**GetMapMode**</span><span class="sxs-lookup"><span data-stu-id="ea3aa-128">**GetMapMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| <span data-ttu-id="ea3aa-129">Polígono – preenchimento</span><span class="sxs-lookup"><span data-stu-id="ea3aa-129">Polygon-fill</span></span>  | [<span data-ttu-id="ea3aa-130">**GetPolyFillMode**</span><span class="sxs-lookup"><span data-stu-id="ea3aa-130">**GetPolyFillMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| <span data-ttu-id="ea3aa-131">Tira</span><span class="sxs-lookup"><span data-stu-id="ea3aa-131">Stretching</span></span>    | [<span data-ttu-id="ea3aa-132">**GetStretchBltMode**</span><span class="sxs-lookup"><span data-stu-id="ea3aa-132">**GetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

<span data-ttu-id="ea3aa-133">Um aplicativo pode alterar os modos padrão chamando uma das funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea3aa-133">An application can change the default modes by calling one of the following functions.</span></span>



| <span data-ttu-id="ea3aa-134">Modo gráfico</span><span class="sxs-lookup"><span data-stu-id="ea3aa-134">Graphics mode</span></span> | <span data-ttu-id="ea3aa-135">Função</span><span class="sxs-lookup"><span data-stu-id="ea3aa-135">Function</span></span>                                       |
|---------------|------------------------------------------------|
| <span data-ttu-id="ea3aa-136">Tela de fundo</span><span class="sxs-lookup"><span data-stu-id="ea3aa-136">Background</span></span>    | [<span data-ttu-id="ea3aa-137">**SetBkMode**</span><span class="sxs-lookup"><span data-stu-id="ea3aa-137">**SetBkMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| <span data-ttu-id="ea3aa-138">Desenho</span><span class="sxs-lookup"><span data-stu-id="ea3aa-138">Drawing</span></span>       | [<span data-ttu-id="ea3aa-139">**SetROP2**</span><span class="sxs-lookup"><span data-stu-id="ea3aa-139">**SetROP2**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| <span data-ttu-id="ea3aa-140">Mapeamento</span><span class="sxs-lookup"><span data-stu-id="ea3aa-140">Mapping</span></span>       | [<span data-ttu-id="ea3aa-141">**SetMapMode**</span><span class="sxs-lookup"><span data-stu-id="ea3aa-141">**SetMapMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| <span data-ttu-id="ea3aa-142">Polígono – preenchimento</span><span class="sxs-lookup"><span data-stu-id="ea3aa-142">Polygon-fill</span></span>  | [<span data-ttu-id="ea3aa-143">**SetPolyFillMode**</span><span class="sxs-lookup"><span data-stu-id="ea3aa-143">**SetPolyFillMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| <span data-ttu-id="ea3aa-144">Tira</span><span class="sxs-lookup"><span data-stu-id="ea3aa-144">Stretching</span></span>    | [<span data-ttu-id="ea3aa-145">**SetStretchBltMode**</span><span class="sxs-lookup"><span data-stu-id="ea3aa-145">**SetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 



