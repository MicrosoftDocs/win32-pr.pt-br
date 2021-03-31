---
title: Tipos de dispositivo
description: Tipos de dispositivo
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27ed77debb663a1d90e03512832ca83e6e276d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636724"
---
# <a name="device-types"></a><span data-ttu-id="5457b-103">Tipos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5457b-103">Device Types</span></span>

<span data-ttu-id="5457b-104">O MCI reconhece um conjunto básico de *tipos de dispositivo*.</span><span class="sxs-lookup"><span data-stu-id="5457b-104">MCI recognizes a basic set of *device types*.</span></span> <span data-ttu-id="5457b-105">Um tipo de dispositivo é um conjunto de drivers MCI que compartilham um conjunto de comandos comum e são usados para controlar dispositivos multimídia ou arquivos de dados semelhantes.</span><span class="sxs-lookup"><span data-stu-id="5457b-105">A device type is a set of MCI drivers that share a common command set and are used to control similar multimedia devices or data files.</span></span> <span data-ttu-id="5457b-106">Muitos comandos MCI, como [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)), exigem que você especifique um tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5457b-106">Many MCI commands, such as [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)), require you to specify a device type.</span></span>

<span data-ttu-id="5457b-107">A tabela a seguir lista os tipos de dispositivos definidos.</span><span class="sxs-lookup"><span data-stu-id="5457b-107">The following table lists the defined device types.</span></span> <span data-ttu-id="5457b-108">A implementação atual do MCI inclui conjuntos de comandos para um subconjunto desses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5457b-108">The current implementation of MCI includes command sets for a subset of these devices.</span></span>



| <span data-ttu-id="5457b-109">Tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5457b-109">Device type</span></span>      | <span data-ttu-id="5457b-110">Constante</span><span class="sxs-lookup"><span data-stu-id="5457b-110">Constant</span></span>                      | <span data-ttu-id="5457b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5457b-111">Description</span></span>                                      |
|------------------|-------------------------------|--------------------------------------------------|
| <span data-ttu-id="5457b-112">**cdaudio**</span><span class="sxs-lookup"><span data-stu-id="5457b-112">**cdaudio**</span></span>      | <span data-ttu-id="5457b-113">\_áudio MCI DEVTYPE \_ CD \_</span><span class="sxs-lookup"><span data-stu-id="5457b-113">MCI\_DEVTYPE\_CD\_AUDIO</span></span>       | <span data-ttu-id="5457b-114">Player de áudio de CD</span><span class="sxs-lookup"><span data-stu-id="5457b-114">CD audio player</span></span>                                  |
| <span data-ttu-id="5457b-115">**DATs**</span><span class="sxs-lookup"><span data-stu-id="5457b-115">**dat**</span></span>          | <span data-ttu-id="5457b-116">\_dat DEVTYPE \_ MCI</span><span class="sxs-lookup"><span data-stu-id="5457b-116">MCI\_DEVTYPE\_DAT</span></span>             | <span data-ttu-id="5457b-117">Player de fita de áudio digital</span><span class="sxs-lookup"><span data-stu-id="5457b-117">Digital-audio tape player</span></span>                        |
| <span data-ttu-id="5457b-118">**digitalvideo**</span><span class="sxs-lookup"><span data-stu-id="5457b-118">**digitalvideo**</span></span> | <span data-ttu-id="5457b-119">\_ \_ vídeo digital DEVTYPE \_ MCI</span><span class="sxs-lookup"><span data-stu-id="5457b-119">MCI\_DEVTYPE\_DIGITAL\_VIDEO</span></span>  | <span data-ttu-id="5457b-120">Vídeo digital em uma janela (não baseado em GDI)</span><span class="sxs-lookup"><span data-stu-id="5457b-120">Digital video in a window (not GDI-based)</span></span>        |
| <span data-ttu-id="5457b-121">**outros**</span><span class="sxs-lookup"><span data-stu-id="5457b-121">**other**</span></span>        | <span data-ttu-id="5457b-122">\_DEVTYPE MCI \_</span><span class="sxs-lookup"><span data-stu-id="5457b-122">MCI\_DEVTYPE\_OTHER</span></span>           | <span data-ttu-id="5457b-123">Dispositivo MCI indefinido</span><span class="sxs-lookup"><span data-stu-id="5457b-123">Undefined MCI device</span></span>                             |
| <span data-ttu-id="5457b-124">**Overlay**</span><span class="sxs-lookup"><span data-stu-id="5457b-124">**overlay**</span></span>      | <span data-ttu-id="5457b-125">sobreposição de \_ DEVTYPE MCI \_</span><span class="sxs-lookup"><span data-stu-id="5457b-125">MCI\_DEVTYPE\_OVERLAY</span></span>         | <span data-ttu-id="5457b-126">Dispositivo de sobreposição (vídeo analógico em uma janela)</span><span class="sxs-lookup"><span data-stu-id="5457b-126">Overlay device (analog video in a window)</span></span>        |
| <span data-ttu-id="5457b-127">**detector**</span><span class="sxs-lookup"><span data-stu-id="5457b-127">**scanner**</span></span>      | <span data-ttu-id="5457b-128">\_scanner MCI DEVTYPE \_</span><span class="sxs-lookup"><span data-stu-id="5457b-128">MCI\_DEVTYPE\_SCANNER</span></span>         | <span data-ttu-id="5457b-129">Scanner de imagem</span><span class="sxs-lookup"><span data-stu-id="5457b-129">Image scanner</span></span>                                    |
| <span data-ttu-id="5457b-130">**sequenciador**</span><span class="sxs-lookup"><span data-stu-id="5457b-130">**sequencer**</span></span>    | <span data-ttu-id="5457b-131">\_ \_ sequenciador DEVTYPE MCI</span><span class="sxs-lookup"><span data-stu-id="5457b-131">MCI\_DEVTYPE\_SEQUENCER</span></span>       | <span data-ttu-id="5457b-132">Sequenciador MIDI</span><span class="sxs-lookup"><span data-stu-id="5457b-132">MIDI sequencer</span></span>                                   |
| <span data-ttu-id="5457b-133">**videocassete**</span><span class="sxs-lookup"><span data-stu-id="5457b-133">**vcr**</span></span>          | <span data-ttu-id="5457b-134">\_VCR DEVTYPE \_ MCI</span><span class="sxs-lookup"><span data-stu-id="5457b-134">MCI\_DEVTYPE\_VCR</span></span>             | <span data-ttu-id="5457b-135">Gravador ou player de fita de vídeo</span><span class="sxs-lookup"><span data-stu-id="5457b-135">Video-cassette recorder or player</span></span>                |
| <span data-ttu-id="5457b-136">**videodisc**</span><span class="sxs-lookup"><span data-stu-id="5457b-136">**videodisc**</span></span>    | <span data-ttu-id="5457b-137">\_VIDEODISC MCI DEVTYPE \_</span><span class="sxs-lookup"><span data-stu-id="5457b-137">MCI\_DEVTYPE\_VIDEODISC</span></span>       | <span data-ttu-id="5457b-138">VIDEODISC Player</span><span class="sxs-lookup"><span data-stu-id="5457b-138">Videodisc player</span></span>                                 |
| <span data-ttu-id="5457b-139">**waveaudio**</span><span class="sxs-lookup"><span data-stu-id="5457b-139">**waveaudio**</span></span>    | <span data-ttu-id="5457b-140">\_áudio MCI DEVTYPE \_ Wave \_</span><span class="sxs-lookup"><span data-stu-id="5457b-140">MCI\_DEVTYPE\_WAVEFORM\_AUDIO</span></span> | <span data-ttu-id="5457b-141">Dispositivo de áudio que reproduz arquivos de formato de onda digitalizados</span><span class="sxs-lookup"><span data-stu-id="5457b-141">Audio device that plays digitized waveform files</span></span> |



 

<span data-ttu-id="5457b-142">Neste documento, os nomes dos tipos de dispositivo estão em negrito.</span><span class="sxs-lookup"><span data-stu-id="5457b-142">In this document, the names of device types are bold.</span></span> <span data-ttu-id="5457b-143">Nomes de tipo de dispositivo são usados com a interface de cadeia de caracteres de comando.</span><span class="sxs-lookup"><span data-stu-id="5457b-143">Device-type names are used with the command-string interface.</span></span> <span data-ttu-id="5457b-144">As constantes do tipo de dispositivo são usadas com a interface de mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="5457b-144">Device-type constants are used with the command-message interface.</span></span>

 

 




