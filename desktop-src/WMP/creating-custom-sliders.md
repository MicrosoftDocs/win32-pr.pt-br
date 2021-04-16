---
title: Criando controles deslizantes personalizados
description: Criando controles deslizantes personalizados
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- Criando capas, controles deslizantes
- Capas, controles deslizantes do Windows Media Player
- capas, controles deslizantes
- controles deslizantes em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f205d46af003589fcc2c3b741a253ea08fae12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498752"
---
# <a name="creating-custom-sliders"></a><span data-ttu-id="e1302-107">Criando controles deslizantes personalizados</span><span class="sxs-lookup"><span data-stu-id="e1302-107">Creating Custom Sliders</span></span>

<span data-ttu-id="e1302-108">Você pode criar controles deslizantes personalizados em qualquer forma desejada.</span><span class="sxs-lookup"><span data-stu-id="e1302-108">You can create custom sliders in any shape you want.</span></span> <span data-ttu-id="e1302-109">Neste exemplo, uma faixa simples é escolhida, mas a forma real pode ser qualquer coisa.</span><span class="sxs-lookup"><span data-stu-id="e1302-109">For this example, a simple strip is chosen, but the actual shape can be anything.</span></span> <span data-ttu-id="e1302-110">Este é o código para o elemento **CUSTOMSLIDER** :</span><span class="sxs-lookup"><span data-stu-id="e1302-110">Here is the code for the **CUSTOMSLIDER** element:</span></span>


```C++
<CustomSlider 
  top="160"
  left="130"
  min="0"
  max="100"
  toolTip="volume control"
  image="slider.bmp"
  positionImage="graymap.bmp"
  enabled="true"
  value="wmpprop:player.settings.volume"
  value_onchange="player.settings.volume = value" />

```



<span data-ttu-id="e1302-111">Isso configura um valor inicial para o controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="e1302-111">This sets up an initial value for the slider.</span></span> <span data-ttu-id="e1302-112">Dois novos bitmaps são introduzidos.</span><span class="sxs-lookup"><span data-stu-id="e1302-112">Two new bitmaps are introduced.</span></span> <span data-ttu-id="e1302-113">Um é o bitmap em escala de cinza (slider.bmp) que define quais valores serão usados quando clicados e o outro (slider.bmp) que determina qual imagem será mostrada quando uma parte específica da escala de cinza for clicada.</span><span class="sxs-lookup"><span data-stu-id="e1302-113">One is the grayscale bitmap (slider.bmp) that defines which values will be used when clicked on, and the other (slider.bmp) that determines which image will be shown when a particular portion of the grayscale is clicked on.</span></span>

<span data-ttu-id="e1302-114">O valor inicial é determinado pela escuta do volume com wmpprop e, em seguida, o volume pode ser alterado quando o usuário clica em uma parte do controle deslizante que dispara uma alteração no valor.</span><span class="sxs-lookup"><span data-stu-id="e1302-114">The initial value is determined by listening to the volume with wmpprop and then the volume can be changed when the user clicks on a portion of the slider that triggers a change in value.</span></span>

<span data-ttu-id="e1302-115">Você pode ver uma aparência de controle deslizante de trabalho semelhante na seção de exemplo do SDK.</span><span class="sxs-lookup"><span data-stu-id="e1302-115">You can see a similar working slider skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1302-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1302-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1302-117">**Guia de criação de capa**</span><span class="sxs-lookup"><span data-stu-id="e1302-117">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




