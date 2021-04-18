---
title: Consultando dispositivos de entrada MIDI
description: Consultando dispositivos de entrada MIDI
ms.assetid: 2da88418-f9cf-49da-b17f-8a26d357b5ab
keywords:
- MIDI (interface digital de instrumento musical), dispositivos de entrada
- MIDI (interface digital de instrumentos musicais), dispositivos de entrada
- gravando áudio MIDI, dispositivos de entrada
- Dispositivos de entrada MIDI
- MIDI (interface digital de instrumento musical), consultando dispositivos de entrada
- MIDI (interface digital de instrumentos musicais), consultando dispositivos de entrada
- gravando áudio MIDI, consultando dispositivos de entrada
- consultando dispositivos de entrada MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a92bec8733887e20c25f37d1de3dd493e555c8a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105758949"
---
# <a name="querying-midi-input-devices"></a><span data-ttu-id="244be-111">Consultando dispositivos de entrada MIDI</span><span class="sxs-lookup"><span data-stu-id="244be-111">Querying MIDI Input Devices</span></span>

<span data-ttu-id="244be-112">Antes de gravar áudio MIDI, você deve usar a função [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) para determinar os recursos do dispositivo de entrada MIDI que está presente no sistema.</span><span class="sxs-lookup"><span data-stu-id="244be-112">Before recording MIDI audio, you should use the [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) function to determine the capabilities of the MIDI input device that is present in the system.</span></span> <span data-ttu-id="244be-113">Essa função usa um endereço de uma estrutura [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) , que preenche as informações sobre os recursos do determinado dispositivo.</span><span class="sxs-lookup"><span data-stu-id="244be-113">This function takes an address of a [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) structure, which it fills with information about the capabilities of the given device.</span></span> <span data-ttu-id="244be-114">Essas informações incluem os identificadores de fabricante e produto, um nome de produto para o dispositivo e o número de versão do driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="244be-114">This information includes the manufacturer and product identifiers, a product name for the device, and the version number of the device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="244be-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="244be-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="244be-116">Gravando áudio MIDI</span><span class="sxs-lookup"><span data-stu-id="244be-116">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 