---
title: Método Controls. fastReverse
description: O método fastReverse inicia a verificação rápida do item de mídia na direção inversa.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- método fastReverse Windows Media Player
- método fastReverse Windows Media Player, classe Controls
- Classe Controls Windows Media Player, método fastReverse
topic_type:
- apiref
api_name:
- Controls.fastReverse
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e5a63c4299bf08c25e36e2d61924f3fb171792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758232"
---
# <a name="controlsfastreverse-method"></a><span data-ttu-id="c9290-106">Método Controls. fastReverse</span><span class="sxs-lookup"><span data-stu-id="c9290-106">Controls.fastReverse method</span></span>

<span data-ttu-id="c9290-107">O método **fastReverse** inicia a verificação rápida do item de mídia na direção inversa.</span><span class="sxs-lookup"><span data-stu-id="c9290-107">The **fastReverse** method starts fast scanning of the media item in the reverse direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9290-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9290-108">Syntax</span></span>


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a><span data-ttu-id="c9290-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9290-109">Parameters</span></span>

<span data-ttu-id="c9290-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c9290-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9290-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c9290-111">Return value</span></span>

<span data-ttu-id="c9290-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c9290-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9290-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9290-113">Remarks</span></span>

<span data-ttu-id="c9290-114">O método **fastReverse** examina o clipe de forma inversa em cinco vezes a velocidade normal, exibindo apenas os quadros-chave se for um arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c9290-114">The **fastReverse** method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file.</span></span> <span data-ttu-id="c9290-115">Invocar **fastReverse** altera as *configurações*. **taxa** de propriedade para 5,0.</span><span class="sxs-lookup"><span data-stu-id="c9290-115">Invoking **fastReverse** changes the *Settings*.**rate** property to  5.0.</span></span> <span data-ttu-id="c9290-116">Se a **taxa** for alterada posteriormente, ou se **Play** ou **Stop** for chamado, o Windows Media Player deixará de ser revertido rapidamente.</span><span class="sxs-lookup"><span data-stu-id="c9290-116">If **rate** is subsequently changed, or if **play** or **stop** is called, Windows Media Player will cease fast reverse.</span></span>

<span data-ttu-id="c9290-117">Se o item fizer parte de uma lista de reprodução, o **fastReverse** para no início da faixa atual. Por exemplo, se Track 3 estiver em **fastReverse**, quando o início do Track 3 for atingido, o Windows Media Player não vai para o Track 2.</span><span class="sxs-lookup"><span data-stu-id="c9290-117">If the item is part of a playlist, **fastReverse** stops at the beginning of the current track. For instance, if track 3 is in **fastReverse**, when the beginning of track 3 is reached, Windows Media Player will not go to track 2.</span></span> <span data-ttu-id="c9290-118">A contagem de execuções não é incrementada ao chamar **fastReverse**.</span><span class="sxs-lookup"><span data-stu-id="c9290-118">The play count is not incremented when calling **fastReverse**.</span></span>

<span data-ttu-id="c9290-119">Se você chamar **Fastforward** enquanto **fastReverse** estiver em vigor, **fastReverse** será interrompido e **Fastforward** será iniciado.</span><span class="sxs-lookup"><span data-stu-id="c9290-119">If you call **fastForward** while **fastReverse** is in effect, **fastReverse** will be stopped and **fastForward** will begin.</span></span>

<span data-ttu-id="c9290-120">Esse método não funciona para transmissões ao vivo e certos tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="c9290-120">This method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="c9290-121">Para determinar se você pode usar a inversão rápida em um clipe, chame **IsAvailable**("fastReverse").</span><span class="sxs-lookup"><span data-stu-id="c9290-121">To determine whether you can use fast reverse in a clip, call **isAvailable**("FastReverse").</span></span>

## <a name="examples"></a><span data-ttu-id="c9290-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c9290-122">Examples</span></span>

<span data-ttu-id="c9290-123">O exemplo a seguir cria um elemento de botão HTML que usa **fastReverse** para iniciar a reprodução rápida do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="c9290-123">The following example creates an HTML BUTTON element that uses **fastReverse** to start fast-reverse play of the media item.</span></span> <span data-ttu-id="c9290-124">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c9290-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "REW"  NAME = "REW"  VALUE = "<<"  

    /* Run JScript when the BUTTON is clicked. 
       Check first to make sure fast-reverse mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastReverse'))
        Player.controls.fastReverse();
">
```



## <a name="requirements"></a><span data-ttu-id="c9290-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9290-125">Requirements</span></span>



| <span data-ttu-id="c9290-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9290-126">Requirement</span></span> | <span data-ttu-id="c9290-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c9290-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9290-128">Versão</span><span class="sxs-lookup"><span data-stu-id="c9290-128">Version</span></span><br/> | <span data-ttu-id="c9290-129">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c9290-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c9290-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c9290-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="c9290-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9290-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9290-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9290-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9290-133">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="c9290-133">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="c9290-134">**Controls. fastForward**</span><span class="sxs-lookup"><span data-stu-id="c9290-134">**Controls.fastForward**</span></span>](controls-fastforward.md)
</dt> <dt>

[<span data-ttu-id="c9290-135">**Controls. IsAvailable**</span><span class="sxs-lookup"><span data-stu-id="c9290-135">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> <dt>

[<span data-ttu-id="c9290-136">**Controls. Play**</span><span class="sxs-lookup"><span data-stu-id="c9290-136">**Controls.play**</span></span>](controls-play.md)
</dt> <dt>

[<span data-ttu-id="c9290-137">**Controls. Stop**</span><span class="sxs-lookup"><span data-stu-id="c9290-137">**Controls.stop**</span></span>](controls-stop.md)
</dt> <dt>

[<span data-ttu-id="c9290-138">**Settings. Rate**</span><span class="sxs-lookup"><span data-stu-id="c9290-138">**Settings.rate**</span></span>](settings-rate.md)
</dt> </dl>

 

 





