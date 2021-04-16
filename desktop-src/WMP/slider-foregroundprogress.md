---
title: SLIDER. foregroundProgress
description: O atributo foregroundProgress especifica ou recupera a posição atual da barra de progresso em primeiro plano como uma porcentagem da área do controle deslizante.
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- Controle deslizante. foregroundProgress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4597630453444564411d0bcfad8dc6b39914d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754073"
---
# <a name="sliderforegroundprogress"></a><span data-ttu-id="8be16-104">SLIDER. foregroundProgress</span><span class="sxs-lookup"><span data-stu-id="8be16-104">SLIDER.foregroundProgress</span></span>

<span data-ttu-id="8be16-105">O atributo **foregroundProgress** especifica ou recupera a posição atual da barra de progresso em primeiro plano como uma porcentagem da área do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="8be16-105">The **foregroundProgress** attribute specifies or retrieves the current position of the foreground progress bar as a percentage of the slider area.</span></span>

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a><span data-ttu-id="8be16-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="8be16-106">Possible Values</span></span>

<span data-ttu-id="8be16-107">Esse atributo é um **número** de leitura/gravação (**float**) que varia de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="8be16-107">This attribute is a read/write **Number** (**float**) ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="8be16-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="8be16-108">Remarks</span></span>

<span data-ttu-id="8be16-109">Esse atributo é usado principalmente para acompanhar o progresso do download de um arquivo de mídia enquanto controla simultaneamente a posição de execução atual do arquivo usando o atributo **Value** .</span><span class="sxs-lookup"><span data-stu-id="8be16-109">This attribute is used primarily to track the download progress of a media file while simultaneously tracking the current play position of the file using the **value** attribute.</span></span> <span data-ttu-id="8be16-110">A posição da miniatura deslizante é restrita à área do andamento do primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="8be16-110">The position of the slider thumb is constrained to the area of the foreground progress.</span></span> <span data-ttu-id="8be16-111">Isso permite que a busca interativa ocorra somente dentro da parte disponível de um arquivo de download.</span><span class="sxs-lookup"><span data-stu-id="8be16-111">This allows interactive seeking to take place only within the available portion of a downloading file.</span></span>

<span data-ttu-id="8be16-112">Para usar essa funcionalidade, o atributo **useForegroundProgress** deve ser definido como true.</span><span class="sxs-lookup"><span data-stu-id="8be16-112">To use this functionality, the **useForegroundProgress** attribute must be set to true.</span></span>

## <a name="examples"></a><span data-ttu-id="8be16-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8be16-113">Examples</span></span>


```C++
<SLIDER
  id="seek"
  backgroundColor="blue"
  foregroundColor="red"
  thumbImage="seekthumb.bmp"
  min="0"
  max="wmpprop:player.currentMedia.duration"
  value="wmpprop:player.controls.currentPosition"
  useForegroundProgress="true"
  foregroundProgress="wmpprop:player.network.downloadProgress"
  ondragend="player.controls.currentposition=value"
/>

```



## <a name="requirements"></a><span data-ttu-id="8be16-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8be16-114">Requirements</span></span>



| <span data-ttu-id="8be16-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8be16-115">Requirement</span></span> | <span data-ttu-id="8be16-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8be16-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8be16-117">Versão</span><span class="sxs-lookup"><span data-stu-id="8be16-117">Version</span></span><br/> | <span data-ttu-id="8be16-118">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8be16-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8be16-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="8be16-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be16-120">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="8be16-120">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="8be16-121">**SLIDER. min**</span><span class="sxs-lookup"><span data-stu-id="8be16-121">**SLIDER.min**</span></span>](slider-min.md)
</dt> <dt>

[<span data-ttu-id="8be16-122">**SLIDER. Max**</span><span class="sxs-lookup"><span data-stu-id="8be16-122">**SLIDER.max**</span></span>](slider-max.md)
</dt> <dt>

[<span data-ttu-id="8be16-123">**SLIDER. useForegroundProgress**</span><span class="sxs-lookup"><span data-stu-id="8be16-123">**SLIDER.useForegroundProgress**</span></span>](slider-useforegroundprogress.md)
</dt> <dt>

[<span data-ttu-id="8be16-124">**Controle deslizante. valor**</span><span class="sxs-lookup"><span data-stu-id="8be16-124">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





