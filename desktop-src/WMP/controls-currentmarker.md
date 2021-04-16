---
title: Controls. currentMarker
description: A propriedade currentMarker especifica ou recupera o número do marcador atual.
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- Controls. currentMarker Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentMarker
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aae8af226b62550b3faae9389385d321bf10aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758233"
---
# <a name="controlscurrentmarker"></a><span data-ttu-id="6b1fc-104">Controls. currentMarker</span><span class="sxs-lookup"><span data-stu-id="6b1fc-104">Controls.currentMarker</span></span>

<span data-ttu-id="6b1fc-105">A propriedade **currentMarker** especifica ou recupera o número do marcador atual.</span><span class="sxs-lookup"><span data-stu-id="6b1fc-105">The **currentMarker** property specifies or retrieves the current marker number.</span></span>

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a><span data-ttu-id="6b1fc-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="6b1fc-106">Possible Values</span></span>

<span data-ttu-id="6b1fc-107">Essa propriedade é um **número** de leitura/gravação (**longo**) com um valor padrão de zero.</span><span class="sxs-lookup"><span data-stu-id="6b1fc-107">This property is a read/write **Number** (**long**) with a default value of zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b1fc-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b1fc-108">Remarks</span></span>

<span data-ttu-id="6b1fc-109">A definição de **currentMarker** faz com que a reprodução seja iniciada a partir do marcador especificado.</span><span class="sxs-lookup"><span data-stu-id="6b1fc-109">Setting **currentMarker** causes playback to start from the specified marker.</span></span> <span data-ttu-id="6b1fc-110">Antes de tentar definir **currentMarker**, determine se um arquivo tem marcadores e quantos deles tem usando **markerCount**.</span><span class="sxs-lookup"><span data-stu-id="6b1fc-110">Before attempting to set **currentMarker**, determine whether a file has markers and how many it has by using **markerCount**.</span></span> <span data-ttu-id="6b1fc-111">Se um arquivo não tiver marcadores, definir **currentMarker** como qualquer coisa, exceto zero, resultará em um erro.</span><span class="sxs-lookup"><span data-stu-id="6b1fc-111">If a file has no markers, setting **currentMarker** to anything but zero results in an error.</span></span> <span data-ttu-id="6b1fc-112">A definição de **currentMarker** como um número maior que **markerCount** também resulta em um erro.</span><span class="sxs-lookup"><span data-stu-id="6b1fc-112">Setting **currentMarker** to a number higher than **markerCount** also results in an error.</span></span>

<span data-ttu-id="6b1fc-113">A propriedade **currentMarker** sempre retorna o marcador atual ou último, o que significa que a posição real do arquivo pode ser no marcador atual ou antes do próximo marcador.</span><span class="sxs-lookup"><span data-stu-id="6b1fc-113">The **currentMarker** property always returns the current or last marker, which means the actual file position can be either at the current marker or before the next marker.</span></span> <span data-ttu-id="6b1fc-114">Os marcadores são numerados começando em 1, portanto, se um arquivo tiver marcadores, você poderá definir **currentMarker** como zero para alterar a posição do arquivo para zero.</span><span class="sxs-lookup"><span data-stu-id="6b1fc-114">Markers are numbered beginning at 1, so if a file has markers, you can set **currentMarker** to zero to change the file position to zero.</span></span>

<span data-ttu-id="6b1fc-115">Até que o item de mídia atual seja definido (usando o *Player*.**URL** ou *Player*. **currentMedia**), **currentMarker** retorna zero.</span><span class="sxs-lookup"><span data-stu-id="6b1fc-115">Until the current media item is set (using *Player*.**URL** or *Player*.**currentMedia**), **currentMarker** returns zero.</span></span>

## <a name="examples"></a><span data-ttu-id="6b1fc-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6b1fc-116">Examples</span></span>

<span data-ttu-id="6b1fc-117">O exemplo de JScript a seguir usa **currentMarker** para iniciar a reprodução de vídeo do marcador que corresponde à propriedade **SelectedIndex** de um elemento HTML SELECT.</span><span class="sxs-lookup"><span data-stu-id="6b1fc-117">The following JScript example uses **currentMarker** to start video playback from the marker that corresponds to the **selectedIndex** property of an HTML SELECT element.</span></span> <span data-ttu-id="6b1fc-118">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6b1fc-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = "markers"  NAME = "markers"  LANGUAGE = "JScript"

    /* Seek to the marker number that corresponds to the SELECT element
       selectedIndex value when the list selection changes. */
    onChange = "Player.controls.currentMarker = markers.selectedIndex + 1;
">

    /* Fill the SELECT element with the marker identifiers. */
    <OPTION SELECTED>Sunrise
    <OPTION>Car chase 
    <OPTION>Happy ending
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="6b1fc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b1fc-119">Requirements</span></span>



| <span data-ttu-id="6b1fc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b1fc-120">Requirement</span></span> | <span data-ttu-id="6b1fc-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6b1fc-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b1fc-122">Versão</span><span class="sxs-lookup"><span data-stu-id="6b1fc-122">Version</span></span><br/> | <span data-ttu-id="6b1fc-123">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6b1fc-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6b1fc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6b1fc-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="6b1fc-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b1fc-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b1fc-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b1fc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b1fc-127">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="6b1fc-127">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="6b1fc-128">**Media. markerCount**</span><span class="sxs-lookup"><span data-stu-id="6b1fc-128">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="6b1fc-129">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="6b1fc-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="6b1fc-130">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="6b1fc-130">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





