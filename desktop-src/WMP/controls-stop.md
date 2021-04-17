---
title: Método Controls. Stop
description: O método Stop interrompe a reprodução do item de mídia. | Método Controls. Stop
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- método Stop Windows Media Player
- método Stop Windows Media Player, classe Controls
- Classe Controls do Windows Media Player, método Stop
topic_type:
- apiref
api_name:
- Controls.stop
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1ffc581fffbce0a341559e82c6bd196f712149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762090"
---
# <a name="controlsstop-method"></a><span data-ttu-id="488f9-107">Método Controls. Stop</span><span class="sxs-lookup"><span data-stu-id="488f9-107">Controls.stop method</span></span>

<span data-ttu-id="488f9-108">O método **Stop** interrompe a reprodução do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="488f9-108">The **stop** method stops playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="488f9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="488f9-109">Syntax</span></span>


```JScript
Controls.stop()
```



## <a name="parameters"></a><span data-ttu-id="488f9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="488f9-110">Parameters</span></span>

<span data-ttu-id="488f9-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="488f9-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="488f9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="488f9-112">Return value</span></span>

<span data-ttu-id="488f9-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="488f9-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="488f9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="488f9-114">Remarks</span></span>

<span data-ttu-id="488f9-115">Esse método faz com que o Windows Media Player libere os recursos do sistema que está usando, como o dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="488f9-115">This method causes Windows Media Player to release any system resources it is using, such as the audio device.</span></span> <span data-ttu-id="488f9-116">O item de mídia atual, no entanto, não é liberado.</span><span class="sxs-lookup"><span data-stu-id="488f9-116">The current media item, however, is not released.</span></span>

<span data-ttu-id="488f9-117">Quando o jogador for interrompido, a faixa retrocederá até o início.</span><span class="sxs-lookup"><span data-stu-id="488f9-117">When the player is stopped, the track rewinds to the beginning.</span></span> <span data-ttu-id="488f9-118">Chamar **Play** começará a reprodução do clipe desde o início.</span><span class="sxs-lookup"><span data-stu-id="488f9-118">Calling **play** will then begin playback of the clip from the beginning.</span></span> <span data-ttu-id="488f9-119">Para interromper uma operação de reprodução sem alterar a posição atual, use o método **Pause** .</span><span class="sxs-lookup"><span data-stu-id="488f9-119">To halt a play operation without changing the current position, use the **pause** method.</span></span>

## <a name="examples"></a><span data-ttu-id="488f9-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="488f9-120">Examples</span></span>

<span data-ttu-id="488f9-121">O exemplo a seguir cria um elemento de botão HTML que usa **parar** para parar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="488f9-121">The following example creates an HTML BUTTON element that uses **stop** to stop playback.</span></span> <span data-ttu-id="488f9-122">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="488f9-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "STOP"  NAME = "STOP"  VALUE = "Stop"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Stop'))

            /* Stop the Player. */
            Player.controls.stop();
">

```



## <a name="requirements"></a><span data-ttu-id="488f9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="488f9-123">Requirements</span></span>



| <span data-ttu-id="488f9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="488f9-124">Requirement</span></span> | <span data-ttu-id="488f9-125">Valor</span><span class="sxs-lookup"><span data-stu-id="488f9-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="488f9-126">Versão</span><span class="sxs-lookup"><span data-stu-id="488f9-126">Version</span></span><br/> | <span data-ttu-id="488f9-127">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="488f9-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="488f9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="488f9-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="488f9-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="488f9-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="488f9-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="488f9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="488f9-131">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="488f9-131">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="488f9-132">**Controles. Next**</span><span class="sxs-lookup"><span data-stu-id="488f9-132">**Controls.next**</span></span>](controls-next.md)
</dt> <dt>

[<span data-ttu-id="488f9-133">**Controls. Pause**</span><span class="sxs-lookup"><span data-stu-id="488f9-133">**Controls.pause**</span></span>](controls-pause.md)
</dt> <dt>

[<span data-ttu-id="488f9-134">**Controles. Previous**</span><span class="sxs-lookup"><span data-stu-id="488f9-134">**Controls.previous**</span></span>](controls-previous.md)
</dt> </dl>

 

 





