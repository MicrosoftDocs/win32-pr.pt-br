---
description: As dimensões de uma caneta superficial são especificadas em unidades do dispositivo.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Canetas superficiais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb312ed0b3825397ff79ebc32d363956ad04519
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661623"
---
# <a name="cosmetic-pens"></a><span data-ttu-id="f0308-103">Canetas superficiais</span><span class="sxs-lookup"><span data-stu-id="f0308-103">Cosmetic Pens</span></span>

<span data-ttu-id="f0308-104">As dimensões de uma caneta superficial são especificadas em unidades do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f0308-104">The dimensions of a cosmetic pen are specified in device units.</span></span> <span data-ttu-id="f0308-105">Portanto, as linhas desenhadas com uma caneta superficial sempre têm uma largura fixa.</span><span class="sxs-lookup"><span data-stu-id="f0308-105">Therefore, lines drawn with a cosmetic pen always have a fixed width.</span></span> <span data-ttu-id="f0308-106">As linhas desenhadas com uma caneta superficial geralmente são desenhadas de 3 a 10 vezes mais rápido do que as linhas desenhadas com uma caneta geométrica.</span><span class="sxs-lookup"><span data-stu-id="f0308-106">Lines drawn with a cosmetic pen are generally drawn 3 to 10 times faster than lines drawn with a geometric pen.</span></span> <span data-ttu-id="f0308-107">As canetas superficiais têm três atributos: largura, estilo e cor.</span><span class="sxs-lookup"><span data-stu-id="f0308-107">Cosmetic pens have three attributes: width, style, and color.</span></span> <span data-ttu-id="f0308-108">Para obter mais informações sobre esses atributos, consulte [atributos de caneta](pen-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="f0308-108">For more information about these attributes, see [Pen Attributes](pen-attributes.md).</span></span>

<span data-ttu-id="f0308-109">Para criar uma caneta superficial, use a função [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)ou [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) .</span><span class="sxs-lookup"><span data-stu-id="f0308-109">To create a cosmetic pen, use the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="f0308-110">Para recuperar uma das três canetas de superficial de estoque gerenciadas pelo sistema, use a função [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) .</span><span class="sxs-lookup"><span data-stu-id="f0308-110">To retrieve one of the three stock cosmetic pens managed by the system, use the [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function.</span></span>

<span data-ttu-id="f0308-111">Depois de criar uma caneta (ou obter um identificador para uma das canetas de ações), selecione a caneta no contexto do dispositivo do aplicativo (DC) usando a função [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="f0308-111">After you create a pen (or obtain a handle to one of the stock pens), select the pen into the application's device context (DC) using the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span> <span data-ttu-id="f0308-112">A partir desse ponto, o aplicativo usa essa caneta para qualquer operação de desenho de linha em sua área de cliente.</span><span class="sxs-lookup"><span data-stu-id="f0308-112">From this point on, the application uses this pen for any line-drawing operations in its client area.</span></span>

 

 



