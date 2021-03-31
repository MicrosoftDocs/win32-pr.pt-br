---
title: Erros do Sequencer
description: Erros do Sequencer
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- Valores de retorno de MCIERR, erros de sequenciador
- referência de multimídia, erros do Sequencer
- referência para multimídia, erros do Sequencer
- MCI (interface de controle de mídia), erros do Sequencer
- MCI (interface de controle de mídia), erros do Sequencer
- referência para MCI, erros do Sequencer
- Referência MCI, erros do Sequencer
- MCI (interface de controle de mídia), erros
- MCI (interface de controle de mídia), erros
- referência para MCI, erros
- Referência de MCI, erros
- erros do Sequencer
- Erros do sequenciador MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd7d55d3b49be3d641f7396148d98766b224a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635882"
---
# <a name="sequencer-errors"></a><span data-ttu-id="6fe74-116">Erros do Sequencer</span><span class="sxs-lookup"><span data-stu-id="6fe74-116">Sequencer Errors</span></span>

<span data-ttu-id="6fe74-117">Os seguintes valores de retorno adicionais são definidos para sequenciais MCI:</span><span class="sxs-lookup"><span data-stu-id="6fe74-117">The following additional return values are defined for MCI sequencers:</span></span>



| <span data-ttu-id="6fe74-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6fe74-118">Value</span></span>                          | <span data-ttu-id="6fe74-119">Significado</span><span class="sxs-lookup"><span data-stu-id="6fe74-119">Meaning</span></span>                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe74-120">\_div Seq \_ MCIERR \_ incompatível</span><span class="sxs-lookup"><span data-stu-id="6fe74-120">MCIERR\_SEQ\_DIV\_INCOMPATIBLE</span></span> | <span data-ttu-id="6fe74-121">Os formatos de hora do "ponteiro de música" e SMPTE são singulares.</span><span class="sxs-lookup"><span data-stu-id="6fe74-121">The time formats of the "song pointer" and SMPTE are singular.</span></span> <span data-ttu-id="6fe74-122">Você não pode usá-los juntos.</span><span class="sxs-lookup"><span data-stu-id="6fe74-122">You can't use them together.</span></span>                                                              |
| <span data-ttu-id="6fe74-123">MCIERR \_ Seq \_ NOMIDIPRESENT</span><span class="sxs-lookup"><span data-stu-id="6fe74-123">MCIERR\_SEQ\_NOMIDIPRESENT</span></span>     | <span data-ttu-id="6fe74-124">Este sistema não tem dispositivos MIDI instalados.</span><span class="sxs-lookup"><span data-stu-id="6fe74-124">This system has no installed MIDI devices.</span></span> <span data-ttu-id="6fe74-125">Use a opção drivers do painel de controle para instalar um driver de MIDI.</span><span class="sxs-lookup"><span data-stu-id="6fe74-125">Use the Drivers option from the Control Panel to install a MIDI driver.</span></span>                                       |
| <span data-ttu-id="6fe74-126">\_porta MCIERR \_ Seq \_ INUSE</span><span class="sxs-lookup"><span data-stu-id="6fe74-126">MCIERR\_SEQ\_PORT\_INUSE</span></span>       | <span data-ttu-id="6fe74-127">A porta MIDI especificada já está em uso.</span><span class="sxs-lookup"><span data-stu-id="6fe74-127">The specified MIDI port is already in use.</span></span> <span data-ttu-id="6fe74-128">Aguarde até que seja gratuito; em seguida, tente novamente.</span><span class="sxs-lookup"><span data-stu-id="6fe74-128">Wait until it is free; then, try again.</span></span>                                                                       |
| <span data-ttu-id="6fe74-129">MCIERR \_ Seq \_ porta \_ MAPNODEVICE</span><span class="sxs-lookup"><span data-stu-id="6fe74-129">MCIERR\_SEQ\_PORT\_MAPNODEVICE</span></span> | <span data-ttu-id="6fe74-130">A instalação atual do mapeador de MIDI se refere a um dispositivo MIDI que não está instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="6fe74-130">The current MIDI Mapper setup refers to a MIDI device that is not installed on the system.</span></span> <span data-ttu-id="6fe74-131">Use o mapeador de MIDI no painel de controle para editar a configuração.</span><span class="sxs-lookup"><span data-stu-id="6fe74-131">Use the MIDI Mapper from the Control Panel to edit the setup.</span></span> |
| <span data-ttu-id="6fe74-132">MCIERR \_ Seq \_ porta \_ MISCERROR</span><span class="sxs-lookup"><span data-stu-id="6fe74-132">MCIERR\_SEQ\_PORT\_MISCERROR</span></span>   | <span data-ttu-id="6fe74-133">Ocorreu um erro com a porta especificada.</span><span class="sxs-lookup"><span data-stu-id="6fe74-133">An error occurred with specified port.</span></span>                                                                                                                   |
| <span data-ttu-id="6fe74-134">\_porta MCIERR \_ Seq \_ inexistente</span><span class="sxs-lookup"><span data-stu-id="6fe74-134">MCIERR\_SEQ\_PORT\_NONEXISTENT</span></span> | <span data-ttu-id="6fe74-135">O dispositivo MIDI especificado não está instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="6fe74-135">The specified MIDI device is not installed on the system.</span></span> <span data-ttu-id="6fe74-136">Use a opção drivers do painel de controle para instalar um dispositivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="6fe74-136">Use the Drivers option from the Control Panel to install a MIDI device.</span></span>                        |
| <span data-ttu-id="6fe74-137">MCIERR \_ Seq \_ PORTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="6fe74-137">MCIERR\_SEQ\_PORTUNSPECIFIED</span></span>   | <span data-ttu-id="6fe74-138">O sistema não tem uma porta MIDI atual especificada.</span><span class="sxs-lookup"><span data-stu-id="6fe74-138">The system does not have a current MIDI port specified.</span></span>                                                                                                  |
| <span data-ttu-id="6fe74-139">\_ \_ temporizador MCIERR Seq</span><span class="sxs-lookup"><span data-stu-id="6fe74-139">MCIERR\_SEQ\_TIMER</span></span>             | <span data-ttu-id="6fe74-140">Todos os timers de multimídia estão sendo usados por outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6fe74-140">All multimedia timers are being used by other applications.</span></span> <span data-ttu-id="6fe74-141">Encerre um desses aplicativos; em seguida, tente novamente.</span><span class="sxs-lookup"><span data-stu-id="6fe74-141">Quit one of these applications; then, try again.</span></span>                                             |



 

 

 




