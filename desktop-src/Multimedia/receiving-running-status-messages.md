---
title: Recebendo mensagens de Running-Status
description: Recebendo mensagens de Running-Status
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- MIDI (interface digital de instrumento musical), status em execução
- MIDI (interface digital de instrumento musical), status em execução
- gravando áudio MIDI, status em execução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4d12a19f525a6fa673747063774bf4507d65b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363699"
---
# <a name="receiving-running-status-messages"></a><span data-ttu-id="a01c1-106">Recebendo mensagens de Running-Status</span><span class="sxs-lookup"><span data-stu-id="a01c1-106">Receiving Running-Status Messages</span></span>

<span data-ttu-id="a01c1-107">A especificação *padrão de arquivos MIDI 1,0* permite o uso do *status de execução* quando uma mensagem tem o mesmo byte de status da mensagem anterior.</span><span class="sxs-lookup"><span data-stu-id="a01c1-107">The *Standard MIDI Files 1.0* specification allows the use of *running status* when a message has the same status byte as the previous message.</span></span> <span data-ttu-id="a01c1-108">Quando o status em execução é usado, o byte de status das mensagens subsequentes pode ser omitido.</span><span class="sxs-lookup"><span data-stu-id="a01c1-108">When running status is used, the status byte of subsequent messages can be omitted.</span></span> <span data-ttu-id="a01c1-109">Todos os drivers de dispositivo de entrada MIDI são necessários para expandir as mensagens usando o status de execução em mensagens completas, para que você sempre receba mensagens de MIDI completas de um driver de dispositivo de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="a01c1-109">All MIDI input device drivers are required to expand messages using running status into complete messages, so that you always receive complete MIDI messages from a MIDI input device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a01c1-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a01c1-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a01c1-111">Gravando áudio MIDI</span><span class="sxs-lookup"><span data-stu-id="a01c1-111">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 




