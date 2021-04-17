---
title: Abrindo Waveform-Audio dispositivos de entrada
description: Abrindo Waveform-Audio dispositivos de entrada
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- áudio de formato de onda, abrindo dispositivos de entrada
- formato de onda-interface de áudio, abertura de dispositivos de entrada
- gravando áudio de onda, abrindo dispositivos de entrada
- abrindo Wave-dispositivos de entrada de áudio
- função waveInOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92b7f49b9d170ceb8ebce287025ce0e0c1c5530
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105766373"
---
# <a name="opening-waveform-audio-input-devices"></a><span data-ttu-id="4c077-108">Abrindo Waveform-Audio dispositivos de entrada</span><span class="sxs-lookup"><span data-stu-id="4c077-108">Opening Waveform-Audio Input Devices</span></span>

<span data-ttu-id="4c077-109">Use a função [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) para abrir um dispositivo de entrada de formato de onda-áudio para gravação.</span><span class="sxs-lookup"><span data-stu-id="4c077-109">Use the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function to open a waveform-audio input device for recording.</span></span> <span data-ttu-id="4c077-110">Essa função abre o dispositivo associado ao identificador de dispositivo especificado e retorna um identificador do dispositivo aberto gravando o identificador de um local de memória especificado.</span><span class="sxs-lookup"><span data-stu-id="4c077-110">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle of a specified memory location.</span></span>

<span data-ttu-id="4c077-111">Alguns computadores de multimídia têm vários dispositivos de entrada de wave-áudio.</span><span class="sxs-lookup"><span data-stu-id="4c077-111">Some multimedia computers have multiple waveform-audio input devices.</span></span> <span data-ttu-id="4c077-112">A menos que você saiba que deseja abrir um dispositivo de entrada de áudio de forma de onda específico em um sistema, use a \_ constante do mapeador de ondas para o identificador do dispositivo ao abrir um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c077-112">Unless you know you want to open a specific waveform-audio input device in a system, you should use the WAVE\_MAPPER constant for the device identifier when you open a device.</span></span> <span data-ttu-id="4c077-113">A função [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) escolherá o dispositivo no sistema com a melhor capacidade de registrar no formato de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="4c077-113">The [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function will choose the device in the system best able to record in the specified data format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c077-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c077-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c077-115">Gravando áudio de onda</span><span class="sxs-lookup"><span data-stu-id="4c077-115">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 