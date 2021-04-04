---
description: A classe de dispositivo Wave/in consiste em dispositivos de áudio para entrada de áudio de ondas de baixo nível.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: onda/entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3465a575937538c6a4113ec544b1d246fec3a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171238"
---
# <a name="wavein"></a><span data-ttu-id="3a058-103">onda/entrada</span><span class="sxs-lookup"><span data-stu-id="3a058-103">wave/in</span></span>

<span data-ttu-id="3a058-104">A classe de dispositivo Wave/in consiste em dispositivos de áudio para entrada de áudio de ondas de baixo nível.</span><span class="sxs-lookup"><span data-stu-id="3a058-104">The wave/in device class consists of audio devices for low-level wave audio input.</span></span> <span data-ttu-id="3a058-105">Você acessa esses dispositivos usando as funções de onda, que são descritas no SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="3a058-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="3a058-106">Os dispositivos nessa classe estão associados a dispositivos de linha que dão suporte ao \_ tipo de mídia LINEMEDIAMODE AUTOMATEDVOICE, que é especificado no membro **dwMediaModes** da estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para o dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="3a058-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="3a058-107">As funções [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenchem uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **dwStringFormat** como o \_ valor binário StringFormat e acrescentando esse membro adicional:</span><span class="sxs-lookup"><span data-stu-id="3a058-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of audio device
```

<span data-ttu-id="3a058-108">O membro **DeviceID** é o identificador de um dispositivo de áudio fechado.</span><span class="sxs-lookup"><span data-stu-id="3a058-108">The **DeviceId** member is the identifier of a closed audio device.</span></span> <span data-ttu-id="3a058-109">Você usa esse identificador em uma chamada para a função [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) para abrir o dispositivo para entrada.</span><span class="sxs-lookup"><span data-stu-id="3a058-109">You use this identifier in a call to the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function to open the device for input.</span></span> <span data-ttu-id="3a058-110">Você pode usar o identificador de dispositivo resultante para registrar dados de áudio digitalizados do dispositivo de linha ou telefone.</span><span class="sxs-lookup"><span data-stu-id="3a058-110">You can use the resulting device handle to record digitized audio data from the line or phone device.</span></span>

<span data-ttu-id="3a058-111">Embora uma classe de dispositivo "Wave" também exista para dispositivos de áudio wave de baixo nível, você sempre deve usar a classe Wave/in Device para a entrada de ondas de baixo nível.</span><span class="sxs-lookup"><span data-stu-id="3a058-111">Although a "wave" device class also exists for low-level wave audio devices, you should always use the wave/in device class for low-level wave input.</span></span>

<span data-ttu-id="3a058-112">Para obter mais informações sobre as funções de onda, consulte [**funções de multimídia**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="3a058-112">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
