---
description: No Windows 7, as APIs de plataforma de alto nível que usam APIs de áudio de núcleo como Media Foundation, DirectSound e APIs Wave, implementam o recurso de roteamento de fluxo manipulando a alternância de fluxo de um dispositivo existente para um novo ponto de extremidade de áudio padrão.
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: Obtendo o ponto de extremidade do dispositivo para roteamento de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed8c7546c2bd7437ed9705dc93c2a736bbb64e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826433"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a><span data-ttu-id="6b5e8-103">Obtendo o ponto de extremidade do dispositivo para roteamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="6b5e8-103">Getting the Device Endpoint for Stream Routing</span></span>

<span data-ttu-id="6b5e8-104">No Windows 7, as APIs de plataforma de alto nível que usam APIs de áudio de núcleo como Media Foundation, DirectSound e APIs Wave, implementam o recurso de roteamento de fluxo manipulando a alternância de fluxo de um dispositivo existente para um novo ponto de extremidade de áudio padrão.</span><span class="sxs-lookup"><span data-stu-id="6b5e8-104">In Windows 7, high-level platform APIs that use Core Audio APIs such as Media Foundation, DirectSound, and Wave APIs, implement the stream routing feature by handling stream switching from an existing device to a new default audio endpoint.</span></span> <span data-ttu-id="6b5e8-105">Aplicativos de mídia que usam essas APIs (por exemplo, um aplicativo ativando um objeto **IDirectSound** ou **IBaseFilter** em um objeto [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) ) usam o comportamento de roteamento de fluxo sem nenhuma modificação na origem.</span><span class="sxs-lookup"><span data-stu-id="6b5e8-105">Media applications that use these APIs (for example, an application activating an **IDirectSound** or **IBaseFilter** object on an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) object) use the stream routing behavior without any modifications to the source.</span></span>

<span data-ttu-id="6b5e8-106">As APIs de alto nível implementam o roteamento de fluxo para o ponto de extremidade do dispositivo que é obtido por meio de [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span><span class="sxs-lookup"><span data-stu-id="6b5e8-106">The high-level APIs implement stream routing for the device endpoint that is obtained through [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="6b5e8-107">Se um aplicativo transmitir para o dispositivo padrão, o recurso de roteamento de fluxo funcionará conforme definido.</span><span class="sxs-lookup"><span data-stu-id="6b5e8-107">If an application streams to the default device, the stream routing feature operates as defined.</span></span> <span data-ttu-id="6b5e8-108">Os fluxos não serão alternados para o novo dispositivo se ele for recuperado por qualquer outro mecanismo, mesmo se for o mesmo que o dispositivo padrão.</span><span class="sxs-lookup"><span data-stu-id="6b5e8-108">Streams are not switched to the new device if it is retrieved by any other mechanism even if it is the same as the default device.</span></span>

<span data-ttu-id="6b5e8-109">Um aplicativo de mídia que usa APIs de áudio de núcleo diretamente (cliente WASAPI) pode fornecer uma implementação de roteamento de fluxo personalizada para qualquer dispositivo de renderização ou de captura.</span><span class="sxs-lookup"><span data-stu-id="6b5e8-109">A media application that uses Core Audio APIs directly (WASAPI client) can provide a custom stream routing implementation for any rendering or capture device.</span></span> <span data-ttu-id="6b5e8-110">Um cliente WASAPI pode replicar o implemetation fornecido pelas APIs de alto nível restringindo-o a fluxos que são abertos em dispositivos que são definidos como o dispositivo padrão.</span><span class="sxs-lookup"><span data-stu-id="6b5e8-110">A WASAPI client can replicate the implemetation provided by the high-level APIs by restricting it to streams that are opened on devices that are set as the default device.</span></span> <span data-ttu-id="6b5e8-111">Para obter uma referência ao ponto de extremidade do dispositivo padrão, o cliente deve chamar [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span><span class="sxs-lookup"><span data-stu-id="6b5e8-111">To get a reference to the default device's endpoint, the client must call [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="6b5e8-112">Nesta chamada, o cliente deve indicar se ele requer um ponteiro para o dispositivo padrão de renderização ou o dispositivo padrão de captura especificando o parâmetro *Dataflow* .</span><span class="sxs-lookup"><span data-stu-id="6b5e8-112">In this call, the client must indicate whether it requires a pointer to the rendering default device or the capture default device by specifying the *dataFlow* parameter.</span></span> <span data-ttu-id="6b5e8-113">O cliente também deve especificar a função apropriada para o ponto de extremidade no atributo **ERole** (**eConsole** ou **eCommunications**).</span><span class="sxs-lookup"><span data-stu-id="6b5e8-113">The client must also specify the appropriate role for the endpoint in the **ERole** attribute (**eConsole** or **eCommunications**).</span></span> <span data-ttu-id="6b5e8-114">Não use **eMultimedia**.</span><span class="sxs-lookup"><span data-stu-id="6b5e8-114">Do not use **eMultimedia**.</span></span>

<span data-ttu-id="6b5e8-115">Se o aplicativo flui para qualquer outro dispositivo, o aplicativo pode obter o dispositivo especificando uma cadeia de caracteres de ID de ponto de extremidade (chamando [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).</span><span class="sxs-lookup"><span data-stu-id="6b5e8-115">If the application streams to any other device, the application can get the device by specifying an endpoint ID string (by calling [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).</span></span>

<span data-ttu-id="6b5e8-116">Depois que o dispositivo é identificado, o cliente WASAPI pode fornecer a implementação para o roteamento de fluxo manipulando as notificações de sessão de dispositivo e de áudio enviadas para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b5e8-116">After the device is identified, the WASAPI client can provide the implementation for stream routing by handling the device and audio session notifications sent for the device.</span></span> <span data-ttu-id="6b5e8-117">Para obter mais informações sobre essas notificações, consulte [notificações relevantes para o roteamento de fluxo](relevant-device-notifications-for-stream-routing.md).</span><span class="sxs-lookup"><span data-stu-id="6b5e8-117">For more information about these notifications, see [Relevant Notifications for Stream Routing](relevant-device-notifications-for-stream-routing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b5e8-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b5e8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b5e8-119">Sobre a API do MMDevice</span><span class="sxs-lookup"><span data-stu-id="6b5e8-119">About MMDevice API</span></span>](mmdevice-api.md)
</dt> <dt>

[<span data-ttu-id="6b5e8-120">Sobre o WASAPI</span><span class="sxs-lookup"><span data-stu-id="6b5e8-120">About WASAPI</span></span>](wasapi.md)
</dt> <dt>

[<span data-ttu-id="6b5e8-121">Roteamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="6b5e8-121">Stream Routing</span></span>](stream-routing.md)
</dt> </dl>

 

 



