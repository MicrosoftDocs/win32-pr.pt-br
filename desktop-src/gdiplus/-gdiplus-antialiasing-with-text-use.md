---
description: O Windows GDI+ fornece vários níveis de qualidade para o texto de desenho. Normalmente, a renderização de qualidade superior leva mais tempo de processamento do que a renderização de qualidade inferior.
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: Anti-aliasing com texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c7b7c59a436db6c16251aa8e866648eed5cc51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988928"
---
# <a name="antialiasing-with-text"></a><span data-ttu-id="5ffe8-104">Anti-aliasing com texto</span><span class="sxs-lookup"><span data-stu-id="5ffe8-104">Antialiasing with Text</span></span>

<span data-ttu-id="5ffe8-105">O Windows GDI+ fornece vários níveis de qualidade para o texto de desenho.</span><span class="sxs-lookup"><span data-stu-id="5ffe8-105">Windows GDI+ provides various quality levels for drawing text.</span></span> <span data-ttu-id="5ffe8-106">Normalmente, a renderização de qualidade superior leva mais tempo de processamento do que a renderização de qualidade inferior.</span><span class="sxs-lookup"><span data-stu-id="5ffe8-106">Typically, higher quality rendering takes more processing time than lower quality rendering.</span></span>

<span data-ttu-id="5ffe8-107">O nível de qualidade é uma propriedade da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="5ffe8-107">The quality level is a property of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="5ffe8-108">Para definir o nível de qualidade, chame o método [**Graphics:: SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) de um objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="5ffe8-108">To set the quality level, call the [**Graphics::SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) method of a **Graphics** object.</span></span> <span data-ttu-id="5ffe8-109">O método **Graphics:: SetTextRenderingHint** recebe um dos elementos da enumeração [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) , que é declarado em Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="5ffe8-109">The **Graphics::SetTextRenderingHint** method receives one of the elements of the [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) enumeration, which is declared in Gdiplusenums.h.</span></span>

<span data-ttu-id="5ffe8-110">A GDI+ fornece anti-aliasing tradicional e um novo tipo de anti-aliasing baseado na tecnologia de vídeo Microsoft ClearType disponível somente no Windows XP e no Windows Server 2003 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="5ffe8-110">GDI+ provides traditional antialiasing and a new kind of antialiasing based on Microsoft ClearType display technology only available on Windows XP and Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="5ffe8-111">A suavização de ClearType melhora a legibilidade em monitores de LCD colorido que têm uma interface digital, como os monitores em laptops e monitores de área de trabalho plana de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="5ffe8-111">ClearType smoothing improves readability on color LCD monitors that have a digital interface, such as the monitors in laptops and high-quality flat desktop displays.</span></span> <span data-ttu-id="5ffe8-112">A legibilidade em telas CRT também é um pouco melhor.</span><span class="sxs-lookup"><span data-stu-id="5ffe8-112">Readability on CRT screens is also somewhat improved.</span></span>

<span data-ttu-id="5ffe8-113">O ClearType depende da orientação e da ordenação das faixas do LCD.</span><span class="sxs-lookup"><span data-stu-id="5ffe8-113">ClearType is dependent on the orientation and ordering of the LCD stripes.</span></span> <span data-ttu-id="5ffe8-114">Atualmente, o ClearType é implementado somente para faixas verticais que são ordenadas como RGB.</span><span class="sxs-lookup"><span data-stu-id="5ffe8-114">Currently, ClearType is implemented only for vertical stripes that are ordered RGB.</span></span> <span data-ttu-id="5ffe8-115">Isso pode ser uma preocupação se você estiver usando um Tablet PC, onde a exibição pode ser orientada em qualquer direção ou se você estiver usando uma tela que pode ser transformada de paisagem para retrato.</span><span class="sxs-lookup"><span data-stu-id="5ffe8-115">This might be a concern if you are using a tablet PC, where the display can be oriented in any direction, or if you are using a screen that can be turned from landscape to portrait.</span></span>

<span data-ttu-id="5ffe8-116">O exemplo a seguir Desenha texto com duas configurações de qualidade diferentes:</span><span class="sxs-lookup"><span data-stu-id="5ffe8-116">The following example draws text with two different quality settings:</span></span>


```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 32, FontStyleRegular, UnitPixel);
SolidBrush  solidBrush(Color(255, 0, 0, 255));
WCHAR       string1[] = L"SingleBitPerPixel";
WCHAR       string2[] = L"AntiAlias";

graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);
graphics.DrawString(string1, -1, &font, PointF(10.0f, 10.0f), &solidBrush);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
graphics.DrawString(string2, -1, &font, PointF(10.0f, 60.0f), &solidBrush);
            
```



<span data-ttu-id="5ffe8-117">A ilustração a seguir mostra a saída do código anterior.</span><span class="sxs-lookup"><span data-stu-id="5ffe8-117">The following illustration shows the output of the preceding code.</span></span>

![captura de tela de uma cadeia cujos caracteres têm bordas denteadas em contraste com uma com bordas suaves](images/fontstext10.png)

 

 



