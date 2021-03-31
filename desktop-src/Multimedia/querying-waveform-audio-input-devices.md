---
title: Consultando Waveform-Audio dispositivos de entrada
description: Consultando Waveform-Audio dispositivos de entrada
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- áudio de formato de onda, consultando dispositivos de entrada
- Wave-interface de áudio, consultando dispositivos de entrada
- gravando áudio de onda, consultando dispositivos de entrada
- consultando dispositivos de entrada de formato wave-áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b915b3f39ad417a3d92396d887e5fb66092119
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917242"
---
# <a name="querying-waveform-audio-input-devices"></a><span data-ttu-id="4cc59-107">Consultando Waveform-Audio dispositivos de entrada</span><span class="sxs-lookup"><span data-stu-id="4cc59-107">Querying Waveform-Audio Input Devices</span></span>

<span data-ttu-id="4cc59-108">Antes de gravar áudio de onda, você deve chamar a função [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) para determinar os recursos de entrada de onda de áudio do sistema.</span><span class="sxs-lookup"><span data-stu-id="4cc59-108">Before recording waveform audio, you should call the [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) function to determine the waveform-audio input capabilities of the system.</span></span> <span data-ttu-id="4cc59-109">Essa função preenche uma estrutura [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) com informações sobre os recursos de um dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="4cc59-109">This function fills a [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) structure with information about the capabilities of a specified device.</span></span> <span data-ttu-id="4cc59-110">Essas informações incluem os identificadores de fabricante e produto, um nome de produto para o dispositivo e o número de versão do driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4cc59-110">This information includes the manufacturer and product identifiers, a product name for the device, and the version number of the device driver.</span></span> <span data-ttu-id="4cc59-111">Além disso, a estrutura **WAVEINCAPS** fornece informações sobre os formatos de áudio de forma de onda padrão aos quais o dispositivo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="4cc59-111">In addition, the **WAVEINCAPS** structure provides information about the standard waveform-audio formats that the device supports.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cc59-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4cc59-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cc59-113">Gravando áudio de onda</span><span class="sxs-lookup"><span data-stu-id="4cc59-113">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 