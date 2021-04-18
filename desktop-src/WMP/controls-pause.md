---
title: Método Controls. Pause
description: O método pause pausa a reprodução do item de mídia. | Método Controls. Pause
ms.assetid: 7307a3b2-e5d6-4067-bdb5-38011565142a
keywords:
- Método Pause Windows Media Player
- Método Pause Windows Media Player, classe Controls
- Classe Controls do Windows Media Player, método pause
topic_type:
- apiref
api_name:
- Controls.pause
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 898efb51355a1301bc76717f6d0184d0b30d619d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811123"
---
# <a name="controlspause-method"></a><span data-ttu-id="324d5-107">Método Controls. Pause</span><span class="sxs-lookup"><span data-stu-id="324d5-107">Controls.pause method</span></span>

<span data-ttu-id="324d5-108">O método **Pause** pausa a reprodução do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="324d5-108">The **pause** method pauses playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="324d5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="324d5-109">Syntax</span></span>


```JScript
Controls.pause()
```



## <a name="parameters"></a><span data-ttu-id="324d5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="324d5-110">Parameters</span></span>

<span data-ttu-id="324d5-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="324d5-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="324d5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="324d5-112">Return value</span></span>

<span data-ttu-id="324d5-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="324d5-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="324d5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="324d5-114">Remarks</span></span>

<span data-ttu-id="324d5-115">Quando um arquivo é pausado, o Windows Media Player não fornece nenhum recurso do sistema, como o dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="324d5-115">When a file is paused, Windows Media Player does not give up any system resources, such as the audio device.</span></span>

<span data-ttu-id="324d5-116">Determinados tipos de mídia não podem ser pausados, como transmissões ao vivo.</span><span class="sxs-lookup"><span data-stu-id="324d5-116">Certain media types cannot be paused, such as live streams.</span></span> <span data-ttu-id="324d5-117">Para determinar se um determinado tipo de mídia pode ser pausado, use *controles*. **isdisponível (' pause ')**.</span><span class="sxs-lookup"><span data-stu-id="324d5-117">To determine whether a particular media type can be paused, use *Controls*.**isAvailable('Pause')**.</span></span>

## <a name="examples"></a><span data-ttu-id="324d5-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="324d5-118">Examples</span></span>

<span data-ttu-id="324d5-119">O exemplo a seguir cria um elemento de botão HTML que usa **Pause** para pausar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="324d5-119">The following example creates an HTML BUTTON element that uses **pause** to pause playback.</span></span> <span data-ttu-id="324d5-120">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="324d5-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PAUSE"  NAME = "PAUSE"  VALUE = "||"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Pause'))

            /* Pause the Player. */
            Player.controls.pause();
">
```



## <a name="requirements"></a><span data-ttu-id="324d5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="324d5-121">Requirements</span></span>



| <span data-ttu-id="324d5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="324d5-122">Requirement</span></span> | <span data-ttu-id="324d5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="324d5-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="324d5-124">Versão</span><span class="sxs-lookup"><span data-stu-id="324d5-124">Version</span></span><br/> | <span data-ttu-id="324d5-125">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="324d5-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="324d5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="324d5-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="324d5-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="324d5-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="324d5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="324d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="324d5-129">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="324d5-129">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="324d5-130">**Controls. IsAvailable**</span><span class="sxs-lookup"><span data-stu-id="324d5-130">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> </dl>

 

 





