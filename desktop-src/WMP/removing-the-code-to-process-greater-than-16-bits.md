---
title: Removendo o código para processar mais de 16 bits
description: Removendo o código para processar mais de 16 bits
ms.assetid: 90c165e1-bc77-42a5-878d-056762c62991
keywords:
- Plug-ins do Windows Media Player, método Echo DoProcessOutput de exemplo
- plug-ins, exemplo de método Echo DoProcessOutput
- plug-ins de processamento de sinal digital, Echo Sample DoProcessOutput Method
- Plug-ins do DSP, método Echo de exemplo DoProcessOutput
- Exemplo de plug-in do DSP de eco, método DoProcessOutput
- Exemplo de plug-in do eco DSP, processando mais de 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec33332ee332d0ca7b615844ba8ad5cd7b00eb2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822651"
---
# <a name="removing-the-code-to-process-greater-than-16-bits"></a><span data-ttu-id="0e81d-109">Removendo o código para processar mais de 16 bits</span><span class="sxs-lookup"><span data-stu-id="0e81d-109">Removing the Code to Process Greater than 16 Bits</span></span>

<span data-ttu-id="0e81d-110">Como este exemplo só processa áudio de 8 ou 16 bits, você precisa modificar o código em **CEcho:: ValidateMediaType** para retornar o \_ tipo DMO E \_ \_ não \_ aceito para tipos de mídia maiores que 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0e81d-110">Because this sample only processes 8-bit or 16-bit audio, you need to modify the code in **CEcho::ValidateMediaType** to return DMO\_E\_TYPE\_NOT\_ACCEPTED for media types greater than 16 bits.</span></span> <span data-ttu-id="0e81d-111">Para fazer isso, você deve alterar o código no bloco switch que testa os formatos do tipo WAVE \_ Format \_ extensível.</span><span class="sxs-lookup"><span data-stu-id="0e81d-111">To accomplish this, you must change the code in the switch block that tests formats of type WAVE\_FORMAT\_EXTENSIBLE.</span></span> <span data-ttu-id="0e81d-112">Substitua o código do assistente pelo seguinte código de exemplo:</span><span class="sxs-lookup"><span data-stu-id="0e81d-112">Replace the wizard code with the following example code:</span></span>


```C++
case WAVE_FORMAT_EXTENSIBLE:
    {
         // Sample size is greater than 16-bit or is multichannel.
        WAVEFORMATEXTENSIBLE *pWaveXT = (WAVEFORMATEXTENSIBLE *) pWave;

        if (KSDATAFORMAT_SUBTYPE_PCM != pWaveXT->SubFormat)
        {
            return DMO_E_TYPE_NOT_ACCEPTED;
        }
    }
    break;

```



<span data-ttu-id="0e81d-113">Em seguida, exclua ou comente as seções de código em **DoProcessOutput** que lidam com áudio de alta resolução de bits.</span><span class="sxs-lookup"><span data-stu-id="0e81d-113">Next, delete or comment out the sections of code in **DoProcessOutput** that handle high bit resolution audio.</span></span> <span data-ttu-id="0e81d-114">Essas são as seções que começam com o caso 24 e o caso 32.</span><span class="sxs-lookup"><span data-stu-id="0e81d-114">These are the sections that begin with case 24 and case 32.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e81d-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e81d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e81d-116">**Implementando CEcho::D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="0e81d-116">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




