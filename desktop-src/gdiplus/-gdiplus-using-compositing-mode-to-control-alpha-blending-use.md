---
description: 'Pode haver ocasiões em que você deseja criar um bitmap fora da tela com as seguintes características:'
ms.assetid: 2a7590ce-daf4-4892-a838-603e3f89b1bb
title: Usando o modo de composição para controlar a mesclagem alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db54c71ac9687a1ddf28db09b922b7799d0ebaa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967740"
---
# <a name="using-compositing-mode-to-control-alpha-blending"></a><span data-ttu-id="f0225-103">Usando o modo de composição para controlar a mesclagem alfa</span><span class="sxs-lookup"><span data-stu-id="f0225-103">Using Compositing Mode to Control Alpha Blending</span></span>

<span data-ttu-id="f0225-104">Pode haver ocasiões em que você deseja criar um bitmap fora da tela com as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="f0225-104">There might be times when you want to create an off-screen bitmap that has the following characteristics:</span></span>

-   <span data-ttu-id="f0225-105">Cores com valores alfabéticos inferiores a 255.</span><span class="sxs-lookup"><span data-stu-id="f0225-105">Colors have alpha values that are less than 255.</span></span>
-   <span data-ttu-id="f0225-106">As cores não têm combinação alfa umas com as outras ao criar o bitmap.</span><span class="sxs-lookup"><span data-stu-id="f0225-106">Colors are not alpha blended with each other as you create the bitmap.</span></span>
-   <span data-ttu-id="f0225-107">Ao exibir o bitmap terminado, as cores no bitmap são combinadas em alfo com as cores da tela de fundo no dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f0225-107">When you display the finished bitmap, colors in the bitmap are alpha blended with the background colors on the display device.</span></span>

<span data-ttu-id="f0225-108">Para criar um bitmap desse tipo, construa um objeto de [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) em branco e, em seguida, construa um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) com base nesse bitmap.</span><span class="sxs-lookup"><span data-stu-id="f0225-108">To create such a bitmap, construct a blank [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object, and then construct a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on that bitmap.</span></span> <span data-ttu-id="f0225-109">Defina o modo de composição do objeto **gráfico** como CompositingModeSourceCopy.</span><span class="sxs-lookup"><span data-stu-id="f0225-109">Set the compositing mode of the **Graphics** object to CompositingModeSourceCopy.</span></span>

<span data-ttu-id="f0225-110">O exemplo a seguir cria um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) com base em um objeto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) .</span><span class="sxs-lookup"><span data-stu-id="f0225-110">The following example creates a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="f0225-111">O código usa o objeto **Graphics** junto com dois pincéis semitransparentes (alfa = 160) para pintar no bitmap.</span><span class="sxs-lookup"><span data-stu-id="f0225-111">The code uses the **Graphics** object along with two semitransparent brushes (alpha = 160) to paint on the bitmap.</span></span> <span data-ttu-id="f0225-112">O código preenche uma elipse vermelha e uma elipse verde usando os pincéis semitransparentes.</span><span class="sxs-lookup"><span data-stu-id="f0225-112">The code fills a red ellipse and a green ellipse using the semitransparent brushes.</span></span> <span data-ttu-id="f0225-113">A elipse verde sobrepõe a elipse vermelha, mas o verde não é mesclado com o vermelho porque o modo de composição do objeto **gráfico** é definido como CompositingModeSourceCopy.</span><span class="sxs-lookup"><span data-stu-id="f0225-113">The green ellipse overlaps the red ellipse, but the green is not blended with the red because the compositing mode of the **Graphics** object is set to CompositingModeSourceCopy.</span></span>

<span data-ttu-id="f0225-114">Em seguida, o código se prepara para desenhar na tela chamando [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) e criando um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) com base em um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f0225-114">Next the code prepares to draw on the screen by calling [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) and creating a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a device context.</span></span> <span data-ttu-id="f0225-115">O código desenha o bitmap na tela duas vezes: uma vez em uma tela de fundo branca e uma vez em uma tela de fundo multicolorida.</span><span class="sxs-lookup"><span data-stu-id="f0225-115">The code draws the bitmap on the screen twice: once on a white background and once on a multicolored background.</span></span> <span data-ttu-id="f0225-116">Os pixels no bitmap que fazem parte das duas elipses têm um componente alfa de 160, de forma que as elipses são mescladas com as cores da tela de fundo na tela.</span><span class="sxs-lookup"><span data-stu-id="f0225-116">The pixels in the bitmap that are part of the two ellipses have an alpha component of 160, so the ellipses are blended with the background colors on the screen.</span></span>


```
// Create a blank bitmap.
Bitmap bitmap(180, 100);
// Create a Graphics object that can be used to draw on the bitmap.
Graphics bitmapGraphics(&bitmap);
// Create a red brush and a green brush, each with an alpha value of 160.
SolidBrush redBrush(Color(210, 255, 0, 0));
SolidBrush greenBrush(Color(210, 0, 255, 0));
// Set the compositing mode so that when overlapping ellipses are drawn,
// the colors of the ellipses are not blended.
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
// Fill an ellipse using a red brush that has an alpha value of 160.
bitmapGraphics.FillEllipse(&redBrush, 0, 0, 150, 70);
// Fill a second ellipse using green brush that has an alpha value of 160. 
// The green ellipse overlaps the red ellipse, but the green is not 
// blended with the red.
bitmapGraphics.FillEllipse(&greenBrush, 30, 30, 150, 70);
// Prepare to draw on the screen.
hdc = BeginPaint(hWnd, &ps);
Graphics* pGraphics = new Graphics(hdc);
pGraphics->SetCompositingQuality(CompositingQualityGammaCorrected);
// Draw a multicolored background.
SolidBrush brush(Color((ARGB)Color::Aqua));
pGraphics->FillRectangle(&brush, 200, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Yellow));
pGraphics->FillRectangle(&brush, 260, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Fuchsia));
pGraphics->FillRectangle(&brush, 320, 0, 60, 100);
   
// Display the bitmap on a white background.
pGraphics->DrawImage(&bitmap, 0, 0);
// Display the bitmap on a multicolored background.
pGraphics->DrawImage(&bitmap, 200, 0);
delete pGraphics;
EndPaint(hWnd, &ps);
```



<span data-ttu-id="f0225-117">A ilustração a seguir mostra a saída do código anterior.</span><span class="sxs-lookup"><span data-stu-id="f0225-117">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="f0225-118">Observe que as elipses são mescladas com a tela de fundo, mas elas não são mescladas uma com a outra.</span><span class="sxs-lookup"><span data-stu-id="f0225-118">Note that the ellipses are blended with the background, but they are not blended with each other.</span></span>

![ilustração mostrando duas elipses com cores diferentes, cada uma misturada com seu plano de fundo multicolorido](images/sourcecopy.png)

<span data-ttu-id="f0225-120">O exemplo de código anterior tem a seguinte instrução:</span><span class="sxs-lookup"><span data-stu-id="f0225-120">The preceding code example has the following statement:</span></span>


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



<span data-ttu-id="f0225-121">Se desejar que as elipses sejam mescladas entre si e com a tela de fundo, altere essa instrução para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f0225-121">If you want the ellipses to be blended with each other as well as with the background, change that statement to the following:</span></span>


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



<span data-ttu-id="f0225-122">A ilustração a seguir mostra a saída do código revisado.</span><span class="sxs-lookup"><span data-stu-id="f0225-122">The following illustration shows the output of the revised code.</span></span>

![usando o modo de composição para controlar a ilustração de mistura alfa](images/sourceover.png)

 

 



