---
title: Abrindo e fechando dispositivos do mixer
description: Abrindo e fechando dispositivos do mixer
ms.assetid: b1943308-3778-485e-80f3-6d80cb583e00
keywords:
- áudio de multimídia, abrindo dispositivos de mixer
- áudio, abrindo dispositivos do mixer
- mixers de áudio, abrindo
- mixers, abrindo
- áudio multimídia, dispositivos do mixer de fechamento
- áudio, fechando dispositivos do mixer
- mixers de áudio, fechando
- mixers, fechando
- abrindo dispositivos do mixer
- fechando dispositivos do mixer
- identificadores de dispositivo vs. identificadores de dispositivo
- mixers de áudio, identificadores de dispositivo versus identificadores de dispositivo
- mixers, identificadores de dispositivo versus identificadores de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2be7fcc0563508aabfd957109d62c7dbfe1c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007396"
---
# <a name="opening-and-closing-mixer-devices"></a><span data-ttu-id="5c2b8-116">Abrindo e fechando dispositivos do mixer</span><span class="sxs-lookup"><span data-stu-id="5c2b8-116">Opening and Closing Mixer Devices</span></span>

<span data-ttu-id="5c2b8-117">Quando você quiser usar um dispositivo de mixer, você pode simplesmente começar a usá-lo ou pode abrir o dispositivo explicitamente antes de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-117">When you want to use a mixer device, you can either simply begin using it or you can explicitly open the device before using it.</span></span> <span data-ttu-id="5c2b8-118">A abertura explícita de um dispositivo de mixer oferece dois benefícios principais:</span><span class="sxs-lookup"><span data-stu-id="5c2b8-118">Explicitly opening a mixer device offers two main benefits:</span></span>

-   <span data-ttu-id="5c2b8-119">Ele garante a existência contínua desse dispositivo de mixer.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-119">It guarantees the continued existence of that mixer device.</span></span>
-   <span data-ttu-id="5c2b8-120">Ele permite que você receba notificação de alterações de linha de áudio e controle.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-120">It lets you receive notification of audio line and control changes.</span></span>

<span data-ttu-id="5c2b8-121">Você pode usar a função [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) para abrir explicitamente um dispositivo de mixer.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-121">You can use the [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) function to explicitly open a mixer device.</span></span> <span data-ttu-id="5c2b8-122">Essa função usa como parâmetros um identificador de dispositivo, um ponteiro para um local de memória e outros valores exclusivos para cada tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-122">This function takes as parameters a device identifier, a pointer to a memory location, and other values unique to each type of device.</span></span> <span data-ttu-id="5c2b8-123">O local da memória é preenchido com um identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-123">The memory location is filled with a device handle.</span></span> <span data-ttu-id="5c2b8-124">Use este identificador de dispositivo para identificar o dispositivo do mixer aberto ao chamar outras funções do mixer de áudio.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-124">Use this device handle to identify the open mixer device when calling other audio mixer functions.</span></span> <span data-ttu-id="5c2b8-125">Desde que exista um identificador de um dispositivo de mixer, o dispositivo continua existindo no sistema.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-125">As long as a handle of a mixer device exists, the device continues to exist in the system.</span></span> <span data-ttu-id="5c2b8-126">Se uma alteração de configuração ocorrer no dispositivo do mixer e ele não tiver sido aberto explicitamente, seu aplicativo poderá não conseguir acessá-lo repentinamente.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-126">If a configuration change occurs to the mixer device and it hasn't been explicitly opened, your application might suddenly be unable to access it.</span></span>

> [!Note]  
> <span data-ttu-id="5c2b8-127">A diferença entre identificadores de dispositivo e identificadores de dispositivo é importante.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-127">The difference between device identifiers and device handles is important.</span></span> <span data-ttu-id="5c2b8-128">Os identificadores de dispositivo são retornados quando você abre um driver de dispositivo usando **mixerOpen**.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-128">Device handles are returned when you open a device driver by using **mixerOpen**.</span></span> <span data-ttu-id="5c2b8-129">Os identificadores de dispositivo são determinados implicitamente do número de dispositivos presentes em um sistema; Esse número é obtido usando a função [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="5c2b8-129">Device identifiers are determined implicitly from the number of devices present in a system; this number is obtained by using the [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) function.</span></span>

 

<span data-ttu-id="5c2b8-130">Você pode usar a função [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) para fechar um dispositivo de mixer.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-130">You can use the [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) function to close a mixer device.</span></span> <span data-ttu-id="5c2b8-131">Você deve fechar o dispositivo depois de terminar de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="5c2b8-131">You should close the device after you finish using it.</span></span>

 

 