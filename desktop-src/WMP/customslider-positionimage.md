---
title: CUSTOMSLIDER.positionImage
description: O atributo positionImage especifica ou recupera o mapa de imagem usado para determinar qual imagem de posição do arquivo de imagem a ser exibida.
ms.assetid: 7e99dc21-ebba-438a-a983-190dbe429578
keywords:
- CUSTOMSLIDER. positionImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.positionImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc92a9c263e2b450e64d526ccfc7976fdd6227a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761470"
---
# <a name="customsliderpositionimage"></a><span data-ttu-id="19043-104">CUSTOMSLIDER.positionImage</span><span class="sxs-lookup"><span data-stu-id="19043-104">CUSTOMSLIDER.positionImage</span></span>

<span data-ttu-id="19043-105">O atributo **positionImage** especifica ou recupera o mapa de imagem usado para determinar qual imagem de posição do arquivo de imagem a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="19043-105">The **positionImage** attribute specifies or retrieves the image map used to determine which position image from the image file to display.</span></span>

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a><span data-ttu-id="19043-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="19043-106">Possible Values</span></span>

<span data-ttu-id="19043-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="19043-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="19043-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="19043-108">Remarks</span></span>

<span data-ttu-id="19043-109">Esse atributo é necessário e deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="19043-109">This attribute is required and must be specified.</span></span>

<span data-ttu-id="19043-110">O **positionImage** não é exibido.</span><span class="sxs-lookup"><span data-stu-id="19043-110">The **positionImage** is not displayed.</span></span> <span data-ttu-id="19043-111">Em vez disso, ele serve como um mapa que define as regiões clicáveis da imagem exibida.</span><span class="sxs-lookup"><span data-stu-id="19043-111">Instead, it serves as a map defining the clickable regions of the displayed image.</span></span> <span data-ttu-id="19043-112">A imagem exibida é uma das subimagems do arquivo de imagem e representa o estado real do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="19043-112">The displayed image is one of the sub-images of the image file and represents the actual state of the slider.</span></span> <span data-ttu-id="19043-113">O **positionImage** inclui várias regiões de escala cinza iguais ao número dessas subimagems.</span><span class="sxs-lookup"><span data-stu-id="19043-113">The **positionImage** includes a number of gray scale regions equal to the number of these sub-images.</span></span> <span data-ttu-id="19043-114">As subimagems devem ter as mesmas dimensões que o **positionImage** ou o controle deslizante personalizado não funcionará corretamente.</span><span class="sxs-lookup"><span data-stu-id="19043-114">The sub-images must have the same dimensions as the **positionImage** or the custom slider will not work correctly.</span></span>

<span data-ttu-id="19043-115">Qualquer região que não esteja em escala cinza não será clicável.</span><span class="sxs-lookup"><span data-stu-id="19043-115">Any region that is not in gray scale will not be clickable.</span></span> <span data-ttu-id="19043-116">As regiões clicáveis devem ser definidas para valores de cor que variam uniformemente no espectro de escala cinza de preto para branco, com a primeira região puro preto e a última região em branco puro.</span><span class="sxs-lookup"><span data-stu-id="19043-116">The clickable regions should be set to color values that range evenly across the gray scale spectrum from black to white, with the first region being pure black and the last region being pure white.</span></span> <span data-ttu-id="19043-117">Os valores de cor de cada região sucessiva devem ser incrementados por um valor igual a 255 dividido pelo número total de regiões menos um, arredondando para o número inteiro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="19043-117">The color values of each successive region should be incremented by a value equal to 255 divided by the total number of regions minus one, rounding to the nearest whole number.</span></span>

<span data-ttu-id="19043-118">Por exemplo, se houver seis regiões, o incremento seria 51 (255 dividido por 5) e os seis valores de escala de cinza seriam 0, 51, 102, 153, 204 e 255.</span><span class="sxs-lookup"><span data-stu-id="19043-118">For example, if there are six regions, the increment would be 51 (255 divided by 5), and the six gray scale values would be 0, 51, 102, 153, 204, and 255.</span></span> <span data-ttu-id="19043-119">Os valores de cor hexadecimais para as seis regiões seriam \# 000000, \# 333333, \# 666666, \# 999999, \# CCCCCC e \# FFFFFF.</span><span class="sxs-lookup"><span data-stu-id="19043-119">The hexadecimal color values for the six regions would then be \#000000, \#333333, \#666666, \#999999, \#CCCCCC, and \#FFFFFF.</span></span>

<span data-ttu-id="19043-120">Dessa forma, as regiões terão uma sequência determinada por seus valores de cor de escala cinza e essa sequência corresponderá à sequência de subimagem no arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="19043-120">In this way, the regions will have a sequence dictated by their gray scale color values, and this sequence will correspond to the sequence of sub-images in the image file.</span></span> <span data-ttu-id="19043-121">Quando uma das regiões é clicada, a subimagem correspondente é mostrada e o **valor** do controle deslizante personalizado é atualizado de acordo.</span><span class="sxs-lookup"><span data-stu-id="19043-121">When one of the regions is clicked, the corresponding sub-image is shown and the **value** of the custom slider is updated accordingly.</span></span>

<span data-ttu-id="19043-122">Os tipos de arquivo de imagem com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).</span><span class="sxs-lookup"><span data-stu-id="19043-122">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="examples"></a><span data-ttu-id="19043-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="19043-123">Examples</span></span>

<span data-ttu-id="19043-124">Veja a seguir um exemplo de um controle deslizante personalizado **positionImage**.</span><span class="sxs-lookup"><span data-stu-id="19043-124">The following is an example of a custom slider **positionImage**.</span></span> <span data-ttu-id="19043-125">A imagem correspondente é mostrada na seção de exemplo da propriedade **Image** .</span><span class="sxs-lookup"><span data-stu-id="19043-125">The corresponding image is shown in the example section of the **image** property.</span></span>

![gráfico positionimage de exemplo](images/dialmap.png)

<span data-ttu-id="19043-127">O código a seguir ilustra o uso de atributos **CUSTOMSLIDER** .</span><span class="sxs-lookup"><span data-stu-id="19043-127">The following code illustrates the use of **CUSTOMSLIDER** attributes.</span></span>


```XML
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >

    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    >
      <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition;"
      />
    </PLAYER>

    <SLIDER
      id = "myslider"
      min = "0"
      max = "wmpprop:player.currentMedia.duration"
      onmouseup = "player.controls.currentPosition = myslider.value; "
      tooltip = "current position"
      height = "10"
      width = "180"
      top = "150"
      left = "88"
      backgroundColor = "red"
      foregroundColor = "blue"
      thumbImage = "thumb.bmp"
    />

    <CUSTOMSLIDER
      top = "120"
      left = "23"
      min = "0"
      max = "100"
      borderSize = "10"
      toolTip = "volume control"
      image = "dial.bmp"
      transparencyColor = "#00FFFF"
      positionImage = "dialmap.bmp"
      enabled = "true"
      value = "wmpprop:player.settings.volume"
      value_onchange = "player.settings.volume = value"
    />

    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "100"
    />

    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    > 

      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />

      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />

    </BUTTONGROUP>

  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="19043-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19043-128">Requirements</span></span>



| <span data-ttu-id="19043-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="19043-129">Requirement</span></span> | <span data-ttu-id="19043-130">Valor</span><span class="sxs-lookup"><span data-stu-id="19043-130">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="19043-131">Versão</span><span class="sxs-lookup"><span data-stu-id="19043-131">Version</span></span><br/> | <span data-ttu-id="19043-132">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="19043-132">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19043-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="19043-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19043-134">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="19043-134">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="19043-135">**CUSTOMSLIDER. Image**</span><span class="sxs-lookup"><span data-stu-id="19043-135">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





