---
title: Abrindo dispositivos de entrada MIDI
description: Abrindo dispositivos de entrada MIDI
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- MIDI (interface digital de instrumento musical), dispositivos de entrada
- MIDI (interface digital de instrumentos musicais), dispositivos de entrada
- gravando áudio MIDI, dispositivos de entrada
- Dispositivos de entrada MIDI
- MIDI (interface digital de instrumento musical), abrindo dispositivos de entrada
- MIDI (interface digital de instrumentos musicais), abrindo dispositivos de entrada
- gravando áudio MIDI, abrindo dispositivos de entrada
- abrindo dispositivos de entrada MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4c1271cee1e6a47c35f8c555932d87d1055065
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640854"
---
# <a name="opening-midi-input-devices"></a><span data-ttu-id="94e0a-111">Abrindo dispositivos de entrada MIDI</span><span class="sxs-lookup"><span data-stu-id="94e0a-111">Opening MIDI Input Devices</span></span>

<span data-ttu-id="94e0a-112">Para abrir um dispositivo de entrada MIDI para gravação, use a função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="94e0a-112">To open a MIDI input device for recording, use the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span> <span data-ttu-id="94e0a-113">Essa função abre o dispositivo associado ao identificador de dispositivo especificado e retorna um identificador do dispositivo aberto gravando o identificador em um local de memória especificado.</span><span class="sxs-lookup"><span data-stu-id="94e0a-113">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle to a specified memory location.</span></span>

<span data-ttu-id="94e0a-114">Se você usar o \_ sinalizador de status de e/s MIDI \_ com **midiInOpen**, o sistema usará a mensagem [**\_ MOREDATA do mim**](mim-moredata.md) para alertar a função de retorno de chamada do aplicativo quando não estiver processando dados MIDI rápido o suficiente para acompanhar o driver de dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="94e0a-114">If you use the MIDI\_IO\_STATUS flag with **midiInOpen**, the system uses the [**MIM\_MOREDATA**](mim-moredata.md) message to alert your application's callback function when it is not processing MIDI data fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="94e0a-115">(A mensagem [**mm \_ mim \_ MOREDATA**](mm-mim-moredata.md) faz o mesmo trabalho com retornos de chamada de janela.</span><span class="sxs-lookup"><span data-stu-id="94e0a-115">(The [**MM\_MIM\_MOREDATA**](mm-mim-moredata.md) message does the same job with window callbacks.</span></span> <span data-ttu-id="94e0a-116">No entanto, por motivos de desempenho, a maioria dos aplicativos usará funções de retorno de chamada em vez de retornos de chamada de janela. Se seu aplicativo processa dados MIDI em um thread separado, aumentar a prioridade do thread pode ter um impacto significativo na capacidade do aplicativo de acompanhar o fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="94e0a-116">However, for performance reasons, most applications will use callback functions instead of window callbacks.) If your application processes MIDI data in a separate thread, boosting the thread's priority can have a significant impact on the application's ability to keep up with the data flow.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94e0a-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94e0a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94e0a-118">Gravando áudio MIDI</span><span class="sxs-lookup"><span data-stu-id="94e0a-118">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 