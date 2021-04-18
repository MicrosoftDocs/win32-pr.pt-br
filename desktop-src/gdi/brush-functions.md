---
description: As funções a seguir são usadas com pincéis.
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: Funções de pincel (GDI do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2170ff5c4b743e19da669bd76b340ca95ac2ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502436"
---
# <a name="brush-functions-windows-gdi"></a><span data-ttu-id="fbde6-103">Funções de pincel (GDI do Windows)</span><span class="sxs-lookup"><span data-stu-id="fbde6-103">Brush Functions (Windows GDI)</span></span>

<span data-ttu-id="fbde6-104">As funções a seguir são usadas com pincéis.</span><span class="sxs-lookup"><span data-stu-id="fbde6-104">The following functions are used with brushes.</span></span>



| <span data-ttu-id="fbde6-105">Função</span><span class="sxs-lookup"><span data-stu-id="fbde6-105">Function</span></span>                                                   | <span data-ttu-id="fbde6-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="fbde6-106">Description</span></span>                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="fbde6-107">**CreateBrushIndirect**</span><span class="sxs-lookup"><span data-stu-id="fbde6-107">**CreateBrushIndirect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)         | <span data-ttu-id="fbde6-108">Cria um pincel com um estilo, cor e padrão especificados</span><span class="sxs-lookup"><span data-stu-id="fbde6-108">Creates a brush with a specified style, color, and pattern</span></span> |
| [<span data-ttu-id="fbde6-109">**CreateDIBPatternBrushPt**</span><span class="sxs-lookup"><span data-stu-id="fbde6-109">**CreateDIBPatternBrushPt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) | <span data-ttu-id="fbde6-110">Cria um pincel com o padrão de um DIB</span><span class="sxs-lookup"><span data-stu-id="fbde6-110">Creates a brush with the pattern from a DIB</span></span>                |
| [<span data-ttu-id="fbde6-111">**CreateHatchBrush**</span><span class="sxs-lookup"><span data-stu-id="fbde6-111">**CreateHatchBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)               | <span data-ttu-id="fbde6-112">Cria um pincel com um padrão de hachura e cor</span><span class="sxs-lookup"><span data-stu-id="fbde6-112">Creates a brush with a hatch pattern and color</span></span>             |
| [<span data-ttu-id="fbde6-113">**CreatePatternBrush**</span><span class="sxs-lookup"><span data-stu-id="fbde6-113">**CreatePatternBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)           | <span data-ttu-id="fbde6-114">Cria um pincel com um padrão de bitmap</span><span class="sxs-lookup"><span data-stu-id="fbde6-114">Creates a brush with a bitmap pattern</span></span>                      |
| [<span data-ttu-id="fbde6-115">**CreateSolidBrush**</span><span class="sxs-lookup"><span data-stu-id="fbde6-115">**CreateSolidBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)               | <span data-ttu-id="fbde6-116">Cria um pincel com uma cor sólida</span><span class="sxs-lookup"><span data-stu-id="fbde6-116">Creates a brush with a solid color</span></span>                         |
| [<span data-ttu-id="fbde6-117">**GetBrushOrgEx**</span><span class="sxs-lookup"><span data-stu-id="fbde6-117">**GetBrushOrgEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)                     | <span data-ttu-id="fbde6-118">Obtém a origem do pincel para um contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="fbde6-118">Gets the brush origin for a device context</span></span>                 |
| [<span data-ttu-id="fbde6-119">**GetSysColorBrush**</span><span class="sxs-lookup"><span data-stu-id="fbde6-119">**GetSysColorBrush**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush)               | <span data-ttu-id="fbde6-120">Obtém um identificador para um pincel que corresponde a um índice de cor</span><span class="sxs-lookup"><span data-stu-id="fbde6-120">Gets a handle to a brush that corresponds to a color index</span></span> |
| [<span data-ttu-id="fbde6-121">**PatBlt**</span><span class="sxs-lookup"><span data-stu-id="fbde6-121">**PatBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-patblt)                                   | <span data-ttu-id="fbde6-122">Pinta um retângulo</span><span class="sxs-lookup"><span data-stu-id="fbde6-122">Paints a rectangle</span></span>                                         |
| [<span data-ttu-id="fbde6-123">**SetBrushOrgEx**</span><span class="sxs-lookup"><span data-stu-id="fbde6-123">**SetBrushOrgEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex)                     | <span data-ttu-id="fbde6-124">Define a origem do pincel para um contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="fbde6-124">Sets the brush origin for a device context</span></span>                 |
| [<span data-ttu-id="fbde6-125">**SetDCBrushColor**</span><span class="sxs-lookup"><span data-stu-id="fbde6-125">**SetDCBrushColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | <span data-ttu-id="fbde6-126">Define a cor do pincel do contexto do dispositivo atual.</span><span class="sxs-lookup"><span data-stu-id="fbde6-126">Sets the current device context brush color.</span></span>               |



 

## <a name="obsolete-functions"></a><span data-ttu-id="fbde6-127">Funções obsoletas</span><span class="sxs-lookup"><span data-stu-id="fbde6-127">Obsolete Functions</span></span>

<span data-ttu-id="fbde6-128">As funções a seguir são fornecidas apenas para compatibilidade com versões de 16 bits do Windows.</span><span class="sxs-lookup"><span data-stu-id="fbde6-128">The following functions are provided only for compatibility with 16-bit versions of Windows.</span></span>

[<span data-ttu-id="fbde6-129">**CreateDIBPatternBrush**</span><span class="sxs-lookup"><span data-stu-id="fbde6-129">**CreateDIBPatternBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)

 

 



