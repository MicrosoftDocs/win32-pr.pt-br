---
description: A caneta, o pincel, o bitmap, a paleta, a região e o caminho associados a um controlador de domínio são chamados de objetos gráficos. Os atributos a seguir estão associados a cada um desses objetos.
ms.assetid: 95c82efa-257e-4718-9853-7ef10cdfd76c
title: Objetos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b80aadcb0988e7bd64910d04ecfbf6ec608845d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988809"
---
# <a name="graphic-objects"></a><span data-ttu-id="471ec-104">Objetos gráficos</span><span class="sxs-lookup"><span data-stu-id="471ec-104">Graphic Objects</span></span>

<span data-ttu-id="471ec-105">A caneta, o pincel, o bitmap, a paleta, a região e o caminho associados a um controlador de domínio são chamados de objetos gráficos.</span><span class="sxs-lookup"><span data-stu-id="471ec-105">The pen, brush, bitmap, palette, region, and path associated with a DC are referred to as its graphic objects.</span></span> <span data-ttu-id="471ec-106">Os atributos a seguir estão associados a cada um desses objetos.</span><span class="sxs-lookup"><span data-stu-id="471ec-106">The following attributes are associated with each of these objects.</span></span>



| <span data-ttu-id="471ec-107">Objeto gráfico</span><span class="sxs-lookup"><span data-stu-id="471ec-107">Graphic object</span></span> | <span data-ttu-id="471ec-108">Atributos associados</span><span class="sxs-lookup"><span data-stu-id="471ec-108">Associated attributes</span></span>                                                               |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="471ec-109">Bitmap</span><span class="sxs-lookup"><span data-stu-id="471ec-109">Bitmap</span></span>         | <span data-ttu-id="471ec-110">Tamanho, em bytes; dimensões, em pixels; formato de cor; esquema de compactação; e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="471ec-110">Size, in bytes; dimensions, in pixels; color-format; compression scheme; and so on.</span></span> |
| <span data-ttu-id="471ec-111">Pincel</span><span class="sxs-lookup"><span data-stu-id="471ec-111">Brush</span></span>          | <span data-ttu-id="471ec-112">Estilo, cor, padrão e origem.</span><span class="sxs-lookup"><span data-stu-id="471ec-112">Style, color, pattern, and origin.</span></span>                                                  |
| <span data-ttu-id="471ec-113">Paleta</span><span class="sxs-lookup"><span data-stu-id="471ec-113">Palette</span></span>        | <span data-ttu-id="471ec-114">Cores e tamanho (ou número de cores).</span><span class="sxs-lookup"><span data-stu-id="471ec-114">Colors and size (or number of colors).</span></span>                                              |
| <span data-ttu-id="471ec-115">Fonte</span><span class="sxs-lookup"><span data-stu-id="471ec-115">Font</span></span>           | <span data-ttu-id="471ec-116">Nome da face de tipos, largura, altura, peso, conjunto de caracteres e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="471ec-116">Typeface name, width, height, weight, character set, and so on.</span></span>                     |
| <span data-ttu-id="471ec-117">Caminho</span><span class="sxs-lookup"><span data-stu-id="471ec-117">Path</span></span>           | <span data-ttu-id="471ec-118">La.</span><span class="sxs-lookup"><span data-stu-id="471ec-118">Shape.</span></span>                                                                              |
| <span data-ttu-id="471ec-119">Caneta</span><span class="sxs-lookup"><span data-stu-id="471ec-119">Pen</span></span>            | <span data-ttu-id="471ec-120">Estilo, largura e cor.</span><span class="sxs-lookup"><span data-stu-id="471ec-120">Style, width, and color.</span></span>                                                            |
| <span data-ttu-id="471ec-121">Região</span><span class="sxs-lookup"><span data-stu-id="471ec-121">Region</span></span>         | <span data-ttu-id="471ec-122">Local e dimensões.</span><span class="sxs-lookup"><span data-stu-id="471ec-122">Location and dimensions.</span></span>                                                            |



 

<span data-ttu-id="471ec-123">Quando um aplicativo cria um controlador de domínio, o sistema armazena automaticamente um conjunto de objetos padrão nele (não há bitmap ou caminho padrão).</span><span class="sxs-lookup"><span data-stu-id="471ec-123">When an application creates a DC, the system automatically stores a set of default objects in it (there is no default bitmap or path).</span></span> <span data-ttu-id="471ec-124">Um aplicativo pode examinar os atributos dos objetos padrão chamando as funções [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) e [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) .</span><span class="sxs-lookup"><span data-stu-id="471ec-124">An application can examine the attributes of the default objects by calling the [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) and [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) functions.</span></span> <span data-ttu-id="471ec-125">O aplicativo pode alterar esses padrões criando um novo objeto e selecionando-o no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="471ec-125">The application can change these defaults by creating a new object and selecting it into the DC.</span></span> <span data-ttu-id="471ec-126">Um objeto é selecionado em um controlador de domínio chamando a função [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="471ec-126">An object is selected into a DC by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span>

<span data-ttu-id="471ec-127">Um aplicativo pode definir a cor do pincel atual com um valor de cor especificado com [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).</span><span class="sxs-lookup"><span data-stu-id="471ec-127">An application can set the current brush color to a specified color value with [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).</span></span>

<span data-ttu-id="471ec-128">A função [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) retorna a cor do pincel do DC.</span><span class="sxs-lookup"><span data-stu-id="471ec-128">The [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) function returns the DC brush color.</span></span> <span data-ttu-id="471ec-129">A função [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) define a cor da caneta para um valor de cor especificado.</span><span class="sxs-lookup"><span data-stu-id="471ec-129">The [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) function sets the pen color to a specified color value.</span></span> <span data-ttu-id="471ec-130">A função [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) retorna a cor da caneta do DC.</span><span class="sxs-lookup"><span data-stu-id="471ec-130">The [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) function returns the DC pen color.</span></span>

 

 



