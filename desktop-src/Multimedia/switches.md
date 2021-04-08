---
title: Comutadores
description: Comutadores
ms.assetid: ab92d30d-97ab-4229-aed8-1080b6e6dc88
keywords:
- mixers de áudio, controles
- mixers de áudio, comutadores
- mixers, controles
- mixers, comutadores
- alternar controles
- Estrutura de MIXERCONTROLDETAILS_BOOLEAN
- Controle booliano
- controle de botão
- controle ativar/desativar
- controle mono
- controle de intensidade
- controle avançado de estéreo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d65bb2a14a0e7dc527fab0e628035839855934
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823706"
---
# <a name="switches"></a><span data-ttu-id="741fd-115">Comutadores</span><span class="sxs-lookup"><span data-stu-id="741fd-115">Switches</span></span>

<span data-ttu-id="741fd-116">Os controles switch são opções de dois Estados.</span><span class="sxs-lookup"><span data-stu-id="741fd-116">The switch controls are two-state switches.</span></span> <span data-ttu-id="741fd-117">Esses controles usam a [**estrutura \_ booliana MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) para recuperar e definir propriedades de controle.</span><span class="sxs-lookup"><span data-stu-id="741fd-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="741fd-118">A tabela a seguir descreve os tipos de comutadores.</span><span class="sxs-lookup"><span data-stu-id="741fd-118">The following table describes the types of switches.</span></span>



| <span data-ttu-id="741fd-119">Control</span><span class="sxs-lookup"><span data-stu-id="741fd-119">Control</span></span>         | <span data-ttu-id="741fd-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="741fd-120">Description</span></span>                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="741fd-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="741fd-121">Boolean</span></span>         | <span data-ttu-id="741fd-122">A opção genérica.</span><span class="sxs-lookup"><span data-stu-id="741fd-122">The generic switch.</span></span> <span data-ttu-id="741fd-123">Ele pode ser definido como **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="741fd-123">It can be set to **TRUE** or **FALSE**.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="741fd-124">Botão</span><span class="sxs-lookup"><span data-stu-id="741fd-124">Button</span></span>          | <span data-ttu-id="741fd-125">Defina como **verdadeiro** para todos os botões que o driver deve manipular, como se eles tivessem sido pressionados.</span><span class="sxs-lookup"><span data-stu-id="741fd-125">Set to **TRUE** for all buttons that the driver should handle as though they had been pressed.</span></span> <span data-ttu-id="741fd-126">Se o valor for **false**, nenhuma ação será executada.</span><span class="sxs-lookup"><span data-stu-id="741fd-126">If the value is **FALSE**, no action is taken.</span></span>                                                                                         |
| <span data-ttu-id="741fd-127">Ativar/desativar</span><span class="sxs-lookup"><span data-stu-id="741fd-127">On/Off</span></span>          | <span data-ttu-id="741fd-128">Um comutador alternativo que é representado por um gráfico diferente daquele usado para a opção booliana.</span><span class="sxs-lookup"><span data-stu-id="741fd-128">An alternative switch that is represented by a graphic other than the one used for the Boolean switch.</span></span> <span data-ttu-id="741fd-129">Ele pode ser definido como ON ou OFF.</span><span class="sxs-lookup"><span data-stu-id="741fd-129">It can be set to ON or OFF.</span></span>                                                                                                    |
| <span data-ttu-id="741fd-130">Mute</span><span class="sxs-lookup"><span data-stu-id="741fd-130">Mute</span></span>            | <span data-ttu-id="741fd-131">Silencia uma linha de áudio (suprimindo o fluxo de dados da linha) ou permite que os dados de áudio sejam reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="741fd-131">Mutes an audio line (suppressing the data flow of the line) or allows the audio data to play.</span></span> <span data-ttu-id="741fd-132">Essa opção é usada frequentemente para ajudar a controlar as linhas que alimentam o mixer.</span><span class="sxs-lookup"><span data-stu-id="741fd-132">This switch is frequently used to help control the lines feeding into the mixer.</span></span>                                                        |
| <span data-ttu-id="741fd-133">Mono</span><span class="sxs-lookup"><span data-stu-id="741fd-133">Mono</span></span>            | <span data-ttu-id="741fd-134">Alterna entre a saída mono e estéreo para uma linha de áudio estéreo.</span><span class="sxs-lookup"><span data-stu-id="741fd-134">Switches between mono and stereo output for a stereo audio line.</span></span> <span data-ttu-id="741fd-135">Defina como desativado para reproduzir dados estéreo como canais separados.</span><span class="sxs-lookup"><span data-stu-id="741fd-135">Set to OFF to play stereo data as separate channels.</span></span> <span data-ttu-id="741fd-136">Defina como ON para combinar dados de ambos os canais em uma linha de áudio mono.</span><span class="sxs-lookup"><span data-stu-id="741fd-136">Set to ON to combine data from both channels into a mono audio line.</span></span>                                            |
| <span data-ttu-id="741fd-137">Intensidade</span><span class="sxs-lookup"><span data-stu-id="741fd-137">Loudness</span></span>        | <span data-ttu-id="741fd-138">Aumenta baixo volume baixo para uma linha de áudio.</span><span class="sxs-lookup"><span data-stu-id="741fd-138">Boosts low-volume bass for an audio line.</span></span> <span data-ttu-id="741fd-139">Defina como ativado para impulsionar baixo volume baixo.</span><span class="sxs-lookup"><span data-stu-id="741fd-139">Set to ON to boost low-volume bass.</span></span> <span data-ttu-id="741fd-140">Defina como desativado para definir os níveis de volume como normal.</span><span class="sxs-lookup"><span data-stu-id="741fd-140">Set to OFF to set volume levels to normal.</span></span> <span data-ttu-id="741fd-141">A quantidade de aumento é específica de hardware.</span><span class="sxs-lookup"><span data-stu-id="741fd-141">The amount of boost is hardware specific.</span></span> <span data-ttu-id="741fd-142">Para obter mais informações, consulte a documentação do seu dispositivo MIXER.</span><span class="sxs-lookup"><span data-stu-id="741fd-142">For more information, see the documentation for your mixer device.</span></span> |
| <span data-ttu-id="741fd-143">Estéreo avançado</span><span class="sxs-lookup"><span data-stu-id="741fd-143">Stereo Enhanced</span></span> | <span data-ttu-id="741fd-144">Aumenta a separação de estéreo.</span><span class="sxs-lookup"><span data-stu-id="741fd-144">Increases stereo separation.</span></span> <span data-ttu-id="741fd-145">Defina como ativado para aumentar a separação de estéreo.</span><span class="sxs-lookup"><span data-stu-id="741fd-145">Set to ON to increase stereo separation.</span></span> <span data-ttu-id="741fd-146">Defina como desativado para nenhum aprimoramento.</span><span class="sxs-lookup"><span data-stu-id="741fd-146">Set to OFF for no enhancement.</span></span>                                                                                                                                  |



 

 

 