---
title: Reprodução de loops (áudio de onda)
description: Reprodução de loops (áudio de onda)
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- áudio de onda, sons de loop
- Wave-interface de áudio, looping de sons
- áudio de onda, reprodução em loop
- Wave-interface de áudio, reprodução em loop
- executar loop de Wave-sons de áudio
- execução em loop de Wave-reprodução de áudio
- função waveOutWrite
- função waveOutBreakLoop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c233799e2d4faf8107b4a2a68a261b544ec1274
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105747733"
---
# <a name="looping-playback"></a><span data-ttu-id="eb40e-111">Reprodução de loop</span><span class="sxs-lookup"><span data-stu-id="eb40e-111">Looping Playback</span></span>

<span data-ttu-id="eb40e-112">O loop de um som é controlado pelos membros **dwLoops** e **dwFlags** nas estruturas [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) passadas para o dispositivo com a função [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) .</span><span class="sxs-lookup"><span data-stu-id="eb40e-112">Looping a sound is controlled by the **dwLoops** and **dwFlags** members in the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structures passed to the device with the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function.</span></span> <span data-ttu-id="eb40e-113">Use os sinalizadores **WHDR \_ BEGINLOOP** e **WHDR \_ ENDLOOP** no membro **dwFlags** para especificar os blocos de dados inicial e final para looping.</span><span class="sxs-lookup"><span data-stu-id="eb40e-113">Use the **WHDR\_BEGINLOOP** and **WHDR\_ENDLOOP** flags in the **dwFlags** member to specify the beginning and ending data blocks for looping.</span></span>

<span data-ttu-id="eb40e-114">Para repetir um único bloco de dados, especifique os dois sinalizadores para o mesmo bloco.</span><span class="sxs-lookup"><span data-stu-id="eb40e-114">To loop a single data block, specify both flags for the same block.</span></span> <span data-ttu-id="eb40e-115">Para especificar o número de loops, use o membro **dwLoops** na estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para o primeiro bloco no loop.</span><span class="sxs-lookup"><span data-stu-id="eb40e-115">To specify the number of loops, use the **dwLoops** member in the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure for the first block in the loop.</span></span>

<span data-ttu-id="eb40e-116">Você pode chamar a função [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) para interromper um som de loop.</span><span class="sxs-lookup"><span data-stu-id="eb40e-116">You can call the [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) function to stop a looping sound.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb40e-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eb40e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb40e-118">Executando Waveform-Audio arquivos</span><span class="sxs-lookup"><span data-stu-id="eb40e-118">Playing Waveform-Audio Files</span></span>](playing-waveform-audio-files.md)
</dt> </dl>

 

 
