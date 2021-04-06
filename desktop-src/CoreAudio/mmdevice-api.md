---
description: Sobre a API do MMDevice
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: Sobre a API do MMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82843bbecf004d0931575d73ec2459c3e72a3cf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646469"
---
# <a name="about-mmdevice-api"></a><span data-ttu-id="58329-103">Sobre a API do MMDevice</span><span class="sxs-lookup"><span data-stu-id="58329-103">About MMDevice API</span></span>

<span data-ttu-id="58329-104">A API do dispositivo de multimídia do Windows (MMDevice) permite que os clientes de áudio descubram [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md), determinem seus recursos e criem instâncias de driver para esses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="58329-104">The Windows Multimedia Device (MMDevice) API enables audio clients to discover [audio endpoint devices](audio-endpoint-devices.md), determine their capabilities, and create driver instances for those devices.</span></span>

<span data-ttu-id="58329-105">O arquivo de cabeçalho Mmdeviceapi. h define as interfaces na API MMDevice.</span><span class="sxs-lookup"><span data-stu-id="58329-105">Header file Mmdeviceapi.h defines the interfaces in the MMDevice API.</span></span>

<span data-ttu-id="58329-106">A API MMDevice consiste em várias interfaces.</span><span class="sxs-lookup"><span data-stu-id="58329-106">The MMDevice API consists of several interfaces.</span></span> <span data-ttu-id="58329-107">A primeira delas é a interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="58329-107">The first of these is the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="58329-108">Para acessar as interfaces na API MMDevice, um cliente obtém uma referência à interface **IMMDeviceEnumerator** de um objeto de enumerador de dispositivo chamando a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , conforme mostrado no fragmento de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="58329-108">To access the interfaces in the MMDevice API, a client obtains a reference to the **IMMDeviceEnumerator** interface of a device-enumerator object by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, as shown in the following code fragment:</span></span>


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



<span data-ttu-id="58329-109">No fragmento de código anterior, CLSID \_ MMDeviceEnumerator e IID \_ IMMDeviceEnumerator são os valores de GUID anexados como atributos ao objeto de classe **MMDeviceEnumerator** e à interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="58329-109">In the preceding code fragment, CLSID\_MMDeviceEnumerator and IID\_IMMDeviceEnumerator are the GUID values that are attached as attributes to the **MMDeviceEnumerator** class object and to the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="58329-110">A chamada [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) passa esses valores por referência.</span><span class="sxs-lookup"><span data-stu-id="58329-110">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) call passes these values by reference.</span></span> <span data-ttu-id="58329-111">Variable `hr` é do tipo **HRESULT**, e Variable `pEnumerator` é um ponteiro para a interface **IMMDeviceEnumerator** de um objeto de enumerador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="58329-111">Variable `hr` is of type **HRESULT**, and variable `pEnumerator` is a pointer to the **IMMDeviceEnumerator** interface of a device-enumerator object.</span></span> <span data-ttu-id="58329-112">**IMMDeviceEnumerator** fornece métodos para enumerar dispositivos de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="58329-112">**IMMDeviceEnumerator** provides methods for enumerating audio endpoint devices.</span></span> <span data-ttu-id="58329-113">Para obter informações sobre o operador **\_ \_ uuidof** , a função **CoCreateInstance** e as constantes CLSCTX \_ *xxx* , consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="58329-113">For information about the **\_\_uuidof** operator, the **CoCreateInstance** function, and the CLSCTX\_*Xxx* constants, see the Windows SDK documentation.</span></span>

<span data-ttu-id="58329-114">Por meio da interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) , o cliente pode obter referências às outras interfaces na API MMDevice.</span><span class="sxs-lookup"><span data-stu-id="58329-114">Through the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, the client can obtain references to the other interfaces in the MMDevice API.</span></span> <span data-ttu-id="58329-115">A API MMDevice implementa as interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="58329-115">The MMDevice API implements the following interfaces.</span></span>



| <span data-ttu-id="58329-116">Interface</span><span class="sxs-lookup"><span data-stu-id="58329-116">Interface</span></span>                                          | <span data-ttu-id="58329-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="58329-117">Description</span></span>                                     |
|----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="58329-118">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="58329-118">**IMMDevice**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | <span data-ttu-id="58329-119">Representa um dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="58329-119">Represents an audio device.</span></span>                     |
| [<span data-ttu-id="58329-120">**IMMDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="58329-120">**IMMDeviceCollection**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | <span data-ttu-id="58329-121">Representa uma coleção de dispositivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="58329-121">Represents a collection of audio devices.</span></span>       |
| [<span data-ttu-id="58329-122">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="58329-122">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | <span data-ttu-id="58329-123">Fornece métodos para enumerar dispositivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="58329-123">Provides methods for enumerating audio devices.</span></span> |
| [<span data-ttu-id="58329-124">**IMMEndpoint**</span><span class="sxs-lookup"><span data-stu-id="58329-124">**IMMEndpoint**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | <span data-ttu-id="58329-125">Representa um dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="58329-125">Represents an audio endpoint device.</span></span>            |



 

<span data-ttu-id="58329-126">Além disso, os clientes da API MMDevice que exigem notificação de alterações de status em dispositivos de ponto de extremidade de áudio devem implementar a interface a seguir.</span><span class="sxs-lookup"><span data-stu-id="58329-126">In addition, clients of the MMDevice API that require notification of status changes in audio endpoint devices should implement the following interface.</span></span>



| <span data-ttu-id="58329-127">Interface</span><span class="sxs-lookup"><span data-stu-id="58329-127">Interface</span></span>                                              | <span data-ttu-id="58329-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="58329-128">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58329-129">**IMMNotificationClient**</span><span class="sxs-lookup"><span data-stu-id="58329-129">**IMMNotificationClient**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | <span data-ttu-id="58329-130">Fornece notificações quando um dispositivo de ponto de extremidade de áudio é adicionado ou removido, quando o estado ou as propriedades de um dispositivo são alterados ou quando há uma alteração na função padrão atribuída a um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="58329-130">Provides notifications when an audio endpoint device is added or removed, when the state or properties of a device change, or when there is a change in the default role assigned to a device.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="58329-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="58329-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58329-132">Dispositivos de ponto de extremidade de áudio</span><span class="sxs-lookup"><span data-stu-id="58329-132">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> <dt>

[<span data-ttu-id="58329-133">**Referência de programação**</span><span class="sxs-lookup"><span data-stu-id="58329-133">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 
