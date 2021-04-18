---
title: Tipos de dados de entrada de MIDI
description: Tipos de dados de entrada de MIDI
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- MIDI (interface digital de instrumento musical), tipos de dados de entrada
- MIDI (interface digital de instrumentos musicais), tipos de dados de entrada
- gravando áudio MIDI, tipos de dados de entrada
- Tipos de dados de entrada de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f0738827cce4cfd8cb4a237dcd2031c2fe71a7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105757367"
---
# <a name="midi-input-data-types"></a><span data-ttu-id="18aa8-107">Tipos de dados de entrada de MIDI</span><span class="sxs-lookup"><span data-stu-id="18aa8-107">MIDI Input Data Types</span></span>

<span data-ttu-id="18aa8-108">O Windows define os seguintes tipos de dados para as funções de entrada de MIDI.</span><span class="sxs-lookup"><span data-stu-id="18aa8-108">Windows defines the following data types for the MIDI input functions.</span></span>



| <span data-ttu-id="18aa8-109">Valor</span><span class="sxs-lookup"><span data-stu-id="18aa8-109">Value</span></span>                            | <span data-ttu-id="18aa8-110">Significado</span><span class="sxs-lookup"><span data-stu-id="18aa8-110">Meaning</span></span>                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18aa8-111">**HMIDIIN**</span><span class="sxs-lookup"><span data-stu-id="18aa8-111">**HMIDIIN**</span></span>                      | <span data-ttu-id="18aa8-112">Identificador de um dispositivo de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="18aa8-112">Handle of a MIDI input device.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="18aa8-113">**MIDIHDR**</span><span class="sxs-lookup"><span data-stu-id="18aa8-113">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | <span data-ttu-id="18aa8-114">Cabeçalho de um buffer de fluxo ou de um bloco de dados exclusivos do sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="18aa8-114">Header for a stream buffer or a block of MIDI system-exclusive data.</span></span> <span data-ttu-id="18aa8-115">Para aplicativos de entrada, essa estrutura registra somente dados exclusivos do sistema (não há suporte para streaming para entrada MIDI).</span><span class="sxs-lookup"><span data-stu-id="18aa8-115">For input applications, this structure records only system-exclusive data (streaming is not supported for MIDI input).</span></span> |
| [<span data-ttu-id="18aa8-116">**MIDIINCAPS**</span><span class="sxs-lookup"><span data-stu-id="18aa8-116">**MIDIINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | <span data-ttu-id="18aa8-117">Estrutura usada para consultar os recursos de um dispositivo de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="18aa8-117">Structure used to inquire about the capabilities of a MIDI input device.</span></span>                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="18aa8-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="18aa8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18aa8-119">Gravando áudio MIDI</span><span class="sxs-lookup"><span data-stu-id="18aa8-119">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 