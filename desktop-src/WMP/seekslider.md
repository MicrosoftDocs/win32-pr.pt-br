---
title: SEEKSLIDER
description: Este é um controle deslizante predefinido com os valores padrão a seguir. | SEEKSLIDER
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- SEEKSLIDER Windows Media Player
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59808fa7c41acfcc28b715362b8724c7f113faee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747286"
---
# <a name="seekslider"></a><span data-ttu-id="61d33-105">SEEKSLIDER</span><span class="sxs-lookup"><span data-stu-id="61d33-105">SEEKSLIDER</span></span>

<span data-ttu-id="61d33-106">Este é um **controle deslizante** predefinido com os valores padrão a seguir.</span><span class="sxs-lookup"><span data-stu-id="61d33-106">This is a predefined **SLIDER** with the following default values.</span></span>

``` syntax
toolTip="Seek"
foregroundProgress="wmpprop:player.network.downloadProgress"
max="wmpprop:player.currentMedia.duration"
min="0"
value="wmpprop:player.controls.currentPosition"
onDragEnd="jscript:player.controls.currentPosition=value;"
useForegroundProgress="true"
```

## <a name="remarks"></a><span data-ttu-id="61d33-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="61d33-107">Remarks</span></span>

<span data-ttu-id="61d33-108">Isso cria um controle **deslizante** que procura o arquivo de mídia em qualquer posição.</span><span class="sxs-lookup"><span data-stu-id="61d33-108">This creates a **SLIDER** control that seeks the media file to any position.</span></span> <span data-ttu-id="61d33-109">As dicas de ferramenta são localizadas.</span><span class="sxs-lookup"><span data-stu-id="61d33-109">The ToolTips are localized.</span></span> <span data-ttu-id="61d33-110">Todas as propriedades desse **controle deslizante** podem ser substituídas especificando-as explicitamente.</span><span class="sxs-lookup"><span data-stu-id="61d33-110">All properties of this **SLIDER** can be overridden by explicitly specifying them.</span></span>

## <a name="requirements"></a><span data-ttu-id="61d33-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61d33-111">Requirements</span></span>



| <span data-ttu-id="61d33-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="61d33-112">Requirement</span></span> | <span data-ttu-id="61d33-113">Valor</span><span class="sxs-lookup"><span data-stu-id="61d33-113">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="61d33-114">Versão</span><span class="sxs-lookup"><span data-stu-id="61d33-114">Version</span></span><br/> | <span data-ttu-id="61d33-115">Windows Media Player 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="61d33-115">Windows Media Player 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="61d33-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="61d33-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61d33-117">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="61d33-117">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





