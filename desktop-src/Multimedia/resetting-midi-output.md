---
title: Redefinindo a saída de MIDI
description: Redefinindo a saída de MIDI
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- MIDI (interface digital de instrumento musical), redefinindo dispositivos de saída
- MIDI (interface digital de instrumentos musicais), redefinindo dispositivos de saída
- executando arquivos MIDI, redefinindo dispositivos de saída
- Redefinindo dispositivos de saída
- MIDI (interface digital de instrumento musical), dispositivos de saída
- MIDI (interface digital de instrumentos musicais), dispositivos de saída
- executando arquivos MIDI, dispositivos de saída
- Dispositivos de saída MIDI
- EOX (fim de exclusivo)
- fim de exclusivo (EOX)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15778fc8a1a48c34b69915aafb7e3139153b5882
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293910"
---
# <a name="resetting-midi-output"></a><span data-ttu-id="5b650-113">Redefinindo a saída de MIDI</span><span class="sxs-lookup"><span data-stu-id="5b650-113">Resetting MIDI Output</span></span>

<span data-ttu-id="5b650-114">A função [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) desativa todas as notas em todos os canais MIDI para um dispositivo MIDI especificado.</span><span class="sxs-lookup"><span data-stu-id="5b650-114">The [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) function turns off all notes on all MIDI channels for a specified MIDI device.</span></span> <span data-ttu-id="5b650-115">Em seguida, a função marca quaisquer buffers exclusivos do sistema pendentes como concluído e os retorna para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5b650-115">Then, the function marks any pending system-exclusive buffers as done and returns them to the application.</span></span> <span data-ttu-id="5b650-116">Essa função pode ser útil em um aplicativo que usa a saída de MIDI para fornecer ao usuário a capacidade de redefinir a saída de MIDI.</span><span class="sxs-lookup"><span data-stu-id="5b650-116">This function can be useful in an application that uses MIDI output to provide the user with the ability to reset MIDI output.</span></span>

> [!Note]  
> <span data-ttu-id="5b650-117">Encerrar uma mensagem exclusiva do sistema sem enviar um byte EOX (fim de exclusivo) pode causar problemas para o dispositivo receptor.</span><span class="sxs-lookup"><span data-stu-id="5b650-117">Terminating a system-exclusive message without sending an EOX (end-of-exclusive) byte can cause problems for the receiving device.</span></span> <span data-ttu-id="5b650-118">A função **midiOutReset** não envia um byte EOX quando ele termina uma mensagem exclusiva do sistema, porque os aplicativos são responsáveis por fazer isso.</span><span class="sxs-lookup"><span data-stu-id="5b650-118">The **midiOutReset** function does not send an EOX byte when it terminates a system-exclusive message, because applications are responsible for doing this.</span></span>

 

 

 