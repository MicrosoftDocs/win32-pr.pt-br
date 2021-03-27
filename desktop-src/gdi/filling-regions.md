---
description: Um aplicativo preenche o interior de uma região chamando a função FillRgn e fornecendo um identificador que identifica um pincel específico.
ms.assetid: 6174b2ea-836a-4538-a0ad-e123c88fc6f6
title: Preenchendo regiões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62709869f5f25a6cde11812844efdab6162b1e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010728"
---
# <a name="filling-regions"></a><span data-ttu-id="bcdd9-103">Preenchendo regiões</span><span class="sxs-lookup"><span data-stu-id="bcdd9-103">Filling Regions</span></span>

<span data-ttu-id="bcdd9-104">Um aplicativo preenche o interior de uma região chamando a função [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) e fornecendo um identificador que identifica um pincel específico.</span><span class="sxs-lookup"><span data-stu-id="bcdd9-104">An application fills the interior of a region by calling the [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) function and supplying a handle that identifies a specific brush.</span></span> <span data-ttu-id="bcdd9-105">Quando um aplicativo chama FillRgn, o sistema preenche a região com o pincel usando o modo de preenchimento atual para o contexto do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="bcdd9-105">When an application calls FillRgn , the system fills the region with the brush by using the current fill mode for the specified device context.</span></span> <span data-ttu-id="bcdd9-106">Há dois modos de preenchimento: alternativo e enrolamento.</span><span class="sxs-lookup"><span data-stu-id="bcdd9-106">There are two fill modes: alternate and winding.</span></span> <span data-ttu-id="bcdd9-107">O aplicativo pode definir o modo de preenchimento para um contexto de dispositivo chamando a função [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="bcdd9-107">The application can set the fill mode for a device context by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="bcdd9-108">O aplicativo pode recuperar o modo de preenchimento atual para um contexto de dispositivo chamando a função [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="bcdd9-108">The application can retrieve the current fill mode for a device context by calling the [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) function.</span></span>

<span data-ttu-id="bcdd9-109">A ilustração a seguir mostra duas regiões idênticas: uma preenchida usando o modo alternativo e outra preenchida usando o modo de enrolamento.</span><span class="sxs-lookup"><span data-stu-id="bcdd9-109">The following illustration shows two identical regions: one filled using alternate mode and the other filled using winding mode.</span></span>

![ilustração mostrando estrelas 2 5-pontas: uma preenchida apenas nos pontos, a outra preenchida completamente](images/csrgn-03.png)

## <a name="alternate-mode"></a><span data-ttu-id="bcdd9-111">Modo alternativo</span><span class="sxs-lookup"><span data-stu-id="bcdd9-111">Alternate Mode</span></span>

<span data-ttu-id="bcdd9-112">Para determinar quais pixels o sistema realça quando o modo alternativo é especificado, execute o seguinte teste:</span><span class="sxs-lookup"><span data-stu-id="bcdd9-112">To determine which pixels the system highlights when alternate mode is specified, perform the following test:</span></span>

1.  <span data-ttu-id="bcdd9-113">Selecione um pixel dentro do interior da região.</span><span class="sxs-lookup"><span data-stu-id="bcdd9-113">Select a pixel within the region's interior.</span></span>
2.  <span data-ttu-id="bcdd9-114">Desenhe um raio de imaginário, na direção x positiva, desse pixel em direção ao infinito.</span><span class="sxs-lookup"><span data-stu-id="bcdd9-114">Draw an imaginary ray, in the positive x-direction, from that pixel toward infinity.</span></span>
3.  <span data-ttu-id="bcdd9-115">Cada vez que Ray intercepta uma linha de limite, incrementa um valor de contagem.</span><span class="sxs-lookup"><span data-stu-id="bcdd9-115">Each time the ray intersects a boundary line, increment a count value.</span></span>

<span data-ttu-id="bcdd9-116">O sistema realça o pixel se o valor da contagem for um número ímpar.</span><span class="sxs-lookup"><span data-stu-id="bcdd9-116">The system highlights the pixel if the count value is an odd number.</span></span>

## <a name="winding-mode"></a><span data-ttu-id="bcdd9-117">Modo de enrolamento</span><span class="sxs-lookup"><span data-stu-id="bcdd9-117">Winding Mode</span></span>

<span data-ttu-id="bcdd9-118">Para determinar quais pixels o sistema realça quando o modo de enrolamento é especificado, execute o seguinte teste:</span><span class="sxs-lookup"><span data-stu-id="bcdd9-118">To determine which pixels the system highlights when winding mode is specified, perform the following test:</span></span>

1.  <span data-ttu-id="bcdd9-119">Determine a direção na qual cada linha de limite é desenhada.</span><span class="sxs-lookup"><span data-stu-id="bcdd9-119">Determine the direction in which each boundary line is drawn.</span></span>
2.  <span data-ttu-id="bcdd9-120">Selecione um pixel dentro do interior da região.</span><span class="sxs-lookup"><span data-stu-id="bcdd9-120">Select a pixel within the region's interior.</span></span>
3.  <span data-ttu-id="bcdd9-121">Desenhe um raio de imaginário, na direção x positiva, do pixel em direção ao infinito.</span><span class="sxs-lookup"><span data-stu-id="bcdd9-121">Draw an imaginary ray, in the positive x-direction, from the pixel toward infinity.</span></span>
4.  <span data-ttu-id="bcdd9-122">Cada vez que Ray intercepta uma linha de limite com um componente y positivo, incrementa um valor de contagem.</span><span class="sxs-lookup"><span data-stu-id="bcdd9-122">Each time the ray intersects a boundary line with a positive y-component, increment a count value.</span></span> <span data-ttu-id="bcdd9-123">Cada vez que Ray intercepta uma linha de limite com um componente y negativo, Decrementa o valor da contagem.</span><span class="sxs-lookup"><span data-stu-id="bcdd9-123">Each time the ray intersects a boundary line with a negative y-component, decrement the count value.</span></span>

<span data-ttu-id="bcdd9-124">O sistema realça o pixel se o valor da contagem for diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="bcdd9-124">The system highlights the pixel if the count value is nonzero.</span></span>

 

 



