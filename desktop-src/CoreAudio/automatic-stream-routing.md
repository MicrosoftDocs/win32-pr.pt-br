---
description: Este artigo descreve como atualizar uma implementação do WASAPI para tirar proveito do roteamento automático de fluxo.
ms.assetid: 718CBEB9-A7A0-4898-81B7-CBD76AFA3A06
title: Roteamento de fluxo automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a9848c5fd764ee49e485fc112c35c347a0f84d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920568"
---
# <a name="automatic-stream-routing"></a><span data-ttu-id="77acf-103">Roteamento de fluxo automático</span><span class="sxs-lookup"><span data-stu-id="77acf-103">Automatic Stream Routing</span></span>

<span data-ttu-id="77acf-104">Este artigo descreve como atualizar uma implementação do WASAPI para tirar proveito do roteamento automático de fluxo.</span><span class="sxs-lookup"><span data-stu-id="77acf-104">This article describes how to update a WASAPI implementation to take advantage of automatic stream routing.</span></span>

<span data-ttu-id="77acf-105">A partir do Windows 7, sempre que o dispositivo de áudio padrão for alterado, o fluxo de reprodução de áudio de um aplicativo será transferido diretamente do dispositivo de áudio padrão anterior para o novo dispositivo de áudio padrão.</span><span class="sxs-lookup"><span data-stu-id="77acf-105">Starting with Windows 7, whenever the default audio device changes, an app's audio playback stream is seamlessly transferred from the previous default audio device to the new default audio device .</span></span> <span data-ttu-id="77acf-106">Essa transferência ocorre automaticamente sem qualquer código de aplicativo adicional.</span><span class="sxs-lookup"><span data-stu-id="77acf-106">This transfer occurs automatically without any additional application code.</span></span> <span data-ttu-id="77acf-107">No entanto, antes do Windows 10, a versão 1607, os aplicativos que usaram a API de sessão de áudio do Windows (WASAPI) de baixo nível não podiam participar dessa funcionalidade de roteamento de fluxo automatizado.</span><span class="sxs-lookup"><span data-stu-id="77acf-107">However, prior to Windows 10, version 1607, apps that used the low-level Windows Audio Session API (WASAPI) could not participate in this automated stream routing functionality.</span></span> <span data-ttu-id="77acf-108">Aplicativos que usam WASAPI eram necessários para implementar sua própria forma de roteamento de fluxo, adicionando código adicional para detectar a chegada e a remoção de dispositivos de áudio e alternar o fluxo para esses dispositivos, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="77acf-108">Apps using WASAPI were required to implement their own form of stream routing by adding additional code to detect the arrival and removal of audio devices and switch the stream to those devices as appropriate.</span></span> <span data-ttu-id="77acf-109">Aplicativos que usam WASAPI que não implementaram seu próprio mecanismo de roteamento de fluxo na chegada ou remoção do dispositivo, fornecendo uma experiência do usuário menos do que o ideal.</span><span class="sxs-lookup"><span data-stu-id="77acf-109">Applications using WASAPI that did not implement their own stream routing mechanism on device arrival or removal risked providing a less than ideal user experience.</span></span>

<span data-ttu-id="77acf-110">A partir do Windows 10, versão 1607, os aplicativos que usam o WASAPI podem aproveitar o roteamento automático de fluxo.</span><span class="sxs-lookup"><span data-stu-id="77acf-110">Starting with the Windows 10, version 1607, apps that use WASAPI can take advantage of automatic stream routing.</span></span> <span data-ttu-id="77acf-111">Se seu aplicativo usar WASAPI, é altamente recomendável que você atualize seu aplicativo para aproveitar essa nova funcionalidade usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="77acf-111">If your application uses WASAPI it is highly recommended that you update your application to take advantage of this new capability using the following steps:</span></span>

1.  <span data-ttu-id="77acf-112">O Windows 10, versão 1607, define dois novos GUIDs que podem ser usados para ativar uma interface de renderização ou captura de áudio com roteamento automático de fluxo, [ \_ \_ processamento de áudio DEVINTERFACE](/windows/desktop/CoreAudio/devinterface-xxx-guids) e [ \_ \_ captura de áudio DEVINTERFACE](/windows/desktop/CoreAudio/devinterface-xxx-guids).</span><span class="sxs-lookup"><span data-stu-id="77acf-112">Windows 10, version 1607, defines two new GUIDs that can be used to activate an audio render or capture interface with automatic stream routing, [DEVINTERFACE\_AUDIO\_RENDER](/windows/desktop/CoreAudio/devinterface-xxx-guids) and [DEVINTERFACE\_AUDIO\_CAPTURE](/windows/desktop/CoreAudio/devinterface-xxx-guids).</span></span> <span data-ttu-id="77acf-113">Obtenha uma representação de cadeia de caracteres dessas GUIDs chamando [**StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid).</span><span class="sxs-lookup"><span data-stu-id="77acf-113">Get a string representation of these GUIDs by calling [**StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid).</span></span> <span data-ttu-id="77acf-114">O exemplo a seguir mostra essa chamada para o GUID de renderização de áudio.</span><span class="sxs-lookup"><span data-stu-id="77acf-114">The following example shows this call for the audio render GUID.</span></span>

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  <span data-ttu-id="77acf-115">Ative o ponto de extremidade de áudio passando a cadeia de caracteres do identificador para a função WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) .</span><span class="sxs-lookup"><span data-stu-id="77acf-115">Activate the audio endpoint by passing the identifier string to the WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) function.</span></span> <span data-ttu-id="77acf-116">O exemplo a seguir passa o identificador de renderização de áudio obtido na etapa 1:</span><span class="sxs-lookup"><span data-stu-id="77acf-116">The following example passes in the audio render identifier obtained in step 1:</span></span>

    ```C++
    //Activate the default audio interface
    ActivateAudioInterfaceAsync(audioRenderGuidString
                                __uuidof(IAudioClient),
                                NULL,
                                completionHandler.Get(),
                                operation.GetAddressOf()));
    ```

    

3.  <span data-ttu-id="77acf-117">Libere a memória alocada para manter o identificador do ponto de extremidade:</span><span class="sxs-lookup"><span data-stu-id="77acf-117">Free the memory allocated for holding the endpoint identifier:</span></span>

    ```C++
    CoTaskMemFree(audioRenderGuidString);  //free the string memory
    ```

    

<span data-ttu-id="77acf-118">Depois de modificar seu aplicativo para ativar a interface de áudio da maneira descrita acima, ele participará do recurso de roteamento de fluxo automático.</span><span class="sxs-lookup"><span data-stu-id="77acf-118">After you have modified your app to activate the audio interface in the manner described above, it will participate in the automatic stream routing feature.</span></span>

<span data-ttu-id="77acf-119">Para demonstrar o roteamento automático de fluxo, use um laptop ou Tablet equipado com alto-falantes internos para reproduzir áudio.</span><span class="sxs-lookup"><span data-stu-id="77acf-119">To demonstrate automatic stream routing, use a laptop or tablet equipped with internal speakers to play back audio.</span></span> <span data-ttu-id="77acf-120">Você deve ouvir o áudio passando pelos alto-falantes internos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77acf-120">You should hear the audio playing through the device's internal speakers.</span></span> <span data-ttu-id="77acf-121">Enquanto o áudio estiver em execução, conecte um par de fones de ouvido.</span><span class="sxs-lookup"><span data-stu-id="77acf-121">While audio is playing, connect a pair of headphones.</span></span> <span data-ttu-id="77acf-122">Agora você deve ouvir áudio passando pelos fones de ouvido.</span><span class="sxs-lookup"><span data-stu-id="77acf-122">You should now hear audio playing through the headphones.</span></span> <span data-ttu-id="77acf-123">Em seguida, desconecte os fones de ouvido e o áudio deve rotear automaticamente de volta para os alto-falantes internos.</span><span class="sxs-lookup"><span data-stu-id="77acf-123">Then, unplug the headphones and audio should automatically route back to the internal speakers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77acf-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77acf-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77acf-125">Roteamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="77acf-125">Stream Routing</span></span>](stream-routing.md)
</dt> <dt>

[<span data-ttu-id="77acf-126">**MediaDevice.GetDefaultAudioRenderId**</span><span class="sxs-lookup"><span data-stu-id="77acf-126">**MediaDevice.GetDefaultAudioRenderId**</span></span>](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[<span data-ttu-id="77acf-127">**MediaDevice.GetDefaultAudioCaptureId**</span><span class="sxs-lookup"><span data-stu-id="77acf-127">**MediaDevice.GetDefaultAudioCaptureId**</span></span>](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[<span data-ttu-id="77acf-128">**ActivateAudioInterfaceAsync**</span><span class="sxs-lookup"><span data-stu-id="77acf-128">**ActivateAudioInterfaceAsync**</span></span>](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
