---
description: Arquivos de cabeçalho e componentes do sistema
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: Arquivos de cabeçalho e componentes do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4b93c63e7d32944dfdf2bf6872bd3a3153e4a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089516"
---
# <a name="header-files-and-system-components"></a><span data-ttu-id="de820-103">Arquivos de cabeçalho e componentes do sistema</span><span class="sxs-lookup"><span data-stu-id="de820-103">Header Files and System Components</span></span>

<span data-ttu-id="de820-104">A tabela a seguir lista os arquivos de cabeçalho que contêm as definições de interface para os quatro componentes de áudio principais.</span><span class="sxs-lookup"><span data-stu-id="de820-104">The following table lists the header files that contain the interface definitions for the four Core Audio components.</span></span>



|                                              |                              |
|----------------------------------------------|------------------------------|
| <span data-ttu-id="de820-105">Componente de áudio principal</span><span class="sxs-lookup"><span data-stu-id="de820-105">Core Audio component</span></span>                         | <span data-ttu-id="de820-106">Arquivo de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="de820-106">Header file</span></span>                  |
| [<span data-ttu-id="de820-107">API MMDevice</span><span class="sxs-lookup"><span data-stu-id="de820-107">MMDevice API</span></span>](mmdevice-api.md)             | <span data-ttu-id="de820-108">Mmdeviceapi. h</span><span class="sxs-lookup"><span data-stu-id="de820-108">Mmdeviceapi.h</span></span>                |
| [<span data-ttu-id="de820-109">WASAPI</span><span class="sxs-lookup"><span data-stu-id="de820-109">WASAPI</span></span>](wasapi.md)                         | <span data-ttu-id="de820-110">Audioclient. h, Audiopolicy. h</span><span class="sxs-lookup"><span data-stu-id="de820-110">Audioclient.h, Audiopolicy.h</span></span> |
| [<span data-ttu-id="de820-111">API DeviceTopology</span><span class="sxs-lookup"><span data-stu-id="de820-111">DeviceTopology API</span></span>](devicetopology-api.md) | <span data-ttu-id="de820-112">Devicetopology. h</span><span class="sxs-lookup"><span data-stu-id="de820-112">Devicetopology.h</span></span>             |
| [<span data-ttu-id="de820-113">API EndpointVolume</span><span class="sxs-lookup"><span data-stu-id="de820-113">EndpointVolume API</span></span>](endpointvolume-api.md) | <span data-ttu-id="de820-114">Endpointvolume. h</span><span class="sxs-lookup"><span data-stu-id="de820-114">Endpointvolume.h</span></span>             |



 

<span data-ttu-id="de820-115">Outro arquivo de cabeçalho, Audiosessiontypes. h, define constantes que são usadas pelo WASAPI.</span><span class="sxs-lookup"><span data-stu-id="de820-115">Another header file, Audiosessiontypes.h, defines constants that are used by WASAPI.</span></span> <span data-ttu-id="de820-116">Esses arquivos de cabeçalho estão localizados no diretório% MSSdk% \\ include, em que% MSSdk% é o diretório raiz da instalação do SDK do Windows no seu computador.</span><span class="sxs-lookup"><span data-stu-id="de820-116">These header files are located in the directory %MSSdk%\\include, where %MSSdk% is the root directory of the Windows SDK installation on your computer.</span></span>

<span data-ttu-id="de820-117">Cada API na tabela anterior consiste em um conjunto de interfaces COM relacionadas.</span><span class="sxs-lookup"><span data-stu-id="de820-117">Each API in the preceding table consists of a set of related COM interfaces.</span></span> <span data-ttu-id="de820-118">Como alguns aspectos do streaming de áudio dependem da baixa latência e da sincronização precisa, as implementações das APIs MMDevice, WASAPI, DeviceTopology e EndpointVolume não usam o Microsoft .NET Framework ou o ambiente de execução gerenciada.</span><span class="sxs-lookup"><span data-stu-id="de820-118">Because some aspects of audio streaming depend on low latency and precise synchronization, the implementations of the MMDevice, WASAPI, DeviceTopology, and EndpointVolume APIs do not use the Microsoft .NET Framework or managed-execution environment.</span></span>

<span data-ttu-id="de820-119">As APIs de áudio principais são implementadas nos componentes do sistema do modo de usuário Audioses.dll e Mmdevapi.dll.</span><span class="sxs-lookup"><span data-stu-id="de820-119">The Core Audio APIs are implemented in the user-mode system components Audioses.dll and Mmdevapi.dll.</span></span> <span data-ttu-id="de820-120">Os aplicativos cliente não acessam os pontos de entrada nessas DLLs diretamente.</span><span class="sxs-lookup"><span data-stu-id="de820-120">Client applications do not access the entry points in these DLLs directly.</span></span> <span data-ttu-id="de820-121">Em vez disso, os clientes chamam a função **CoCreateInstance** ou **CoCreateInstanceEx** para obter a interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) do objeto de classe MMDeviceEnumerator.</span><span class="sxs-lookup"><span data-stu-id="de820-121">Instead, clients call the **CoCreateInstance** or **CoCreateInstanceEx** function to obtain the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface of the MMDeviceEnumerator class object.</span></span> <span data-ttu-id="de820-122">Esse objeto enumera os [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md) no sistema.</span><span class="sxs-lookup"><span data-stu-id="de820-122">This object enumerates the [audio endpoint devices](audio-endpoint-devices.md) in the system.</span></span> <span data-ttu-id="de820-123">A interface **IMMDeviceEnumerator** faz parte da API do MMDevice.</span><span class="sxs-lookup"><span data-stu-id="de820-123">The **IMMDeviceEnumerator** interface is part of the MMDevice API.</span></span> <span data-ttu-id="de820-124">A partir dessa interface, os clientes podem obter direta ou indiretamente as outras interfaces na API MMDevice, incluindo a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) .</span><span class="sxs-lookup"><span data-stu-id="de820-124">From this interface, clients can directly or indirectly obtain the other interfaces in the MMDevice API, including the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface.</span></span> <span data-ttu-id="de820-125">**IMMDevice** representa um dispositivo de ponto de extremidade de áudio específico.</span><span class="sxs-lookup"><span data-stu-id="de820-125">**IMMDevice** represents a particular audio endpoint device.</span></span> <span data-ttu-id="de820-126">Por meio do **IMMDevice**, os clientes podem obter direta ou indiretamente as interfaces específicas do dispositivo em WASAPI, a API do DeviceTopology e a API do EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="de820-126">Through **IMMDevice**, clients can directly or indirectly obtain the device-specific interfaces in WASAPI, the DeviceTopology API, and the EndpointVolume API.</span></span> <span data-ttu-id="de820-127">Para obter mais informações sobre **CoCreateInstance** e **CoCreateInstanceEx**, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="de820-127">For more information about **CoCreateInstance** and **CoCreateInstanceEx**, see the Windows SDK documentation.</span></span> <span data-ttu-id="de820-128">Para obter mais informações sobre como acessar as interfaces nas APIs de áudio principal, consulte [enumerando dispositivos de áudio](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="de820-128">For more information about accessing the interfaces in the Core Audio APIs, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="de820-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="de820-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de820-130">Sobre as APIs de áudio do Windows Core</span><span class="sxs-lookup"><span data-stu-id="de820-130">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



