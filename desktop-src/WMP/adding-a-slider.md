---
title: Adicionando um controle deslizante
description: Adicionando um controle deslizante
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- Criando capas, controles deslizantes
- Capas, controles deslizantes do Windows Media Player
- capas, controles deslizantes
- controles deslizantes em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efcae55b3826b69a7c88fed5a23a262526c9dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005772"
---
# <a name="adding-a-slider"></a><span data-ttu-id="27c72-107">Adicionando um controle deslizante</span><span class="sxs-lookup"><span data-stu-id="27c72-107">Adding a Slider</span></span>

<span data-ttu-id="27c72-108">Você pode adicionar um controle deslizante para mostrar a posição atual da mídia e também permitir que o usuário altere a posição no arquivo de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="27c72-108">You can add a slider to show the current position of the media, and also enable the user to change the position in the current media file.</span></span>

<span data-ttu-id="27c72-109">Primeiro, você deve adicionar o elemento **Slider** :</span><span class="sxs-lookup"><span data-stu-id="27c72-109">First you must add the **SLIDER** element:</span></span>


```C++
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
  thumbImage = "thumb.bmp"/>

```



<span data-ttu-id="27c72-110">Isso define um valor máximo com base na duração do arquivo de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="27c72-110">This sets a maximum value based on the duration of the current media file.</span></span> <span data-ttu-id="27c72-111">Isso usa um pequeno bitmap de imagem Thumb que é apenas 10 pixels por um quadrado verde de 10 pixels.</span><span class="sxs-lookup"><span data-stu-id="27c72-111">This uses a tiny thumb image bitmap that is just a 10 pixel by 10 pixel green square.</span></span> <span data-ttu-id="27c72-112">O plano de fundo do controle deslizante será vermelho e o primeiro plano será azul.</span><span class="sxs-lookup"><span data-stu-id="27c72-112">The background of the slider will be red and the foreground will be blue.</span></span> <span data-ttu-id="27c72-113">Quando o usuário arrasta a imagem em miniatura para uma nova posição e deixa o botão do mouse, a mídia muda para essa posição.</span><span class="sxs-lookup"><span data-stu-id="27c72-113">When the user drags the thumb image to a new position and lets go of the mouse button, the media will change to that position.</span></span>

<span data-ttu-id="27c72-114">Mas o controle deslizante não se moverá por si só, a menos que você meça a posição atual com o atributo **\_ onChange CurrentPosition** do elemento **Controls** , que é inserido no elemento **Player** .</span><span class="sxs-lookup"><span data-stu-id="27c72-114">But the slider will not move by itself unless you measure the current position with the **currentPosition\_onchange** attribute of the **CONTROLS** element, which is embedded in the **PLAYER** element.</span></span>


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



<span data-ttu-id="27c72-115">Quando a posição da mídia é alterada, isso dispara um evento que executa a linha de código que altera o valor do controle deslizante para a posição atual da mídia.</span><span class="sxs-lookup"><span data-stu-id="27c72-115">When the position of the media changes, this fires an event which then runs the line of code that changes the value of the slider to the current position of the media.</span></span>

<span data-ttu-id="27c72-116">Você pode ver uma aparência de controle deslizante de trabalho semelhante na seção de exemplo do SDK.</span><span class="sxs-lookup"><span data-stu-id="27c72-116">You can see a similar working slider skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27c72-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27c72-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27c72-118">**Guia de criação de capa**</span><span class="sxs-lookup"><span data-stu-id="27c72-118">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




