---
title: Método Controls. fastForward
description: O método fastForward inicia a reprodução rápida do item de mídia na direção de encaminhamento. | Método Controls. fastForward
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- método fastForward Windows Media Player
- método fastForward Windows Media Player, classe Controls
- Classe Controls Windows Media Player, método fastForward
topic_type:
- apiref
api_name:
- Controls.fastForward
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d033b8b025955e57a9c3ebed00a6d7a92a666e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813180"
---
# <a name="controlsfastforward-method"></a><span data-ttu-id="328dc-107">Método Controls. fastForward</span><span class="sxs-lookup"><span data-stu-id="328dc-107">Controls.fastForward method</span></span>

<span data-ttu-id="328dc-108">O método **Fastforward** inicia a reprodução rápida do item de mídia na direção de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="328dc-108">The **fastForward** method starts fast play of the media item in the forward direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="328dc-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="328dc-109">Syntax</span></span>


```JScript
Controls.fastForward()
```



## <a name="parameters"></a><span data-ttu-id="328dc-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="328dc-110">Parameters</span></span>

<span data-ttu-id="328dc-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="328dc-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="328dc-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="328dc-112">Return value</span></span>

<span data-ttu-id="328dc-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="328dc-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="328dc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="328dc-114">Remarks</span></span>

<span data-ttu-id="328dc-115">O método **Fastforward** reproduz o clipe em cinco vezes a velocidade normal.</span><span class="sxs-lookup"><span data-stu-id="328dc-115">The **fastForward** method plays the clip back at five times the normal speed.</span></span> <span data-ttu-id="328dc-116">Invocar **Fastforward** altera as *configurações*. **taxa** de propriedade para 5,0.</span><span class="sxs-lookup"><span data-stu-id="328dc-116">Invoking **fastForward** changes the *Settings*.**rate** property to 5.0.</span></span> <span data-ttu-id="328dc-117">Se a **taxa** for alterada posteriormente, ou se **Play** ou **Stop** for chamado, o Windows Media Player cessará o encaminhamento rápido.</span><span class="sxs-lookup"><span data-stu-id="328dc-117">If **rate** is subsequently changed, or if **play** or **stop** is called, Windows Media Player will cease fast forwarding.</span></span>

<span data-ttu-id="328dc-118">O método **Fastforward** não funciona para transmissões ao vivo e certos tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="328dc-118">The **fastForward** method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="328dc-119">Para determinar se você pode avançar rapidamente em um clipe, chame **IsAvailable**("Fastforward").</span><span class="sxs-lookup"><span data-stu-id="328dc-119">To determine whether you can fast forward in a clip, call **isAvailable**("FastForward").</span></span>

## <a name="examples"></a><span data-ttu-id="328dc-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="328dc-120">Examples</span></span>

<span data-ttu-id="328dc-121">O exemplo a seguir cria um elemento de botão HTML que usa **Fastforward** para iniciar a reprodução rápida do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="328dc-121">The following example creates an HTML BUTTON element that uses **fastForward** to start fast play of the media item.</span></span> <span data-ttu-id="328dc-122">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="328dc-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "FF"  NAME = "FF"  VALUE = ">>"  

    /* Execute JScript when the BUTTON is clicked. 
       Check first to make sure fast-forward mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastForward'))
        Player.controls.fastForward();
">

```



## <a name="requirements"></a><span data-ttu-id="328dc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="328dc-123">Requirements</span></span>



| <span data-ttu-id="328dc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="328dc-124">Requirement</span></span> | <span data-ttu-id="328dc-125">Valor</span><span class="sxs-lookup"><span data-stu-id="328dc-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="328dc-126">Versão</span><span class="sxs-lookup"><span data-stu-id="328dc-126">Version</span></span><br/> | <span data-ttu-id="328dc-127">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="328dc-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="328dc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="328dc-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="328dc-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="328dc-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="328dc-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="328dc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="328dc-131">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="328dc-131">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="328dc-132">**Controls. IsAvailable**</span><span class="sxs-lookup"><span data-stu-id="328dc-132">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> <dt>

[<span data-ttu-id="328dc-133">**Controls. Play**</span><span class="sxs-lookup"><span data-stu-id="328dc-133">**Controls.play**</span></span>](controls-play.md)
</dt> <dt>

[<span data-ttu-id="328dc-134">**Controls. Stop**</span><span class="sxs-lookup"><span data-stu-id="328dc-134">**Controls.stop**</span></span>](controls-stop.md)
</dt> <dt>

[<span data-ttu-id="328dc-135">**Settings. Rate**</span><span class="sxs-lookup"><span data-stu-id="328dc-135">**Settings.rate**</span></span>](settings-rate.md)
</dt> </dl>

 

 





