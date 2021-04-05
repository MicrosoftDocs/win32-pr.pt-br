---
title: Abrindo e fechando drivers de dispositivo
description: Abrindo e fechando drivers de dispositivo
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- MIDI (interface digital de instrumento musical), abertura de dispositivos
- MIDI (interface digital de instrumentos musicais), abrindo dispositivos
- Serviços de MIDI, abrindo dispositivos
- abrindo dispositivos MIDI
- MIDI (interface digital de instrumento musical), dispositivos de fechamento
- MIDI (interface digital de instrumentos musicais), fechando dispositivos
- Serviços de MIDI, fechando dispositivos
- fechando dispositivos MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d7035455baa067b81af7da980a4ae043500c7b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640544"
---
# <a name="opening-and-closing-device-drivers"></a><span data-ttu-id="989e5-111">Abrindo e fechando drivers de dispositivo</span><span class="sxs-lookup"><span data-stu-id="989e5-111">Opening and Closing Device Drivers</span></span>

<span data-ttu-id="989e5-112">Você deve abrir um dispositivo MIDI antes de usá-lo e fechar o dispositivo assim que terminar de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="989e5-112">You must open a MIDI device before using it, and you should close the device as soon as you finish using it.</span></span> <span data-ttu-id="989e5-113">O Windows fornece as seguintes funções para abrir e fechar diferentes tipos de dispositivos MIDI.</span><span class="sxs-lookup"><span data-stu-id="989e5-113">Windows provides the following functions to open and close different types of MIDI devices.</span></span>



| <span data-ttu-id="989e5-114">Valor</span><span class="sxs-lookup"><span data-stu-id="989e5-114">Value</span></span>                                | <span data-ttu-id="989e5-115">Significado</span><span class="sxs-lookup"><span data-stu-id="989e5-115">Meaning</span></span>                                            |
|--------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="989e5-116">**midiInClose**</span><span class="sxs-lookup"><span data-stu-id="989e5-116">**midiInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | <span data-ttu-id="989e5-117">Fecha um dispositivo de entrada MIDI especificado.</span><span class="sxs-lookup"><span data-stu-id="989e5-117">Closes a specified MIDI input device.</span></span>              |
| [<span data-ttu-id="989e5-118">**midiInOpen**</span><span class="sxs-lookup"><span data-stu-id="989e5-118">**midiInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | <span data-ttu-id="989e5-119">Abre um dispositivo de entrada MIDI especificado para gravação.</span><span class="sxs-lookup"><span data-stu-id="989e5-119">Opens a specified MIDI input device for recording.</span></span> |
| [<span data-ttu-id="989e5-120">**midiOutClose**</span><span class="sxs-lookup"><span data-stu-id="989e5-120">**midiOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | <span data-ttu-id="989e5-121">Fecha um dispositivo de saída MIDI especificado.</span><span class="sxs-lookup"><span data-stu-id="989e5-121">Closes a specified MIDI output device.</span></span>             |
| [<span data-ttu-id="989e5-122">**midiOutOpen**</span><span class="sxs-lookup"><span data-stu-id="989e5-122">**midiOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | <span data-ttu-id="989e5-123">Abre um dispositivo de saída de MIDI para reprodução.</span><span class="sxs-lookup"><span data-stu-id="989e5-123">Opens a MIDI output device for playback.</span></span>           |



 

<span data-ttu-id="989e5-124">Cada função que abre um dispositivo MIDI usa como parâmetros um identificador de dispositivo, um endereço de um local de memória e alguns parâmetros exclusivos de dispositivos MIDI.</span><span class="sxs-lookup"><span data-stu-id="989e5-124">Each function that opens a MIDI device takes as parameters a device identifier, an address of a memory location, and some parameters unique to MIDI devices.</span></span> <span data-ttu-id="989e5-125">O local da memória é preenchido com um identificador de dispositivo, que é usado para identificar o dispositivo de áudio aberto em chamadas a outras funções de áudio.</span><span class="sxs-lookup"><span data-stu-id="989e5-125">The memory location is filled with a device handle, which is used to identify the open audio device in calls to other audio functions.</span></span>

<span data-ttu-id="989e5-126">Muitas funções MIDI podem aceitar um identificador de dispositivo ou um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="989e5-126">Many MIDI functions can accept either a device handle or a device identifier.</span></span> <span data-ttu-id="989e5-127">Embora seja possível usar um identificador de dispositivo onde quer que você use uma identificação de dispositivo, nem sempre é possível usar um identificador de dispositivo quando um identificador é chamado para.</span><span class="sxs-lookup"><span data-stu-id="989e5-127">Although you can use a device handle wherever you would use a device identifier, you cannot always use a device identifier when a handle is called for.</span></span>

> [!Note]  
> <span data-ttu-id="989e5-128">Os dispositivos MIDI não são necessariamente compartilháveis, portanto, um dispositivo específico pode não estar disponível quando um usuário solicitá-lo.</span><span class="sxs-lookup"><span data-stu-id="989e5-128">MIDI devices are not necessarily sharable, so a particular device may not be available when a user requests it.</span></span> <span data-ttu-id="989e5-129">Se isso acontecer, o aplicativo deve notificar o usuário e permitir que o usuário tente abrir o dispositivo novamente.</span><span class="sxs-lookup"><span data-stu-id="989e5-129">If this happens, the application should notify the user and allow the user to try to open the device again.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="989e5-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="989e5-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="989e5-131">Serviços MIDI</span><span class="sxs-lookup"><span data-stu-id="989e5-131">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 