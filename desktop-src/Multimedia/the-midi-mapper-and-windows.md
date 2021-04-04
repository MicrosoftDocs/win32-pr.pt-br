---
title: O mapeador de MIDI e o Windows
description: O mapeador de MIDI e o Windows
ms.assetid: a077f935-e085-4148-9975-7926ac018f0c
keywords:
- MIDI (interface digital de instrumento musical), mapeador de MIDI
- MIDI (interface digital de instrumentos musicais), mapeador de MIDI
- Mapeador de MIDI, arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad3cee4fb37de6ecbfdc4f81860afcb9f589d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007481"
---
# <a name="the-midi-mapper-and-windows"></a><span data-ttu-id="93fc9-106">O mapeador de MIDI e o Windows</span><span class="sxs-lookup"><span data-stu-id="93fc9-106">The MIDI Mapper and Windows</span></span>

<span data-ttu-id="93fc9-107">O mapeador de MIDI faz parte do software do sistema.</span><span class="sxs-lookup"><span data-stu-id="93fc9-107">The MIDI Mapper is part of the system software.</span></span> <span data-ttu-id="93fc9-108">A ilustração a seguir mostra como o mapeador de MIDI está relacionado a outros elementos dos serviços de áudio.</span><span class="sxs-lookup"><span data-stu-id="93fc9-108">The following illustration shows how the MIDI Mapper relates to other elements of the audio services.</span></span>

![como o mapeador de Midi está relacionado a outros elementos da imagem dos serviços de áudio](images/mmap-a01.gif)

<span data-ttu-id="93fc9-110">Do ponto de vista de um aplicativo, o mapeador de MIDI parece outro dispositivo de saída MIDI.</span><span class="sxs-lookup"><span data-stu-id="93fc9-110">From the viewpoint of an application, the MIDI Mapper looks like another MIDI output device.</span></span> <span data-ttu-id="93fc9-111">O mapeador de MIDI recebe mensagens enviadas a ele pelas funções de saída de MIDI de baixo nível [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) e [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg).</span><span class="sxs-lookup"><span data-stu-id="93fc9-111">The MIDI Mapper receives messages sent to it by the low-level MIDI output functions [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) and [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg).</span></span> <span data-ttu-id="93fc9-112">O mapeador de MIDI modifica essas mensagens e as redireciona para um dispositivo de saída de MIDI de acordo com o mapa de configuração de MIDI atual.</span><span class="sxs-lookup"><span data-stu-id="93fc9-112">The MIDI Mapper modifies these messages and redirects them to a MIDI output device according to the current MIDI setup map.</span></span> <span data-ttu-id="93fc9-113">O mapa de instalação do MIDI atual é selecionado pelo usuário por meio da opção do painel de controle de MIDI.</span><span class="sxs-lookup"><span data-stu-id="93fc9-113">The current MIDI setup map is selected by the user by means of the MIDI Control Panel option.</span></span> <span data-ttu-id="93fc9-114">Somente o usuário pode selecionar o mapa de instalação atual; os aplicativos não podem alterar o mapa de instalação atual.</span><span class="sxs-lookup"><span data-stu-id="93fc9-114">Only the user can select the current setup map; applications cannot change the current setup map.</span></span>

 

 