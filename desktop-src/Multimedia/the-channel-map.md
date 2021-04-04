---
title: O mapa do canal
description: O mapa do canal
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- MIDI (interface digital de instrumento musical), mapeador de MIDI
- MIDI (interface digital de instrumentos musicais), mapeador de MIDI
- Mapeador de MIDI, mapa de canal
- mapa de canal
- Mapeador de MIDI, mensagens de canal
- Mensagens do canal MIDI
- mensagens do canal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87027c74ebddea9b51545d15bfa90e52dee95a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084098"
---
# <a name="the-channel-map"></a><span data-ttu-id="eb192-110">O mapa do canal</span><span class="sxs-lookup"><span data-stu-id="eb192-110">The Channel Map</span></span>

<span data-ttu-id="eb192-111">O mapa de canal afeta todas as mensagens de canal MIDI.</span><span class="sxs-lookup"><span data-stu-id="eb192-111">The channel map affects all MIDI channel messages.</span></span> <span data-ttu-id="eb192-112">As mensagens do canal MIDI incluem observação-em, nota-aftertouch, chave de telefonia, controle de alterações de programa, alteração de programas, canal-AfterTouch e mensagens de alteração de curvatura de densidade.</span><span class="sxs-lookup"><span data-stu-id="eb192-112">MIDI channel messages include note-on, note-off, polyphonic-key-aftertouch, control-change, program-change, channel-aftertouch, and pitch-bend-change messages.</span></span> <span data-ttu-id="eb192-113">O mapeador de MIDI usa um único mapa de canal com uma entrada para cada um dos 16 canais MIDI.</span><span class="sxs-lookup"><span data-stu-id="eb192-113">The MIDI Mapper uses a single channel map with an entry for each of the 16 MIDI channels.</span></span> <span data-ttu-id="eb192-114">Cada entrada de mapa de canal especifica o seguinte:</span><span class="sxs-lookup"><span data-stu-id="eb192-114">Each channel-map entry specifies the following:</span></span>

-   <span data-ttu-id="eb192-115">Um canal de destino para a mensagem MIDI</span><span class="sxs-lookup"><span data-stu-id="eb192-115">A destination channel for the MIDI message</span></span>
-   <span data-ttu-id="eb192-116">Um dispositivo de saída de destino para a mensagem MIDI</span><span class="sxs-lookup"><span data-stu-id="eb192-116">A destination output device for the MIDI message</span></span>
-   <span data-ttu-id="eb192-117">Um mapa de patch opcional especificando outras possíveis modificações para a mensagem MIDI</span><span class="sxs-lookup"><span data-stu-id="eb192-117">An optional patch map specifying other possible modifications for the MIDI message</span></span>

<span data-ttu-id="eb192-118">O canal de destino é definido como um dos 16 canais MIDI.</span><span class="sxs-lookup"><span data-stu-id="eb192-118">The destination channel is set to one of the 16 MIDI channels.</span></span> <span data-ttu-id="eb192-119">As mensagens MIDI são modificadas para refletir cada nova atribuição de canal.</span><span class="sxs-lookup"><span data-stu-id="eb192-119">MIDI messages are modified to reflect each new channel assignment.</span></span> <span data-ttu-id="eb192-120">Por exemplo, se a entrada canal de destino para MIDI Channel 4 estiver definida como 6, todas as mensagens MIDI enviadas para o canal 4 serão mapeadas para o canal 6, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb192-120">For example, if the destination channel entry for MIDI channel 4 is set to 6, all MIDI messages sent to channel 4 will be mapped to channel 6, as shown in the following illustration.</span></span>

![imagem MIDI mapeada](images/mmap-a05.gif)

<span data-ttu-id="eb192-122">Neste exemplo, o byte de status de MIDI 0x93 é mapeado para 0x95.</span><span class="sxs-lookup"><span data-stu-id="eb192-122">In this example, the MIDI status byte 0x93 is mapped to 0x95.</span></span> <span data-ttu-id="eb192-123">A ordem baixa de um byte de status de MIDI especifica o número do canal.</span><span class="sxs-lookup"><span data-stu-id="eb192-123">The low-order of a MIDI status byte specifies the channel number.</span></span> <span data-ttu-id="eb192-124">Os canais de origem são definidos como ativo ou inativo.</span><span class="sxs-lookup"><span data-stu-id="eb192-124">Source channels are set to either active or inactive.</span></span> <span data-ttu-id="eb192-125">As mensagens enviadas a canais de origem inativos são ignoradas, portanto, um canal inativo está em vigor sem áudio ou desligado.</span><span class="sxs-lookup"><span data-stu-id="eb192-125">Messages sent to inactive source channels are ignored, so an inactive channel is in effect muted or turned off.</span></span>

<span data-ttu-id="eb192-126">O dispositivo de saída de destino é definido como um dos dispositivos de saída MIDI disponíveis.</span><span class="sxs-lookup"><span data-stu-id="eb192-126">The destination output device is set to one of the available MIDI output devices.</span></span> <span data-ttu-id="eb192-127">Um dispositivo de saída de MIDI pode ser um sintetizador interno ou uma porta de saída de MIDI física.</span><span class="sxs-lookup"><span data-stu-id="eb192-127">A MIDI output device can be an internal synthesizer or a physical MIDI output port.</span></span>

<span data-ttu-id="eb192-128">Mensagens do sistema MIDI são mensagens de MIDI (com bytes de status) de 0xF0 a 0xFF.</span><span class="sxs-lookup"><span data-stu-id="eb192-128">MIDI system messages are MIDI messages (with status bytes) from 0xF0 to 0xFF.</span></span> <span data-ttu-id="eb192-129">Não há canal associado às mensagens do sistema MIDI, portanto, eles não podem ser mapeados.</span><span class="sxs-lookup"><span data-stu-id="eb192-129">There is no channel associated with MIDI system messages, so they cannot be mapped.</span></span> <span data-ttu-id="eb192-130">As mensagens do sistema MIDI são enviadas para todos os dispositivos de saída MIDI listados em um mapa de canal.</span><span class="sxs-lookup"><span data-stu-id="eb192-130">MIDI system messages are sent to all MIDI output devices listed in a channel map.</span></span>

 

 




