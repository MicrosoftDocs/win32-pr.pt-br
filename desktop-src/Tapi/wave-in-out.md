---
description: A classe de dispositivo Wave/in/out consiste em dispositivos de áudio full duplex.
ms.assetid: 1b49c9ae-da64-4415-95ce-785ffedc65bc
title: Wave/entrada/saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e814cf2e8de1c3c5700a7570d2ed2b4c428572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756981"
---
# <a name="waveinout"></a><span data-ttu-id="b0c85-103">Wave/entrada/saída</span><span class="sxs-lookup"><span data-stu-id="b0c85-103">wave/in/out</span></span>

<span data-ttu-id="b0c85-104">A classe de dispositivo Wave/in/out consiste em dispositivos de áudio full duplex.</span><span class="sxs-lookup"><span data-stu-id="b0c85-104">The wave/in/out device class consists of full duplex audio devices.</span></span> <span data-ttu-id="b0c85-105">Você acessa esses dispositivos usando as funções de onda, que são descritas no SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="b0c85-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="b0c85-106">Os dispositivos nessa classe estão associados a dispositivos de linha que dão suporte ao \_ tipo de mídia LINEMEDIAMODE AUTOMATEDVOICE, que é especificado no membro **dwMediaModes** da estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para o dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="b0c85-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="b0c85-107">As funções [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenchem uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **dwStringFormat** como o \_ valor binário StringFormat e acrescentando dois membros adicionais:</span><span class="sxs-lookup"><span data-stu-id="b0c85-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending two additional members:</span></span>

``` syntax
DWORD DeviceInId;  // identifier of wave in audio device
DWORD DeviceOutId;  // identifier of wave out audio device
```

<span data-ttu-id="b0c85-108">Os membros **DeviceInId** e **DeviceOutId** são identificadores de um dispositivo de áudio fechado.</span><span class="sxs-lookup"><span data-stu-id="b0c85-108">The **DeviceInId** and **DeviceOutId** members are identifiers of a closed audio device.</span></span> <span data-ttu-id="b0c85-109">Você usa esses identificadores em uma chamada para a função [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir o dispositivo para saída.</span><span class="sxs-lookup"><span data-stu-id="b0c85-109">You use these identifiers in a call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function to open the device for output.</span></span> <span data-ttu-id="b0c85-110">Você pode usar o identificador de dispositivo resultante para reproduzir dados de áudio digitalizados no dispositivo de linha ou telefone.</span><span class="sxs-lookup"><span data-stu-id="b0c85-110">You can use the resulting device handle to play digitized audio data at the line or phone device.</span></span>

<span data-ttu-id="b0c85-111">Para obter mais informações sobre as funções de onda, consulte [**funções de multimídia**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b0c85-111">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
