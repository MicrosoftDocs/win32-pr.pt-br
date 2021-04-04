---
title: Consultas de dispositivo do mixer
description: Consultas de dispositivo do mixer
ms.assetid: 3b453802-954b-4356-9ad5-0f8376b6199d
keywords:
- áudio multimídia, consultas de dispositivo do mixer
- áudio, consultas de dispositivo do mixer
- mixers de áudio, consultas de dispositivo
- mixers, consultas de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02acc3d5c7e418d14412c60a2e28e32849497c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007487"
---
# <a name="mixer-device-queries"></a><span data-ttu-id="eedbf-107">Consultas de dispositivo do mixer</span><span class="sxs-lookup"><span data-stu-id="eedbf-107">Mixer Device Queries</span></span>

<span data-ttu-id="eedbf-108">Os serviços de mixer fornecem funções para determinar o número de dispositivos de mixer presentes no sistema e os recursos dos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="eedbf-108">The mixer services provide functions for determining the number of mixer devices present in the system and the capabilities of the devices.</span></span> <span data-ttu-id="eedbf-109">Você também pode usar uma função de serviços de mixer para determinar o identificador de dispositivo para um dispositivo de mixer.</span><span class="sxs-lookup"><span data-stu-id="eedbf-109">You can also use a mixer services function to determine the device identifier for a mixer device.</span></span>

<span data-ttu-id="eedbf-110">Você pode usar a função [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) para determinar quantos dispositivos de mixer estão presentes no sistema.</span><span class="sxs-lookup"><span data-stu-id="eedbf-110">You can use the [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) function to determine how many mixer devices are present in the system.</span></span> <span data-ttu-id="eedbf-111">Os dispositivos do mixer são identificados por um identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eedbf-111">Mixer devices are identified by a device identifier.</span></span> <span data-ttu-id="eedbf-112">Os identificadores de dispositivo são determinados implicitamente a partir do número de dispositivos presentes em um determinado sistema.</span><span class="sxs-lookup"><span data-stu-id="eedbf-112">Device identifiers are determined implicitly from the number of devices present in a given system.</span></span> <span data-ttu-id="eedbf-113">Elas variam de zero a um menor que o número de dispositivos presentes.</span><span class="sxs-lookup"><span data-stu-id="eedbf-113">They range from zero through one less than the number of devices present.</span></span>

<span data-ttu-id="eedbf-114">Antes de usar um dispositivo de mixer, você deve determinar seus recursos.</span><span class="sxs-lookup"><span data-stu-id="eedbf-114">Before using a mixer device, you must determine its capabilities.</span></span> <span data-ttu-id="eedbf-115">Os recursos de áudio podem variar de um computador de multimídia para outro, para que os aplicativos precisem trabalhar com uma variedade de hardwares de áudio.</span><span class="sxs-lookup"><span data-stu-id="eedbf-115">Audio capabilities can vary from one multimedia computer to another, so applications need to work with a variety of audio hardware.</span></span>

<span data-ttu-id="eedbf-116">Você pode usar a função [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) para determinar os recursos dos dispositivos de mixer.</span><span class="sxs-lookup"><span data-stu-id="eedbf-116">You can use the [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) function to determine the capabilities of mixer devices.</span></span> <span data-ttu-id="eedbf-117">Essa função preenche uma estrutura [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) com informações sobre os recursos de um dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="eedbf-117">This function fills a [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) structure with information about the capabilities of a specified device.</span></span>

<span data-ttu-id="eedbf-118">A função [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) recupera o identificador de dispositivo do mixer de áudio associado a um identificador de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="eedbf-118">The [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) function retrieves the audio mixer device identifier associated with a specified device handle.</span></span> <span data-ttu-id="eedbf-119">Por exemplo, você pode usar essa função para recuperar o identificador de dispositivo para um mixer de áudio e, em seguida, usar o identificador do dispositivo para ajustar o volume ou para exibir outro controle.</span><span class="sxs-lookup"><span data-stu-id="eedbf-119">For example, you could use this function to retrieve the device identifier for an audio mixer and then use the device identifier to adjust the volume or to display another control.</span></span>

 

 