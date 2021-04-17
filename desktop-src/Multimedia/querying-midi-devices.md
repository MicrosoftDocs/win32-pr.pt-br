---
title: Consultando dispositivos MIDI
description: Consultando dispositivos MIDI
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- MIDI (interface digital de instrumento musical), consulta de dispositivos
- MIDI (interface digital de instrumentos musicais), consultando dispositivos
- Serviços de MIDI, consultando dispositivos
- consultando dispositivos MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066648d6e9ce89e03b26940cb27f3b62b6a03c07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365880"
---
# <a name="querying-midi-devices"></a><span data-ttu-id="9df19-107">Consultando dispositivos MIDI</span><span class="sxs-lookup"><span data-stu-id="9df19-107">Querying MIDI Devices</span></span>

<span data-ttu-id="9df19-108">Antes de reproduzir ou gravar dados MIDI, você deve determinar os recursos do hardware MIDI presentes no sistema.</span><span class="sxs-lookup"><span data-stu-id="9df19-108">Before playing or recording MIDI data, you must determine the capabilities of the MIDI hardware present in the system.</span></span> <span data-ttu-id="9df19-109">A capacidade de MIDI pode variar de um computador multimídia para o outro; os aplicativos não devem fazer suposições sobre o hardware presente em um determinado sistema.</span><span class="sxs-lookup"><span data-stu-id="9df19-109">MIDI capability can vary from one multimedia computer to the next; applications should not make assumptions about the hardware present in a given system.</span></span>

<span data-ttu-id="9df19-110">O Windows fornece as seguintes funções para determinar quantos dispositivos MIDI estão disponíveis para entrada ou saída em um determinado sistema.</span><span class="sxs-lookup"><span data-stu-id="9df19-110">Windows provides the following functions to determine how many MIDI devices are available for input or output in a given system.</span></span>



| <span data-ttu-id="9df19-111">Valor</span><span class="sxs-lookup"><span data-stu-id="9df19-111">Value</span></span>                                          | <span data-ttu-id="9df19-112">Significado</span><span class="sxs-lookup"><span data-stu-id="9df19-112">Meaning</span></span>                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="9df19-113">**midiInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="9df19-113">**midiInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | <span data-ttu-id="9df19-114">Recupera o número de dispositivos de entrada MIDI presentes no sistema.</span><span class="sxs-lookup"><span data-stu-id="9df19-114">Retrieves the number of MIDI input devices present in the system.</span></span>  |
| [<span data-ttu-id="9df19-115">**midiOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="9df19-115">**midiOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | <span data-ttu-id="9df19-116">Recupera o número de dispositivos de saída de MIDI presentes no sistema.</span><span class="sxs-lookup"><span data-stu-id="9df19-116">Retrieves the number of MIDI output devices present in the system.</span></span> |



 

<span data-ttu-id="9df19-117">Assim como outros dispositivos de áudio, os dispositivos MIDI são identificados por um identificador de dispositivo, que é determinado implicitamente do número de dispositivos presentes em um determinado sistema.</span><span class="sxs-lookup"><span data-stu-id="9df19-117">Like other audio devices, MIDI devices are identified by a device identifier, which is determined implicitly from the number of devices present in a given system.</span></span> <span data-ttu-id="9df19-118">Os identificadores de dispositivo variam de zero até o número de dispositivos presentes, menos um.</span><span class="sxs-lookup"><span data-stu-id="9df19-118">Device identifiers range from zero to the number of devices present, minus one.</span></span> <span data-ttu-id="9df19-119">Por exemplo, se houver dois dispositivos de saída MIDI em um sistema, os identificadores de dispositivo válidos serão 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="9df19-119">For example, if there are two MIDI output devices in a system, valid device identifiers are 0 and 1.</span></span>

<span data-ttu-id="9df19-120">Depois de determinar quantos dispositivos de entrada ou saída de MIDI estão presentes em um sistema, você pode consultar os recursos de cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9df19-120">After you determine how many MIDI input or output devices are present in a system, you can inquire about the capabilities of each device.</span></span> <span data-ttu-id="9df19-121">O Windows fornece as seguintes funções para determinar os recursos dos dispositivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="9df19-121">Windows provides the following functions to determine the capabilities of audio devices.</span></span>



| <span data-ttu-id="9df19-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9df19-122">Value</span></span>                                          | <span data-ttu-id="9df19-123">Significado</span><span class="sxs-lookup"><span data-stu-id="9df19-123">Meaning</span></span>                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9df19-124">**midiInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="9df19-124">**midiInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | <span data-ttu-id="9df19-125">Recupera os recursos de um determinado dispositivo de entrada de MIDI e coloca essas informações na estrutura [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) .</span><span class="sxs-lookup"><span data-stu-id="9df19-125">Retrieves the capabilities of a given MIDI input device and places this information in the [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) structure.</span></span>    |
| [<span data-ttu-id="9df19-126">**midiOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="9df19-126">**midiOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | <span data-ttu-id="9df19-127">Recupera os recursos de um determinado dispositivo de saída de MIDI e coloca essas informações na estrutura [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) .</span><span class="sxs-lookup"><span data-stu-id="9df19-127">Retrieves the capabilities of a given MIDI output device and places this information in the [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) structure.</span></span> |



 

<span data-ttu-id="9df19-128">Cada uma dessas funções tem um parâmetro que especifica o endereço de uma estrutura que a função preenche com informações sobre os recursos de um dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="9df19-128">Each of these functions has a parameter specifying the address of a structure that the function fills with information about the capabilities of a specified device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9df19-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9df19-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9df19-130">Serviços MIDI</span><span class="sxs-lookup"><span data-stu-id="9df19-130">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 