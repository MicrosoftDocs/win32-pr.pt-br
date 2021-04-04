---
title: Mapeando dispositivos Waveform-Audio
description: Mapeando dispositivos Waveform-Audio
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- áudio de multimídia, mapeamento de formato de onda-dispositivos de áudio
- áudio, mapeamento de formato de onda-dispositivos de áudio
- Gerenciador de compactação de áudio (ACM), mapeamento de formato de onda-dispositivos de áudio
- ACM (Gerenciador de compactação de áudio), mapeamento de formato de onda-dispositivos de áudio
- mapeando a onda-dispositivos de áudio
- áudio de multimídia, mapeador
- áudio, mapeador
- Gerenciador de compactação de áudio (ACM), mapeador
- ACM (Gerenciador de compactação de áudio), mapeador
- mapper
- áudio de onda, dispositivos de mapeamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cdd269e21eb992244dd0e5979c7e0d193ba92b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822491"
---
# <a name="mapping-waveform-audio-devices"></a><span data-ttu-id="2ca71-114">Mapeando dispositivos Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="2ca71-114">Mapping Waveform-Audio Devices</span></span>

<span data-ttu-id="2ca71-115">O Windows fornece um conjunto de funções padrão para dispositivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="2ca71-115">Windows provides a set of standard functions for audio devices.</span></span> <span data-ttu-id="2ca71-116">Essas funções emitem chamadas para drivers de dispositivo que gerenciam dispositivos de hardware.</span><span class="sxs-lookup"><span data-stu-id="2ca71-116">These functions issue calls to device drivers that manage hardware devices.</span></span> <span data-ttu-id="2ca71-117">O sistema usa um módulo chamado "mapeador" para gerenciar os dispositivos instalados.</span><span class="sxs-lookup"><span data-stu-id="2ca71-117">The system uses a module called a "mapper" to manage installed devices.</span></span> <span data-ttu-id="2ca71-118">O mapeador usa ganchos especiais na interface do driver para interceptar chamadas e agir como um intermediário entre o sistema e os drivers instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="2ca71-118">The mapper uses special hooks in the driver interface to intercept calls and to act as an intermediary between the system and the drivers installed in the system.</span></span> <span data-ttu-id="2ca71-119">O mapeador é responsável por corresponder as solicitações de um aplicativo para acesso a um dispositivo com os dispositivos disponíveis e para localizar um dispositivo que atenda aos requisitos de áudio do aplicativo atual.</span><span class="sxs-lookup"><span data-stu-id="2ca71-119">The mapper is responsible for matching an application's requests for access to a device with the available devices and for finding a device that meets the current application's audio requirements.</span></span> <span data-ttu-id="2ca71-120">O sistema fornece Mapeadores para tipos de driver padrão: wave-áudio, MIDI (interface digital de instrumentos musicais) e dispositivos auxiliares.</span><span class="sxs-lookup"><span data-stu-id="2ca71-120">The system provides mappers for standard driver types: waveform-audio, MIDI (Musical Instrument Digital Interface), and auxiliary devices.</span></span>

<span data-ttu-id="2ca71-121">O ACM é uma extensão do sistema de multimídia básico e é instalado como um mapeador.</span><span class="sxs-lookup"><span data-stu-id="2ca71-121">The ACM is an extension of the basic multimedia system and is installed as a mapper.</span></span> <span data-ttu-id="2ca71-122">Isso significa que o ACM usa os ganchos do mapeador de interface de driver para dispositivos de forma de onda-áudio.</span><span class="sxs-lookup"><span data-stu-id="2ca71-122">This means the ACM uses the driver-interface mapper hooks for waveform-audio devices.</span></span> <span data-ttu-id="2ca71-123">O uso desses ganchos permite que o ACM decodifique ou codifique dados de wave-áudio antes de passá-los para ou de um driver de dispositivo de forma de onda-áudio.</span><span class="sxs-lookup"><span data-stu-id="2ca71-123">Using these hooks allows the ACM to decode or encode waveform-audio data before passing it to or from a waveform-audio device driver.</span></span> <span data-ttu-id="2ca71-124">A diferença entre o ACM e o mapeador de sistema padrão é que o ACM pode pesquisar um dispositivo de wave-áudio que dá suporte a um formato especificado ou encontrar uma combinação de um dispositivo de wave-áudio e um compressor ou descompactador ACM que dá suporte a um formato especificado.</span><span class="sxs-lookup"><span data-stu-id="2ca71-124">The difference between the ACM and the standard system mapper is that the ACM can search for a waveform-audio device that supports a specified format or find a combination of a waveform-audio device and an ACM compressor or decompressor that supports a specified format.</span></span>

<span data-ttu-id="2ca71-125">Quando um aplicativo solicita que o sistema abra um dispositivo de forma de onda-áudio para entrada ou saída, a solicitação especifica o formato e o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2ca71-125">When an application requests that the system open a waveform-audio device for input or output, the request specifies the format and device.</span></span> <span data-ttu-id="2ca71-126">Quando o dispositivo especificado é o mapeador, o mapeador deve localizar um dispositivo que ofereça suporte ao formato especificado.</span><span class="sxs-lookup"><span data-stu-id="2ca71-126">When the specified device is the mapper, the mapper must find a device that supports the specified format.</span></span> <span data-ttu-id="2ca71-127">O mapeador implementado no ACM pesquisa um dispositivo de wave-áudio instalado que dá suporte ao formato especificado.</span><span class="sxs-lookup"><span data-stu-id="2ca71-127">The mapper implemented in the ACM searches for an installed waveform-audio device that supports the specified format.</span></span> <span data-ttu-id="2ca71-128">Se o ACM não puder encontrar esse dispositivo, ele pesquisará um dispositivo de wave-áudio e um compressor ou descompactador que juntos dão suporte ao formato.</span><span class="sxs-lookup"><span data-stu-id="2ca71-128">If the ACM cannot find such a device, it searches for a waveform-audio device and a compressor or decompressor that together support the format.</span></span> <span data-ttu-id="2ca71-129">Especificamente, o ACM procura um compressor ou descompactador que converte o formato especificado em um formato com suporte de um dispositivo de wave-áudio instalado.</span><span class="sxs-lookup"><span data-stu-id="2ca71-129">Specifically, the ACM searches for a compressor or decompressor that converts the specified format into a format that is supported by an installed waveform-audio device.</span></span> <span data-ttu-id="2ca71-130">Depois que o ACM encontra um dispositivo que dá suporte ao formato convertido, ele pode honrar solicitações para reproduzir ou registrar o formato solicitado originalmente, mesmo que nenhum dispositivo de Wave de som instalado ofereça suporte diretamente a esse formato.</span><span class="sxs-lookup"><span data-stu-id="2ca71-130">After the ACM finds a device that supports the converted format, it can honor requests to play or record the format originally requested, even though no installed waveform-audio device directly supports that format.</span></span>

<span data-ttu-id="2ca71-131">Além da conversão de formato, o ACM também oferece serviços para dar suporte à compactação, descompactação, filtragem, seleção de formato e seleção de filtro.</span><span class="sxs-lookup"><span data-stu-id="2ca71-131">In addition to format conversion, the ACM also offers services to support compression, decompression, filtering, format selection, and filter selection.</span></span> <span data-ttu-id="2ca71-132">Ele fornece uma API padrão que ele suporta chamando seus próprios drivers.</span><span class="sxs-lookup"><span data-stu-id="2ca71-132">It provides a standard API that it supports by calling its own drivers.</span></span>

 

 




