---
title: Implementando um enumerador de ponto de extremidade de áudio personalizado
description: A partir do Windows Server 2008 R2, você pode implementar um enumerador personalizado de ponto de extremidade de áudio remoto como parte de um provedor de protocolo Área de Trabalho Remota.
ms.assetid: 684bd62e-1e28-4330-a3c5-6bce684d652d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435ab2a572169f20a7f8f9db194449be5361e409
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "105783342"
---
# <a name="implementing-a-custom-audio-endpoint-enumerator"></a><span data-ttu-id="2f004-103">Implementando um enumerador de ponto de extremidade de áudio personalizado</span><span class="sxs-lookup"><span data-stu-id="2f004-103">Implementing a Custom Audio Endpoint Enumerator</span></span>

<span data-ttu-id="2f004-104">A partir do Windows Server 2008 R2, você pode implementar um enumerador personalizado de ponto de extremidade de áudio remoto como parte de um provedor de protocolo Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="2f004-104">Beginning with Windows Server 2008 R2, you can implement a custom remote audio endpoint enumerator as part of a Remote Desktop protocol provider.</span></span> <span data-ttu-id="2f004-105">Um provedor de protocolo Área de Trabalho Remota pode usar um enumerador de ponto de extremidade de áudio personalizado para recuperar uma coleção de pontos de extremidades de áudio que têm um conjunto específico de recursos.</span><span class="sxs-lookup"><span data-stu-id="2f004-105">A Remote Desktop protocol provider can use a custom audio endpoint enumerator to retrieve a collection of audio endpoints that have a specific set of capabilities.</span></span>

<span data-ttu-id="2f004-106">**Para implementar um enumerador personalizado de ponto de extremidade de áudio remoto**</span><span class="sxs-lookup"><span data-stu-id="2f004-106">**To implement a custom remote audio endpoint enumerator**</span></span>

1.  <span data-ttu-id="2f004-107">Sua solução de enumerador de ponto de extremidade personalizado deve implementar quatro tipos principais de objetos: objetos de enumerador de dispositivo, objetos de coleção de dispositivos, objetos de dispositivo e objetos de armazenamento de propriedades.</span><span class="sxs-lookup"><span data-stu-id="2f004-107">Your custom endpoint enumerator solution should implement four main types of objects: device enumerator objects, device collection objects, device objects, and property store objects.</span></span>

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="2f004-108">Tipo de Objeto</span><span class="sxs-lookup"><span data-stu-id="2f004-108">Object type</span></span></th>
    <th><span data-ttu-id="2f004-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f004-109">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="2f004-110">Objeto enumerador de dispositivo</span><span class="sxs-lookup"><span data-stu-id="2f004-110">Device enumerator object</span></span><br/></td>
    <td><span data-ttu-id="2f004-111">Um objeto de enumerador de dispositivo fornece a funcionalidade de enumerador de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="2f004-111">A device enumerator object provides the endpoint enumerator functionality.</span></span> <span data-ttu-id="2f004-112">Ele expõe métodos que retornam um ponto de extremidade padrão e coleções especificadas de pontos de extremidades.</span><span class="sxs-lookup"><span data-stu-id="2f004-112">It exposes methods that return a default endpoint and specified collections of endpoints.</span></span> <span data-ttu-id="2f004-113">Por exemplo, dependendo dos critérios especificados, o enumerador pode retornar pontos de extremidade de comunicação, pontos de extremidade de reprodução ou capturar pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="2f004-113">For example, depending on the criteria specified, the enumerator can return communication endpoints, playback endpoints, or capture endpoints.</span></span> <span data-ttu-id="2f004-114">O objeto enumerador de dispositivo deve implementar a interface <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2f004-114">The device enumerator object must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator</strong></a> interface.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="2f004-115">Objeto de coleção de dispositivos</span><span class="sxs-lookup"><span data-stu-id="2f004-115">Device collection object</span></span><br/></td>
    <td><span data-ttu-id="2f004-116">Um objeto de coleção de dispositivos representa uma coleção de dispositivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="2f004-116">A device collection object represents a collection of audio devices.</span></span> <span data-ttu-id="2f004-117">Ele deve implementar a interface <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2f004-117">It must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection</strong></a> interface.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="2f004-118">Objeto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="2f004-118">Device object</span></span><br/></td>
    <td><span data-ttu-id="2f004-119">Um objeto de dispositivo representa um dispositivo de áudio específico.</span><span class="sxs-lookup"><span data-stu-id="2f004-119">A device object represents a particular audio device.</span></span> <span data-ttu-id="2f004-120">Ele fornece acesso ao armazenamento de propriedades do dispositivo de áudio e expõe as interfaces de reprodução e de captura de áudio disponíveis no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f004-120">It provides access to the audio device's property store and exposes the audio playback and capture interfaces available on the device.</span></span> <span data-ttu-id="2f004-121">O objeto de dispositivo deve implementar as interfaces <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>IMMDevice</strong></a> e <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2f004-121">The device object must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>IMMDevice</strong></a> and <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> interfaces.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="2f004-122">Objeto de repositório de propriedades</span><span class="sxs-lookup"><span data-stu-id="2f004-122">Property store object</span></span><br/></td>
    <td><span data-ttu-id="2f004-123">Um objeto de repositório de propriedades expõe as propriedades associadas a um dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="2f004-123">A property store object exposes the properties associated with an audio device.</span></span> <span data-ttu-id="2f004-124">Algumas dessas propriedades são usadas pelo sistema, mas os aplicativos também podem armazenar propriedades arbitrárias com o ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="2f004-124">Some of these properties are used by the system, but applications can store arbitrary properties with the audio endpoint as well.</span></span><br/> <span data-ttu-id="2f004-125">Todos os dispositivos de áudio têm as três propriedades a seguir:</span><span class="sxs-lookup"><span data-stu-id="2f004-125">All audio devices have the following three properties:</span></span><br/>
    <ul>
    <li><span data-ttu-id="2f004-126"><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></span><span class="sxs-lookup"><span data-stu-id="2f004-126"><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></span></span></li>
    <li><span data-ttu-id="2f004-127"><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></span><span class="sxs-lookup"><span data-stu-id="2f004-127"><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></span></span></li>
    <li><span data-ttu-id="2f004-128"><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></span><span class="sxs-lookup"><span data-stu-id="2f004-128"><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></span></span></li>
    </ul>
<span data-ttu-id="2f004-129">O objeto de repositório de propriedades deve implementar a interface <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> .</span><span class="sxs-lookup"><span data-stu-id="2f004-129">The property store object must implement the <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface.</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="2f004-130">O enumerador de ponto de extremidade personalizado deve ser implementado em uma DLL que pode ser carregada no sistema de áudio e em outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2f004-130">The custom endpoint enumerator must be implemented in a DLL that can be loaded into the audio system and other applications.</span></span> <span data-ttu-id="2f004-131">A DLL deve ser assinada para que processos seguros possam carregá-lo.</span><span class="sxs-lookup"><span data-stu-id="2f004-131">The DLL must be signed so that secure processes can load it.</span></span> <span data-ttu-id="2f004-132">A DLL deve implementar e exportar a função [**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md) , que atua como um ponto de entrada para o enumerador de ponto de extremidade personalizado.</span><span class="sxs-lookup"><span data-stu-id="2f004-132">The DLL must implement and export the [**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md) function, which acts as an entry point to the custom endpoint enumerator.</span></span>

<span data-ttu-id="2f004-133">O serviço de Serviços de Área de Trabalho Remota chama o método [**queryproperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) e define o parâmetro *QueryType* como **WTS \_ Query \_ AUDIOENUM \_ dll** para recuperar o nome do objeto enumerador.</span><span class="sxs-lookup"><span data-stu-id="2f004-133">The Remote Desktop Services service calls the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) method and sets the *QueryType* parameter to **WTS\_QUERY\_AUDIOENUM\_DLL** to retrieve the name of the enumerator object.</span></span>

<span data-ttu-id="2f004-134">Os objetos de enumerador personalizados usam interfaces semelhantes a COM e um mecanismo de contagem de referência semelhante a, mas não são objetos COM verdadeiros.</span><span class="sxs-lookup"><span data-stu-id="2f004-134">Custom enumerator objects use COM-like interfaces and a COM-like reference counting mechanism, but they are not true COM objects.</span></span> <span data-ttu-id="2f004-135">O enumerador de ponto de extremidade personalizado deve ter a capacidade de trabalhar com interfaces de áudio herdadas usadas por aplicativos que não dão suporte a COM.</span><span class="sxs-lookup"><span data-stu-id="2f004-135">The custom endpoint enumerator must have the ability to work with legacy audio interfaces used by applications that do not support COM.</span></span> <span data-ttu-id="2f004-136">Por esse motivo, o enumerador de ponto de extremidade personalizado não deve depender do mecanismo de gerenciamento do ciclo de vida do COM.</span><span class="sxs-lookup"><span data-stu-id="2f004-136">For this reason, the custom endpoint enumerator must not rely on COM's life cycle management mechanism.</span></span> <span data-ttu-id="2f004-137">Os consumidores do enumerador de ponto de extremidade de áudio, como MMDevAPI.dll, carregam a DLL do enumerador de ponto de extremidade personalizado quando exigido pelos aplicativos do usuário e não descarregam o enumerador, enquanto o enumerador mantém uma referência a um objeto de enumerador de dispositivo, objeto de coleção de dispositivos, objeto de dispositivo ou objeto de repositório de propriedades.</span><span class="sxs-lookup"><span data-stu-id="2f004-137">Consumers of your audio endpoint enumerator, such as MMDevAPI.dll, load the custom endpoint enumerator DLL when required by user applications, and they will not unload the enumerator while the enumerator holds a reference to a device enumerator object, device collection object, device object, or property store object.</span></span> <span data-ttu-id="2f004-138">No entanto, não é possível que esses consumidores acompanhem referências a outros tipos de objetos pertencentes ao enumerador de ponto de extremidade personalizado.</span><span class="sxs-lookup"><span data-stu-id="2f004-138">It is not possible, however, for these consumers to track references to other types of objects owned by the custom endpoint enumerator.</span></span> <span data-ttu-id="2f004-139">Da mesma forma, recomendamos que seu enumerador de ponto de extremidade personalizado não crie nenhum objeto que possa sobreviver além esses quatro tipos de objetos.</span><span class="sxs-lookup"><span data-stu-id="2f004-139">Accordingly, we recommend that your custom endpoint enumerator not create any objects that could outlive these four types of objects.</span></span>

## <a name="to-implement-a-custom-audio-endpoint"></a><span data-ttu-id="2f004-140">Para implementar um ponto de extremidade de áudio personalizado</span><span class="sxs-lookup"><span data-stu-id="2f004-140">To implement a custom audio endpoint</span></span>

<span data-ttu-id="2f004-141">Para implementar um enumerador de dispositivo de áudio personalizado, você deve implementar um ponto de extremidade de áudio personalizado.</span><span class="sxs-lookup"><span data-stu-id="2f004-141">To implement a custom audio device enumerator, you must implement a custom audio endpoint.</span></span> <span data-ttu-id="2f004-142">A maneira como os dispositivos de áudio personalizados são vinculados é usando as duas instruções a seguir:</span><span class="sxs-lookup"><span data-stu-id="2f004-142">The way that your custom audio devices are linked is by using the following two statements:</span></span>

-   `IMMDevice::Activate(IAudioOutputEndpointRT)`
-   `IMMDevice::Activate(IAudioInputEndpointRT)`

<span data-ttu-id="2f004-143">Não esperamos que você implemente a lista completa de [**IMMDevice:: Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) interfaces no seu enumerador de dispositivo de áudio personalizado.</span><span class="sxs-lookup"><span data-stu-id="2f004-143">We do not expect you to implement the full list of [**IMMDevice::Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) interfaces in your custom audio device enumerator.</span></span> <span data-ttu-id="2f004-144">Em vez disso, você deve implementar [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) e [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span><span class="sxs-lookup"><span data-stu-id="2f004-144">Instead, you should implement [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) and [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span></span> <span data-ttu-id="2f004-145">Opcionalmente, você pode implementar mais alguns, como [**IAudioEndpointVolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume).</span><span class="sxs-lookup"><span data-stu-id="2f004-145">You can optionally implement a few more, such as [**IAudioEndpointVolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume).</span></span> <span data-ttu-id="2f004-146">Para qualquer interface que você não implementar, você deve retornar **E \_ nointerface** (você deve usar esse código de falha específico).</span><span class="sxs-lookup"><span data-stu-id="2f004-146">For any interface you do not implement, you should return **E\_NOINTERFACE** (you must use this specific failure code).</span></span> <span data-ttu-id="2f004-147">Em seguida, o Windows retornará a uma implementação de estoque da interface (por exemplo, [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).</span><span class="sxs-lookup"><span data-stu-id="2f004-147">Windows will then fall back to a stock implementation of the interface (for example, [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).</span></span>

<span data-ttu-id="2f004-148">Para obter mais documentação de referência sobre como implementar e registrar pontos de extremidade de áudio, consulte [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span><span class="sxs-lookup"><span data-stu-id="2f004-148">For additional reference documentation about how to implement and register audio endpoints, see [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span></span> <span data-ttu-id="2f004-149">Para um diagrama que mostra como o WASAPI funciona, consulte [componentes de áudio do modo de usuário](/windows/desktop/CoreAudio/user-mode-audio-components).</span><span class="sxs-lookup"><span data-stu-id="2f004-149">For a diagram that shows how WASAPI works, see [User-Mode Audio Components](/windows/desktop/CoreAudio/user-mode-audio-components).</span></span> <span data-ttu-id="2f004-150">Observe que todo o áudio do modo de usuário é novo, começando com o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2f004-150">Note that all of user-mode audio is new beginning with Windows Server 2008.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f004-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f004-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f004-152">Criando um provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="2f004-152">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dt>

[<span data-ttu-id="2f004-153">**GetTSAudioEndpointEnumeratorForSession**</span><span class="sxs-lookup"><span data-stu-id="2f004-153">**GetTSAudioEndpointEnumeratorForSession**</span></span>](gettsaudioendpointenumeratorforsession.md)
</dt> <dt>

[<span data-ttu-id="2f004-154">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="2f004-154">**IMMDevice**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[<span data-ttu-id="2f004-155">**IMMDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="2f004-155">**IMMDeviceCollection**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
</dt> <dt>

[<span data-ttu-id="2f004-156">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="2f004-156">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[<span data-ttu-id="2f004-157">**IMMEndpoint**</span><span class="sxs-lookup"><span data-stu-id="2f004-157">**IMMEndpoint**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint)
</dt> <dt>

[<span data-ttu-id="2f004-158">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="2f004-158">IPropertyStore</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> </dl>