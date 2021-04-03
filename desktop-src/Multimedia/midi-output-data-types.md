---
title: Tipos de dados de saída de MIDI
description: Tipos de dados de saída de MIDI
ms.assetid: d0cb0614-e979-4b9f-81ce-13457fdde906
keywords:
- MIDI (interface digital de instrumento musical), tipos de dados de saída
- MIDI (interface digital de instrumentos musicais), tipos de dados de saída
- executando arquivos MIDI, tipos de dados de saída
- Tipos de dados de saída de MIDI
- Tipo de dados MIDIHDR
- Tipo de dados MIDIOUTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57911800e0d45c1db515e5b57045aae3856732c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640856"
---
# <a name="midi-output-data-types"></a><span data-ttu-id="a527c-109">Tipos de dados de saída de MIDI</span><span class="sxs-lookup"><span data-stu-id="a527c-109">MIDI Output Data Types</span></span>

<span data-ttu-id="a527c-110">O Windows define os seguintes tipos de dados para funções de saída de MIDI.</span><span class="sxs-lookup"><span data-stu-id="a527c-110">Windows defines the following data types for MIDI output functions.</span></span>



| <span data-ttu-id="a527c-111">Valor</span><span class="sxs-lookup"><span data-stu-id="a527c-111">Value</span></span>                              | <span data-ttu-id="a527c-112">Significado</span><span class="sxs-lookup"><span data-stu-id="a527c-112">Meaning</span></span>                                                                              |
|------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a527c-113">**HMIDIOUT**</span><span class="sxs-lookup"><span data-stu-id="a527c-113">**HMIDIOUT**</span></span>                       | <span data-ttu-id="a527c-114">Identificador de um dispositivo de saída MIDI.</span><span class="sxs-lookup"><span data-stu-id="a527c-114">Handle of a MIDI output device.</span></span>                                                      |
| [<span data-ttu-id="a527c-115">**MIDIHDR**</span><span class="sxs-lookup"><span data-stu-id="a527c-115">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)         | <span data-ttu-id="a527c-116">Cabeçalho de um bloco de dados do sistema MIDI exclusivo ou de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a527c-116">Header for a block of MIDI system-exclusive or stream data.</span></span>                          |
| [<span data-ttu-id="a527c-117">**MIDIOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="a527c-117">**MIDIOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) | <span data-ttu-id="a527c-118">Estrutura usada para consultar os recursos de um dispositivo de saída de MIDI específico.</span><span class="sxs-lookup"><span data-stu-id="a527c-118">Structure used to inquire about the capabilities of a particular MIDI output device.</span></span> |



 

 

 