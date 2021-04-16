---
title: Alterando a sincronização do Sequencer
description: Alterando a sincronização do Sequencer
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET mensagem de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bffdc1606624f63fa05a9cc03c68fe64781620f
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/12/2021
ms.locfileid: "105750210"
---
# <a name="changing-sequencer-synchronization"></a><span data-ttu-id="a9250-104">Alterando a sincronização do Sequencer</span><span class="sxs-lookup"><span data-stu-id="a9250-104">Changing Sequencer Synchronization</span></span>

> [!NOTE]
> <span data-ttu-id="a9250-105">Comunicação sem tendência a Microsoft dá suporte a um ambiente diversificado e de inclusão.</span><span class="sxs-lookup"><span data-stu-id="a9250-105">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="a9250-106">Neste documento, há referências à palavra ' escravo '.</span><span class="sxs-lookup"><span data-stu-id="a9250-106">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="a9250-107">O [Guia de estilo da Microsoft para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconhece isso como uma palavra de exclusão.</span><span class="sxs-lookup"><span data-stu-id="a9250-107">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="a9250-108">Essa palavra-chave é usada, pois é atualmente a palavra usada no software.</span><span class="sxs-lookup"><span data-stu-id="a9250-108">This wording is used as it is currently the wording used within the software.</span></span> <span data-ttu-id="a9250-109">Para fins de consistência, este documento contém esta palavra.</span><span class="sxs-lookup"><span data-stu-id="a9250-109">For consistency, this document contains this word.</span></span> <span data-ttu-id="a9250-110">Quando esta palavra for removida do software, corrigiremos este documento para estar em alinhamento.</span><span class="sxs-lookup"><span data-stu-id="a9250-110">When this word is removed from the software, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="a9250-111">Para alterar o modo de sincronização de um dispositivo de sequenciador, use a mensagem de comando do [**MCI \_ set**](mci-set.md) com os \_ \_ \_ sinalizadores subordinados do MCI Set Master e MCI \_ \_ set \_ slave.</span><span class="sxs-lookup"><span data-stu-id="a9250-111">To change the synchronization mode of a sequencer device, use the [**MCI\_SET**](mci-set.md) command message with the MCI\_SEQ\_SET\_MASTER and MCI\_SEQ\_SET\_SLAVE flags.</span></span> <span data-ttu-id="a9250-112">Dois membros na estrutura [**MCI \_ \_ set \_ parms**](mci-seq-set-parms.md) , **dwMaster** e **dwSlave**, são usados para especificar os modos de sincronização mestre e subordinado.</span><span class="sxs-lookup"><span data-stu-id="a9250-112">Two members in the [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure, **dwMaster** and **dwSlave**, are used to specify the master and subordinate synchronization modes.</span></span>

<span data-ttu-id="a9250-113">O modo de sincronização mestre controla as informações de sincronização enviadas pelo Sequencer para uma porta de saída.</span><span class="sxs-lookup"><span data-stu-id="a9250-113">The master synchronization mode controls synchronization information sent by the sequencer to an output port.</span></span> <span data-ttu-id="a9250-114">A seguir estão as constantes para o membro **dwMaster** e seus modos de sincronização mestre correspondentes.</span><span class="sxs-lookup"><span data-stu-id="a9250-114">Following are the constants for the **dwMaster** member and their corresponding master synchronization modes.</span></span>



| <span data-ttu-id="a9250-115">Constante</span><span class="sxs-lookup"><span data-stu-id="a9250-115">Constant</span></span>        | <span data-ttu-id="a9250-116">Modo de sincronização</span><span class="sxs-lookup"><span data-stu-id="a9250-116">Synchronization mode</span></span>                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9250-117">MCI \_ Seq \_ Midi</span><span class="sxs-lookup"><span data-stu-id="a9250-117">MCI\_SEQ\_MIDI</span></span>  | <span data-ttu-id="a9250-118">Sincronização de MIDI.</span><span class="sxs-lookup"><span data-stu-id="a9250-118">MIDI Synchronization.</span></span> <span data-ttu-id="a9250-119">Envie informações de tempo para a porta de saída usando mensagens de relógio de temporização de MIDI.</span><span class="sxs-lookup"><span data-stu-id="a9250-119">Send timing information to output port using MIDI timing clock messages.</span></span>   |
| <span data-ttu-id="a9250-120">MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="a9250-120">MCI\_SEQ\_SMPTE</span></span> | <span data-ttu-id="a9250-121">Sincronização de SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a9250-121">SMPTE Synchronization.</span></span> <span data-ttu-id="a9250-122">Envie informações de tempo para a porta de saída usando mensagens de quadro do trimestre MIDI.</span><span class="sxs-lookup"><span data-stu-id="a9250-122">Send timing information to output port using MIDI quarter-frame messages.</span></span> |
| <span data-ttu-id="a9250-123">\_Seq MCI \_ None</span><span class="sxs-lookup"><span data-stu-id="a9250-123">MCI\_SEQ\_NONE</span></span>  | <span data-ttu-id="a9250-124">Sem sincronização.</span><span class="sxs-lookup"><span data-stu-id="a9250-124">No Synchronization.</span></span> <span data-ttu-id="a9250-125">Não enviar informações de tempo.</span><span class="sxs-lookup"><span data-stu-id="a9250-125">Send no timing information.</span></span>                                                  |



 

<span data-ttu-id="a9250-126">O modo de sincronização subordinada controla onde o Sequencer obtém suas informações de tempo para reproduzir um arquivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="a9250-126">The subordinate synchronization mode controls where the sequencer gets its timing information to play a MIDI file.</span></span> <span data-ttu-id="a9250-127">A seguir estão as constantes para o membro **dwSlave** e seus modos de sincronização subordinada correspondentes.</span><span class="sxs-lookup"><span data-stu-id="a9250-127">Following are the constants for the **dwSlave** member and their corresponding subordinate synchronization modes.</span></span>



| <span data-ttu-id="a9250-128">Constante</span><span class="sxs-lookup"><span data-stu-id="a9250-128">Constant</span></span>        | <span data-ttu-id="a9250-129">Modo de sincronização</span><span class="sxs-lookup"><span data-stu-id="a9250-129">Synchronization mode</span></span>                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9250-130">\_arquivo Seq \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a9250-130">MCI\_SEQ\_FILE</span></span>  | <span data-ttu-id="a9250-131">Sincronização de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a9250-131">File Synchronization.</span></span> <span data-ttu-id="a9250-132">Obter informações de tempo do arquivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="a9250-132">Get timing information from MIDI file.</span></span>                                                                                       |
| <span data-ttu-id="a9250-133">MCI \_ Seq \_ Midi</span><span class="sxs-lookup"><span data-stu-id="a9250-133">MCI\_SEQ\_MIDI</span></span>  | <span data-ttu-id="a9250-134">Sincronização de MIDI.</span><span class="sxs-lookup"><span data-stu-id="a9250-134">MIDI Synchronization.</span></span> <span data-ttu-id="a9250-135">Obtenha informações de tempo da porta de entrada usando mensagens de relógio de tempo de MIDI.</span><span class="sxs-lookup"><span data-stu-id="a9250-135">Get timing information from input port using MIDI timing clock messages.</span></span>                                                     |
| <span data-ttu-id="a9250-136">MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="a9250-136">MCI\_SEQ\_SMPTE</span></span> | <span data-ttu-id="a9250-137">Sincronização de SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a9250-137">SMPTE Synchronization.</span></span> <span data-ttu-id="a9250-138">Obtenha informações de tempo da porta de entrada usando mensagens de quadro do trimestre MIDI.</span><span class="sxs-lookup"><span data-stu-id="a9250-138">Get timing information from input port using MIDI quarter-frame messages.</span></span>                                                   |
| <span data-ttu-id="a9250-139">\_Seq MCI \_ None</span><span class="sxs-lookup"><span data-stu-id="a9250-139">MCI\_SEQ\_NONE</span></span>  | <span data-ttu-id="a9250-140">Sem sincronização.</span><span class="sxs-lookup"><span data-stu-id="a9250-140">No Synchronization.</span></span> <span data-ttu-id="a9250-141">Obtenha informações de tempo somente de comandos MCI e ignore informações de tempo (como alterações de tempo) que estão no arquivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="a9250-141">Get timing information from MCI commands only and ignore timing information (such as tempo changes) that are in the MIDI file.</span></span> |



 

> [!Note]  
> <span data-ttu-id="a9250-142">Atualmente, para a sincronização mestre, o sequenciador MIDI MCI só dá suporte ao modo sem sincronização (MCI \_ Seq \_ nenhum).</span><span class="sxs-lookup"><span data-stu-id="a9250-142">Currently, for master synchronization, the MCI MIDI sequencer supports only the No Synchronization mode (MCI\_SEQ\_NONE).</span></span> <span data-ttu-id="a9250-143">Para a sincronização subordinada, ele dá suporte apenas ao modo de sincronização de arquivo ( \_ arquivo MCI Seq \_ ) e ao modo sem sincronização (MCI \_ Seq \_ nenhum).</span><span class="sxs-lookup"><span data-stu-id="a9250-143">For subordinate synchronization, it supports only the File Synchronization mode (MCI\_SEQ\_FILE) and the No Synchronization mode (MCI\_SEQ\_NONE).</span></span>

 

 

 




