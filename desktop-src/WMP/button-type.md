---
title: Tipo de botão
description: Tipo de botão
ms.assetid: 0c9e72d5-5cc4-4d6f-b184-2c8c8487e366
keywords:
- Aparências móveis do Windows Media Player, tipos de botão
- capas, tipos de botão
- referência para capas, botões
- botões em capas, tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58eeb7402a13730fd7f4030d2e4326fe7f18e63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822401"
---
# <a name="button-type"></a><span data-ttu-id="e6ba4-107">Tipo de botão</span><span class="sxs-lookup"><span data-stu-id="e6ba4-107">Button Type</span></span>

<span data-ttu-id="e6ba4-108">Os botões vêm em dois tipos gerais: local e região.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-108">Buttons come in two general types: location and region.</span></span> <span data-ttu-id="e6ba4-109">Cada tipo geral tem três tipos específicos, fazendo seis tipos de botão.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-109">Each general type has three specific types, making six button types in all.</span></span>

> [!Note]  
> <span data-ttu-id="e6ba4-110">Os tipos de botões são preteridos em capas para Windows Media Player 10 Mobile ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-110">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="e6ba4-111">Tipos de botão de localização</span><span class="sxs-lookup"><span data-stu-id="e6ba4-111">Location Button Types</span></span>

<span data-ttu-id="e6ba4-112">Os botões de localização usam coordenadas para definir seus locais em relação ao plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-112">Location buttons use coordinates to define their locations relative to the background.</span></span> <span data-ttu-id="e6ba4-113">A tabela a seguir mostra os valores válidos para os tipos de botão de localização.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-113">The following table shows the values that are valid for location button types.</span></span> <span data-ttu-id="e6ba4-114">Não é necessário definir valores para tipos que você não usará em sua capa.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-114">You do not need to define values for types you will not be using in your skin.</span></span>



| <span data-ttu-id="e6ba4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e6ba4-115">Value</span></span>  | <span data-ttu-id="e6ba4-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6ba4-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ba4-117">Push</span><span class="sxs-lookup"><span data-stu-id="e6ba4-117">Push</span></span>   | <span data-ttu-id="e6ba4-118">Define um botão que dispara um evento uma vez.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-118">Defines a button that triggers an event once.</span></span> <span data-ttu-id="e6ba4-119">O botão deve ser enviado a cada vez para disparar outros eventos.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-119">The button must be pushed each time to trigger further events.</span></span> <span data-ttu-id="e6ba4-120">Um exemplo seria um botão que se move para o próximo item na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-120">An example would be a button that moves to the next item in the playlist.</span></span> <span data-ttu-id="e6ba4-121">O local do botão é definido por suas coordenadas.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-121">The location of the button is defined by its coordinates.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e6ba4-122">Alternar</span><span class="sxs-lookup"><span data-stu-id="e6ba4-122">Toggle</span></span> | <span data-ttu-id="e6ba4-123">Define um botão que dispara um evento que altera um estado.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-123">Defines a button that triggers an event that changes a state.</span></span> <span data-ttu-id="e6ba4-124">O estado permanece até que o botão seja enviado novamente.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-124">The state remains until the button is pushed again.</span></span> <span data-ttu-id="e6ba4-125">Um exemplo é um botão que embaralha a lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-125">An example is a button that shuffles the playlist.</span></span> <span data-ttu-id="e6ba4-126">Depois que a playlist estiver em um estado em ordem aleatória, ela permanecerá em ordem aleatória até que o botão seja enviado novamente.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-126">Once the playlist is in a shuffled state, it will remain shuffled until the button is pushed again.</span></span> <span data-ttu-id="e6ba4-127">O local do botão é definido por suas coordenadas.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-127">The location of the button is defined by its coordinates.</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="e6ba4-128">2Push</span><span class="sxs-lookup"><span data-stu-id="e6ba4-128">2Push</span></span>  | <span data-ttu-id="e6ba4-129">Define um botão que dispara um evento e, em seguida, muda para um estado que está pronto para disparar um evento diferente.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-129">Defines a button that triggers an event, and then changes to a state that is ready to trigger a different event.</span></span> <span data-ttu-id="e6ba4-130">Os dois Estados são alternados toda vez que o botão é enviado por push.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-130">The two states are toggled every time the button is pushed.</span></span> <span data-ttu-id="e6ba4-131">Um exemplo é um botão que usa a função **PlayPause** para alternar entre reproduzir e pausar o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-131">An example is a button that uses the **PlayPause** function to toggle between playing and pausing the current media item.</span></span> <span data-ttu-id="e6ba4-132">Quando o botão é enviado pela primeira vez, o estado de execução primário é disparado e uma imagem secundária é exibida para indicar que um evento de **pausa** pode ser disparado.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-132">When the button is pushed the first time, the primary Play state is triggered and a secondary image is displayed to indicate that a **Pause** event can be triggered.</span></span> <span data-ttu-id="e6ba4-133">Quando o botão é colocado novamente, o estado de pausa é disparado e a imagem original é exibida para indicar que um evento de **reprodução** pode ser disparado.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-133">When the button is pushed again, the Pause state is triggered and the original image is displayed to indicate that a **Play** event can be triggered.</span></span> <span data-ttu-id="e6ba4-134">O local do botão é definido por suas coordenadas.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-134">The location of the button is defined by its coordinates.</span></span> |



 

<span data-ttu-id="e6ba4-135">Tipos de botão de região</span><span class="sxs-lookup"><span data-stu-id="e6ba4-135">Region Button Types</span></span>

<span data-ttu-id="e6ba4-136">Os botões de região usam áreas de cores na imagem de região para definir onde os toques serão processados para um determinado botão.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-136">Region buttons use color areas in the Region image to define where taps will be processed for a particular button.</span></span> <span data-ttu-id="e6ba4-137">A tabela a seguir mostra os valores válidos para os tipos de botão de região.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-137">The following table shows the values that are valid for region button types.</span></span> <span data-ttu-id="e6ba4-138">Não é necessário definir valores para tipos que você não usará em sua capa.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-138">You do not need to define values for types you will not be using in your skin.</span></span>



| <span data-ttu-id="e6ba4-139">Valor</span><span class="sxs-lookup"><span data-stu-id="e6ba4-139">Value</span></span>     | <span data-ttu-id="e6ba4-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6ba4-140">Description</span></span>                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ba4-141">PushHit</span><span class="sxs-lookup"><span data-stu-id="e6ba4-141">PushHit</span></span>   | <span data-ttu-id="e6ba4-142">Semelhante ao valor do botão de ação, exceto que a área de pressionamento do botão é definida pelo valor de cor na imagem da região.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-142">Similar to the Push button value except that the hit area of the button is defined by the color value in the Region image.</span></span>   |
| <span data-ttu-id="e6ba4-143">ToggleHit</span><span class="sxs-lookup"><span data-stu-id="e6ba4-143">ToggleHit</span></span> | <span data-ttu-id="e6ba4-144">Semelhante ao valor do botão de alternância, exceto que a área de pressionamento do botão é definida pelo valor de cor na imagem da região.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-144">Similar to the Toggle button value except that the hit area of the button is defined by the color value in the Region image.</span></span> |
| <span data-ttu-id="e6ba4-145">2PushHit</span><span class="sxs-lookup"><span data-stu-id="e6ba4-145">2PushHit</span></span>  | <span data-ttu-id="e6ba4-146">Semelhante ao valor do botão 2Push, exceto que a área de pressionamento do botão é definida pelo valor de cor na imagem da região.</span><span class="sxs-lookup"><span data-stu-id="e6ba4-146">Similar to the 2Push button value except that the hit area of the button is defined by the color value in the Region image.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="e6ba4-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6ba4-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6ba4-148">**Botões**</span><span class="sxs-lookup"><span data-stu-id="e6ba4-148">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




