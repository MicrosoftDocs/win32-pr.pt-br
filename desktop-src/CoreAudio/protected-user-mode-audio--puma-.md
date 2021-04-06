---
description: O Windows Vista introduziu o áudio do modo de usuário protegido (PUMA), o mecanismo de áudio do modo de usuário no ambiente protegido (PE) que fornece um ambiente mais seguro para processamento e renderização de áudio.
ms.assetid: 27a50026-9e48-48b1-9249-7528a97333c9
title: Áudio do modo de usuário protegido (PUMA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233dc82109feb66472e66e4235031696937d70d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826613"
---
# <a name="protected-user-mode-audio-puma"></a><span data-ttu-id="9dc5a-103">Áudio do modo de usuário protegido (PUMA)</span><span class="sxs-lookup"><span data-stu-id="9dc5a-103">Protected User Mode Audio (PUMA)</span></span>

<span data-ttu-id="9dc5a-104">O Windows Vista introduziu o áudio do modo de usuário protegido (PUMA), o mecanismo de áudio do modo de usuário no ambiente protegido (PE) que fornece um ambiente mais seguro para processamento e renderização de áudio.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-104">Windows Vista introduced Protected User Mode Audio (PUMA), the user-mode audio engine in the Protected Environment (PE) that provides a safer environment for audio processing and rendering.</span></span> <span data-ttu-id="9dc5a-105">Ele permite que apenas as saídas de áudio aceitáveis sejam habilitadas e garante que as saídas sejam desabilitadas de forma confiável.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-105">It allows only the acceptable audio outputs to be enabled and ensures that the outputs are disabled reliably.</span></span> <span data-ttu-id="9dc5a-106">Para obter mais informações sobre PUMA, consulte [saída proteção de conteúdo e Windows Vista](https://download.microsoft.com/download/5/D/6/5D6EAF2B-7DDF-476B-93DC-7CF0072878E6/output_protect.doc).</span><span class="sxs-lookup"><span data-stu-id="9dc5a-106">For more information about PUMA, see [Output Content Protection and Windows Vista](https://download.microsoft.com/download/5/D/6/5D6EAF2B-7DDF-476B-93DC-7CF0072878E6/output_protect.doc).</span></span>

<span data-ttu-id="9dc5a-107">O PUMA foi atualizado para o Windows 7 para fornecer os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="9dc5a-107">PUMA has been updated for Windows 7 to provide the following features:</span></span>

-   <span data-ttu-id="9dc5a-108">Definir bits SCMS (sistema de gerenciamento de cópia serial) em pontos de extremidade S/PDIF e bits de Proteção de Conteúdo Digital de largura de banda alta (HDCP) em pontos de extremidade de HDMI (High-Definition Multimedia Interface).</span><span class="sxs-lookup"><span data-stu-id="9dc5a-108">Setting Serial Copying Management System (SCMS) bits on S/PDIF endpoints and High-bandwidth Digital Content Protection (HDCP) bits on High-Definition Multimedia Interface (HDMI) endpoints.</span></span>
-   <span data-ttu-id="9dc5a-109">Habilitando controles de proteção SCMS e HDMI fora de um ambiente protegido (PE).</span><span class="sxs-lookup"><span data-stu-id="9dc5a-109">Enabling SCMS and HDMI protection controls outside of a Protected Environment (PE).</span></span>

## <a name="drm-protection-in-audio-drivers"></a><span data-ttu-id="9dc5a-110">Proteção de DRM em drivers de áudio</span><span class="sxs-lookup"><span data-stu-id="9dc5a-110">DRM Protection in Audio Drivers</span></span>

<span data-ttu-id="9dc5a-111">O DRM (Rights Management digital) fornece a capacidade de empacotar dados de mídia em um contêiner seguro e anexar regras de uso ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-111">Digital Rights Management (DRM) provides the ability to package media data in a secure container and attach usage rules to the content.</span></span> <span data-ttu-id="9dc5a-112">Por exemplo, o provedor de conteúdo pode usar a **proteção de cópia** ou a **saída digital desabilitar** para desabilitar cópias digitais diretas ou a transmissão do sistema de PC.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-112">For example, the content provider might use **Copy Protection** or **Digital Output Disable** to disable direct digital copies or transmission out of the PC system.</span></span>

<span data-ttu-id="9dc5a-113">A pilha de áudio em determinados produtos da Microsoft oferece suporte a DRM implementando as regras de uso que regem a reprodução do conteúdo de áudio.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-113">The audio stack in certain Microsoft products supports DRM by implementing the usage rules that govern playback of the audio content.</span></span> <span data-ttu-id="9dc5a-114">Para reproduzir o conteúdo protegido, o driver de áudio subjacente deve ser um *Driver confiável*; ou seja, o driver deve ser certificado pelo logotipo para DRMLevel 1300.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-114">To play the protected content, the underlying audio driver must be a *trusted driver*; that is, the driver must be logo-certified for DRMLevel 1300.</span></span> <span data-ttu-id="9dc5a-115">Para obter informações sobre como desenvolver drivers confiáveis, você pode usar interfaces que são definidas no Windows 2000 Driver Development Kit ("DDK") ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-115">For information about developing trusted drivers, you can use interfaces that are defined in the Windows 2000 Driver Development Kit ("DDK") or later.</span></span> <span data-ttu-id="9dc5a-116">Os drivers desenvolvidos com o DDK implementarão as interfaces necessárias para DRM.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-116">Drivers developed with the DDK will implement the necessary interfaces to DRM.</span></span> <span data-ttu-id="9dc5a-117">Para obter mais informações, consulte [Digital Rights Management](/windows-hardware/drivers/audio/digital-rights-management).</span><span class="sxs-lookup"><span data-stu-id="9dc5a-117">For more information, see [Digital Rights Management](/windows-hardware/drivers/audio/digital-rights-management).</span></span>

<span data-ttu-id="9dc5a-118">Para renderizar o conteúdo protegido, o driver confiável deve verificar se a **proteção de cópia** e a **desabilitação da saída digital** estão definidas no conteúdo que flui pela pilha de áudio e responder às configurações de acordo.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-118">To render the protected content, the trusted driver must check whether **Copy Protection** and **Digital Output Disable** are set on the content flowing through the audio stack, and respond to the settings accordingly.</span></span>

### <a name="copy-protection-rule"></a><span data-ttu-id="9dc5a-119">Copiar regra de proteção</span><span class="sxs-lookup"><span data-stu-id="9dc5a-119">Copy Protection Rule</span></span>

<span data-ttu-id="9dc5a-120">A **proteção de cópia** indica que cópias digitais diretas não são permitidas no sistema.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-120">**Copy Protection** indicates that direct digital copies are not allowed on the system.</span></span> <span data-ttu-id="9dc5a-121">O anexo B para o contrato de teste de WHQL foi atualizado para refletir as novas expectativas e os requisitos de um driver quando a **proteção de cópia** está definida no conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-121">Exhibit B to the WHQL Testing Agreement has been updated to reflect the new expectations and requirements of a driver when **Copy Protection** is set on the content.</span></span> <span data-ttu-id="9dc5a-122">Para o Windows 7, o driver de classe de áudio HD interno está em conformidade com os requisitos mais recentes.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-122">For Windows 7, the built-in HD audio class driver complies with the latest requirements.</span></span>

<span data-ttu-id="9dc5a-123">Além de garantir que o conteúdo não tenha permissão para passar para outro componente ou ser armazenado em qualquer mídia de armazenamento não volátil que não seja autenticada pelo sistema DRM, o driver de áudio executa as seguintes tarefas quando a **proteção de cópia** é definida:</span><span class="sxs-lookup"><span data-stu-id="9dc5a-123">In addition to ensuring that content is not allowed to pass to another component or be stored on any nonvolatile storage medium that is not authenticated by the DRM system, the audio driver performs the following tasks when **Copy Protection** is set:</span></span>

-   <span data-ttu-id="9dc5a-124">O driver habilita HDCP em pontos de extremidade HDMI.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-124">The driver enables HDCP on HDMI endpoints.</span></span>
-   <span data-ttu-id="9dc5a-125">Para interfaces S/PDIF, o driver valida que a combinação dos bits de código L, CP e Category indica um estado SCMS de "Copy Never", conforme definido no IEC 60958.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-125">For S/PDIF interfaces, the driver validates that the combination of L, Cp and Category Code bits indicates an SCMS state of "Copy Never", as defined in IEC 60958.</span></span>
-   <span data-ttu-id="9dc5a-126">O L bit é definido como 0 e o código da categoria é definido como "mixer de sinal digital".</span><span class="sxs-lookup"><span data-stu-id="9dc5a-126">The L bit is set to 0 and the Category Code is set to "Digital Signal Mixer".</span></span>

<span data-ttu-id="9dc5a-127">A estrutura **DRMRIGHTS** , usada por drivers de áudio confiáveis, especifica os direitos de conteúdo de DRM atribuídos a um PIN de áudio KS ou a um objeto de fluxo do driver de classe de porta.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-127">The **DRMRIGHTS** structure, used by trusted audio drivers, specifies the DRM content rights assigned to a KS audio pin or to a port-class driver's stream object.</span></span> <span data-ttu-id="9dc5a-128">O membro **CopyProtect** indica se a **proteção de cópia** está definida no conteúdo de áudio.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-128">The **CopyProtect** member indicates whether **Copy Protection** is set on the audio content.</span></span>

<span data-ttu-id="9dc5a-129">Para o Windows 7, o uso de **CopyProtect** é mais estrito.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-129">For Windows 7, the use of **CopyProtect** is stricter.</span></span> <span data-ttu-id="9dc5a-130">O driver garante que os controles de proteção sejam definidos nas interfaces de áudio, HDCP está definido para saída de HDMI e SCMS é definido para a saída S/PDIF definindo o estado como "Copy Never".</span><span class="sxs-lookup"><span data-stu-id="9dc5a-130">The driver ensures that the protection controls are set on the audio interfaces, HDCP is set for HDMI output, and SCMS is set for S/PDIF output by setting the state to "Copy Never".</span></span>

### <a name="digital-output-disable-rule"></a><span data-ttu-id="9dc5a-131">Regra de desabilitação de saída digital</span><span class="sxs-lookup"><span data-stu-id="9dc5a-131">Digital Output Disable Rule</span></span>

<span data-ttu-id="9dc5a-132">A **desabilitação da saída digital** indica que o conteúdo não pode ser transmitido do sistema.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-132">**Digital Output Disable** indicates that the content is not allowed to be transmitted out of the system.</span></span> <span data-ttu-id="9dc5a-133">No Windows 7, o driver interno de classe de áudio HD responde a essa configuração habilitando HDCP em pontos de extremidade HDMI.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-133">In Windows 7, the built-in HD audio class driver responds to this setting by enabling HDCP on HDMI endpoints.</span></span> <span data-ttu-id="9dc5a-134">Isso é semelhante à resposta do driver para a configuração de **proteção de cópia** .</span><span class="sxs-lookup"><span data-stu-id="9dc5a-134">This is similar to the driver's response to the **Copy Protection** setting.</span></span>

## <a name="enabling-content-protection-mechanisms-outside-of-a-protected-environment"></a><span data-ttu-id="9dc5a-135">Habilitando mecanismos de proteção de conteúdo fora de um ambiente protegido</span><span class="sxs-lookup"><span data-stu-id="9dc5a-135">Enabling Content-Protection Mechanisms Outside of a Protected Environment</span></span>

<span data-ttu-id="9dc5a-136">O PUMA reside em um processo separado no PE (ambiente protegido).</span><span class="sxs-lookup"><span data-stu-id="9dc5a-136">PUMA resides in a separate process in the Protected Environment (PE).</span></span> <span data-ttu-id="9dc5a-137">No Windows Vista, para usar os controles de proteção de conteúdo de áudio oferecidos pelo PUMA, um aplicativo de mídia deve estar em um PE.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-137">In Windows Vista, to use the audio content protection controls offered by PUMA, a media application must be in a PE.</span></span> <span data-ttu-id="9dc5a-138">Como somente as APIs Media Foundation podem interagir com um PE, os controles de proteção de conteúdo são limitados a aplicativos que usam APIs Media Foundation para transmitir conteúdo de áudio.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-138">Because only Media Foundation APIs can interact with a PE, the content protection controls are limited to applications using Media Foundation APIs to stream audio content.</span></span>

<span data-ttu-id="9dc5a-139">No Windows 7, qualquer aplicativo pode acessar os controles de proteção de conteúdo fornecidos pela PUMA output Trust Authority (OTA), independentemente de estarem em um PE ou usando Media Foundation APIs para reprodução de áudio.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-139">In Windows 7, any application can access the content protection controls provided by the PUMA Output Trust Authority (OTA), regardless of whether they are in a PE or using Media Foundation APIs for audio playback.</span></span>

## <a name="implementation-instructions"></a><span data-ttu-id="9dc5a-140">Instruções de implementação</span><span class="sxs-lookup"><span data-stu-id="9dc5a-140">Implementation Instructions</span></span>

<span data-ttu-id="9dc5a-141">As etapas a seguir são necessárias para que um aplicativo de áudio controle a proteção de conteúdo SCMS ou HDCP em um ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-141">The following steps are required for an audio application to control SCMS or HDCP content protection on an audio endpoint.</span></span> <span data-ttu-id="9dc5a-142">As APIs de áudio com suporte são DirectShow, DirectSound e WASAPI.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-142">Supported Audio APIs are DirectShow, DirectSound, and WASAPI.</span></span>

<span data-ttu-id="9dc5a-143">Este código de exemplo usa as seguintes interfaces.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-143">This example code uses the following interfaces.</span></span>

-   [<span data-ttu-id="9dc5a-144">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="9dc5a-144">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [<span data-ttu-id="9dc5a-145">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="9dc5a-145">**IMMDevice**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [<span data-ttu-id="9dc5a-146">**IAudioClient**</span><span class="sxs-lookup"><span data-stu-id="9dc5a-146">**IAudioClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)
-   [<span data-ttu-id="9dc5a-147">**IMMDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="9dc5a-147">**IMMDeviceCollection**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
-   [<span data-ttu-id="9dc5a-148">**IMFTrustedOutput**</span><span class="sxs-lookup"><span data-stu-id="9dc5a-148">**IMFTrustedOutput**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput)
-   [<span data-ttu-id="9dc5a-149">**IMFOutputPolicy**</span><span class="sxs-lookup"><span data-stu-id="9dc5a-149">**IMFOutputPolicy**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy)

<span data-ttu-id="9dc5a-150">O aplicativo de mídia deve executar as seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-150">The media application must perform the following tasks.</span></span>

1.  <span data-ttu-id="9dc5a-151">Configure o ambiente de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-151">Set up the development environment.</span></span>
    -   <span data-ttu-id="9dc5a-152">Faça referência às interfaces necessárias, inclua os cabeçalhos mostrados no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-152">Reference the required interfaces, include the headers shown in the following code.</span></span>
        ```cpp
        #include <MMdeviceapi.h>        // Device endpoint definitions
        #include <Mfidl.h>              // OTA interface definitions
        ```

        

    -   <span data-ttu-id="9dc5a-153">Link para o Mfuuid. lib para usar as interfaces OTA.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-153">Link to the Mfuuid.lib to use the OTA interfaces.</span></span>
    -   <span data-ttu-id="9dc5a-154">Desabilite o depurador de kernel e o verificador de driver para evitar erros de verificação de autenticação.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-154">Disable the kernel debugger and driver verifier to avoid any authentication checking errors.</span></span>
2.  <span data-ttu-id="9dc5a-155">Enumera todos os pontos de extremidade no sistema e selecione o ponto de extremidade de destino na coleção de pontos de extremidades, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-155">Enumerate all endpoints in the system and select the target endpoint from the endpoint collection, as shown in the following code.</span></span> <span data-ttu-id="9dc5a-156">Para obter mais informações sobre como enumerar dispositivos, consulte [enumerando dispositivos de áudio](/previous-versions//ms678716(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9dc5a-156">For more information about enumerating devices, see [Enumerating Audio Devices](/previous-versions//ms678716(v=vs.85)).</span></span>
    ```cpp
    BOOL IsDigitalEndpoint(IMMDevice *pDevice)
    {
       PROPVARIANT         var;
       IPropertyStore      *pProperties = NULL;
       EndpointFormFactor  formfactor;
       BOOL                bResult = FALSE;
       HRESULT             hr = S_OK;
       PropVariantInit(&var);
       // Open endpoint properties
       hr = pDevice->OpenPropertyStore(STGM_READ, &pProperties);
       IF_FAILED_JUMP(hr, Exit);

       // get form factor 
       hr = pProperties->GetValue(PKEY_AudioEndpoint_FormFactor, &var);
       IF_FAILED_JUMP(hr, Exit);
       formfactor = (EndpointFormFactor)var.uiVal;
       // DigitalAudioDisplayDevice is defined same as HDMI formfactor
       if ((SPDIF == formfactor) || (DigitalAudioDisplayDevice == formfactor))
       {
           bResult = TRUE;
       }

    Exit:
       PropVariantClear(&var);
       SAFE_RELEASE(pProperties);
       return bResult;
    }
    ```

    

    ```cpp
    /******************************************************************
    *                                                                 *
    *  GetDevice:  Selects an endpoint that meets the requirements.   *
    *                                                                 *
    *  ppDevice: Receives a pointer to an IMMDevice interface of      *
    *            the device's endpoint object                         *                                             *                                            *
    *                                                                 *
    ******************************************************************/
    HRESULT GetDevice(IMMDevice** ppDevice)
    {
       IMMDeviceEnumerator    *pEnumerator = NULL;
       IMMDevice              *pDevice = NULL;
       IMMDeviceCollection    *pEndpoints = NULL;
       UINT                    cEndpoints = 0;

       const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
       const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

       // Get enumerator for audio endpoint devices
       hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, 
           NULL,
           CLSCTX_ALL, 
           IID_IMMDeviceEnumerator,
           (void**)&pEnumerator));


       EXIT_ON_ERROR(hr)

       // Enumerate all active endpoints,
       hr = pEnumerator->EnumAudioEndpoints (
           eRender,
           DEVICE_STATE_ACTIVE,
           &pEndpoints);
       EXIT_ON_ERROR(hr)

       hr = pEndpoints->GetCount(&cEndpoints);
       EXIT_ON_ERROR(hr)

       for (UINT i = 0; i < cEndpoints; i++)
       {
           hr = pEndpoints->Item(i, &pDevice);
           IF_FAILED_JUMP(hr, Exit);
           {
               // Select the endpoint that meets the requirements.
               // For example, SPDIF analog output or HDMI
               if (IsDigitalEndpoint(pDevice))
               {
                   *(ppDevice) = pDevice;
                   (*ppDevice)->AddRef();
                   break;
               }
           }
           SAFE_RELEASE(pDevice);
       }
    Exit:
       if (FAILED(hr))
       {
           // Notify error.
           // Not Shown.
       }
       SAFE_RELEASE(pEndpoints);
       SAFE_RELEASE(pEnumerator);
    }
    ```

    

3.  <span data-ttu-id="9dc5a-157">Use o ponteiro [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) para o ponto de extremidade retornado pelo processo de enumeração para ativar a API de streaming de áudio desejada e preparar para streaming.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-157">Use the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) pointer to the endpoint returned by the enumeration process to activate the desired audio streaming API and prepare for streaming.</span></span> <span data-ttu-id="9dc5a-158">Diferentes APIs de áudio exigem uma preparação ligeiramente diferente.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-158">Different audio APIs require slightly different preparation.</span></span>
    -   <span data-ttu-id="9dc5a-159">Para aplicativos de áudio do DShow:</span><span class="sxs-lookup"><span data-stu-id="9dc5a-159">For DShow audio applications:</span></span>
        1.  <span data-ttu-id="9dc5a-160">Crie um objeto COM do DirectShow chamando [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) e ESPECIFICANDO \_ IBaseFilter IID como o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-160">Create a DirectShow COM object by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) and specifying IID\_IBaseFilter as the interface identifier.</span></span>
            ```cpp
            IUnknown *pDShowFilter = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IBaseFilter,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDShowFilter));
            ```

            

        2.  <span data-ttu-id="9dc5a-161">Crie um grafo de filtro do DirectShow com este objeto COM ativado pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-161">Build a DirectShow filter graph with this COM object activated by the device.</span></span> <span data-ttu-id="9dc5a-162">Para obter mais informações sobre esse processo, consulte "criando o grafo de filtro" na documentação do SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-162">For more information about this process, see "Building the Filter Graph" in DirectShow SDK documentation.</span></span>
    -   <span data-ttu-id="9dc5a-163">Para aplicativos de áudio DSound:</span><span class="sxs-lookup"><span data-stu-id="9dc5a-163">For DSound audio applications:</span></span>
        1.  <span data-ttu-id="9dc5a-164">Crie um objeto COM DSound chamando [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) e especificando IID \_ IDirectSound8 como o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-164">Create a DSound COM object by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) and specifying IID\_IDirectSound8 as the interface identifier.</span></span>
            ```cpp
            IDirectSound8  *pDSSound8;
            ...
            hr = pDevice->Activate (
                              IID_IDirectSound8,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDSSound8));
            ```

            

        2.  <span data-ttu-id="9dc5a-165">Use o objeto DSound criado acima para programar DSound para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-165">Use DSound object created above to program DSound for steaming.</span></span> <span data-ttu-id="9dc5a-166">Para obter mais informações sobre esse processo, consulte [DirectSound](/previous-versions//bb219818(v=vs.85)) no msdn.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-166">For more information about this process, see [DirectSound](/previous-versions//bb219818(v=vs.85)) on MSDN.</span></span>
    -   <span data-ttu-id="9dc5a-167">Para WASAPI:</span><span class="sxs-lookup"><span data-stu-id="9dc5a-167">For WASAPI:</span></span>
        1.  <span data-ttu-id="9dc5a-168">Crie um objeto com [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) chamando [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) e especificando IID \_ IAudioClient como o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-168">Create an [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) COM object by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) and specifying IID\_IAudioClient as the interface identifier.</span></span>
            ```cpp
            IAudioClient *pIAudioClient = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IAudioClient,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pIAudioClient));
            ```

            

        2.  <span data-ttu-id="9dc5a-169">Abra o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-169">Open the audio stream.</span></span>
            ```cpp
            hr = pIAudioClient->Initialize(...);
            ```

            
4.  <span data-ttu-id="9dc5a-170">Iniciar streaming de áudio.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-170">Start audio streaming.</span></span>
5.  <span data-ttu-id="9dc5a-171">Defina a política de proteção no fluxo.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-171">Set the protection policy on the stream.</span></span>
    1.  <span data-ttu-id="9dc5a-172">Para clientes WASAPI, obtenha uma referência à interface [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) do objeto de autoridade de confiança de saída (OTA) para o fluxo chamando [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) e especificando IID \_ IMFTrustedOutput como o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-172">For WASAPI clients, get a reference to the [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) interface of the output trust authority (OTA) object for the stream by calling [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) and specifying IID\_IMFTrustedOutput as the interface identifier.</span></span>
        ```cpp
        IMFTrustedOutput*       pTrustedOutput = NULL;
        hr = pIAudioClient>GetService(
                       __uuidof(IMFTrustedOutput),
                       (void**)& pTrustedOutput);
        ```

        

    2.  <span data-ttu-id="9dc5a-173">Obtenha uma contagem dos objetos OTA disponíveis chamando [**IMFTrustedOutput:: GetOutputTrustAuthorityCount**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritycount).</span><span class="sxs-lookup"><span data-stu-id="9dc5a-173">Get a count of the available OTA objects by calling [**IMFTrustedOutput::GetOutputTrustAuthorityCount**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritycount).</span></span>
        ```cpp
        hr = pTrustedOutput->GetOutputTrustAuthorityCount(&m_dwCountOTA);
        ```

        

    3.  <span data-ttu-id="9dc5a-174">Enumere a coleção OTA e obtenha uma referência para o objeto OTA que dá suporte à ação PEACTION \_ Play.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-174">Enumerate the OTA collection and get a reference to the OTA object that supports the action PEACTION\_PLAY.</span></span> <span data-ttu-id="9dc5a-175">Todos os OTAs expõem a interface [**IMFOutputTrustAuthority**](/windows/win32/api/mfidl/nn-mfidl-imfoutputtrustauthority) .</span><span class="sxs-lookup"><span data-stu-id="9dc5a-175">All OTAs expose the [**IMFOutputTrustAuthority**](/windows/win32/api/mfidl/nn-mfidl-imfoutputtrustauthority) interface.</span></span>
        ```cpp
        hr = pMFTrustedOutput->GetOutputTrustAuthorityByIndex(I, &pMFOutputTrustAuthority);
        hr = pMFOutputTrustAuthority->GetAction(&action) 
        ```

        

    4.  <span data-ttu-id="9dc5a-176">Use a interface [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) para definir a política de proteção no fluxo.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-176">Use the [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) interface to set the protection policy on the stream.</span></span>

        ```cpp
        hr = pTrustedOutput ->SetPolicy(&pPolicy, nPolicy, &pbTicket, &cbTicket);
        ```

        

        > [!Note]
        > <span data-ttu-id="9dc5a-177">Se você estiver usando o EVR, [**setpolicy**](/windows/win32/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) gerará o evento [MEPolicySet](../medfound/mepolicyset.md) e retornará o MF \_ S \_ Wait by \_ \_ Policy \_ set para indicar que o OTA irá impor a política de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-177">If you are using the EVR, [**SetPolicy**](/windows/win32/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) raises the [MEPolicySet](../medfound/mepolicyset.md) event and returns MF\_S\_WAIT\_FOR\_POLICY\_SET to indicate that the OTA will enforce the policy asynchronously.</span></span> <span data-ttu-id="9dc5a-178">No entanto, neste código de exemplo, o aplicativo é um cliente WASAPI direto que recuperou o objeto OTA do cliente de áudio (etapa 5 a).</span><span class="sxs-lookup"><span data-stu-id="9dc5a-178">However, in this example code, the application is a direct WASAPI client that retrieved the OTA object from the audio client (Step 5 a).</span></span> <span data-ttu-id="9dc5a-179">Diferentemente do EVR, um cliente de áudio e outros objetos WASAPI não implementam geradores de eventos de mídia.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-179">Unlike the EVR, an audio client and other WASAPI objects do not implement media event generators.</span></span> <span data-ttu-id="9dc5a-180">Sem geradores de eventos de mídia, **IMFTrustedOutput:: Setpolicy** não retorna MF \_ S \_ Wait para o \_ \_ conjunto de políticas \_ .</span><span class="sxs-lookup"><span data-stu-id="9dc5a-180">Without media event generators, **IMFTrustedOutput::SetPolicy** does not return MF\_S\_WAIT\_FOR\_POLICY\_SET.</span></span>
        >
        > <span data-ttu-id="9dc5a-181">As configurações de política de áudio devem ser definidas após o streaming de áudio iniciar, caso contrário, [**IMFTrustedOutput:: GetOutputTrustAuthorityByIndex**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritybyindex) falhará.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-181">The audio policy settings must be set after audio streaming starts, otherwise [**IMFTrustedOutput::GetOutputTrustAuthorityByIndex**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritybyindex) fails.</span></span> <span data-ttu-id="9dc5a-182">Além disso, para dar suporte a esse recurso, o driver de áudio subjacente deve ser um *Driver confiável*.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-182">Also, to support this feature, the underlying audio driver must be a *trusted driver*.</span></span>

         

        <span data-ttu-id="9dc5a-183">No código de exemplo, *pPolicy* é um ponteiro para a interface [**IMFOutputPolicy**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) de um objeto de política implementado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-183">In the example code, *pPolicy* is a pointer to the [**IMFOutputPolicy**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) interface of a client-implemented policy object.</span></span> <span data-ttu-id="9dc5a-184">Para obter informações, consulte a documentação do [SDK do Media Foundation](../medfound/microsoft-media-foundation-sdk.md) .</span><span class="sxs-lookup"><span data-stu-id="9dc5a-184">For information, see [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) documentation.</span></span>

        <span data-ttu-id="9dc5a-185">Na implementação do método [**IMFOutputPolicy:: GenerateRequiredSchemas**](/windows/win32/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) , é necessário gerar uma coleção dos sistemas de proteção de saída (esquemas) que o OTA deve impor.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-185">In the implementation of the [**IMFOutputPolicy::GenerateRequiredSchemas**](/windows/win32/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) method, a collection of the output protection systems (schemas) must be generated that the OTA must enforce.</span></span> <span data-ttu-id="9dc5a-186">Cada esquema é identificado por um GUID e contém dados de configuração para o sistema de proteção.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-186">Each schema is identified by a GUID and contains configuration data for the protection system.</span></span> <span data-ttu-id="9dc5a-187">Verifique se os sistemas de proteção da coleção estão restritos ao uso de drivers de áudio confiáveis.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-187">Make sure that the protection systems in the collection are restricted to using trusted audio drivers.</span></span> <span data-ttu-id="9dc5a-188">Essa restrição é identificada pelo GUID, **MFPROTECTION \_ TRUSTEDAUDIODRIVERS**, Disable ou CONSTRICTAUDIO.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-188">This restriction is identified by the GUID, **MFPROTECTION\_TRUSTEDAUDIODRIVERS**,DISABLE, or CONSTRICTAUDIO.</span></span> <span data-ttu-id="9dc5a-189">Se MFPROTECTION \_ TRUSTEDAUDIODRIVERS for usado, os dados de configuração desse esquema serão um DWORD.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-189">If MFPROTECTION\_TRUSTEDAUDIODRIVERS is used, the configuration data for this schema is a DWORD.</span></span> <span data-ttu-id="9dc5a-190">Para obter mais informações sobre os esquemas e os dados de configuração relacionados, consulte a documentação do SDK do ambiente protegido.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-190">For more information about the schemas and the related configuration data, see Protected Environment SDK documentation.</span></span>

        <span data-ttu-id="9dc5a-191">O cliente também deve fornecer a definição de esquema, implementando a interface [**IMFOutputSchema**](/windows/win32/api/mfidl/nn-mfidl-imfoutputschema) .</span><span class="sxs-lookup"><span data-stu-id="9dc5a-191">The client must also provide the schema definition, by implementing the [**IMFOutputSchema**](/windows/win32/api/mfidl/nn-mfidl-imfoutputschema) interface.</span></span> <span data-ttu-id="9dc5a-192">[**IMFOutputSchema:: Getschematype**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getschematype) recupera **MFPROTECTION \_ TRUSTEDAUDIODRIVERS** como o GUID do esquema.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-192">[**IMFOutputSchema::GetSchemaType**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getschematype) retrieves **MFPROTECTION\_TRUSTEDAUDIODRIVERS** as the schema GUID.</span></span> <span data-ttu-id="9dc5a-193">[**IMFOutputSchema:: GetConfigurationData**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata) retorna um ponteiro para os dados de configuração do esquema.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-193">[**IMFOutputSchema::GetConfigurationData**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata) returns a pointer to the schema's configuration data.</span></span>

6.  <span data-ttu-id="9dc5a-194">Continuar streaming de áudio.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-194">Continue audio streaming.</span></span>
7.  <span data-ttu-id="9dc5a-195">Verifique se a política de proteção está desmarcada antes de parar o streaming.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-195">Make sure the protection policy is clear before stopping streaming.</span></span>

    <span data-ttu-id="9dc5a-196">Libere as referências de interface de política relacionadas acima.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-196">Release the related policy interface references above.</span></span>

    <span data-ttu-id="9dc5a-197">As chamadas de versão desmarcam as configurações de política definidas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-197">The release calls clear the previously set policy settings.</span></span>

    > [!Note]  
    > <span data-ttu-id="9dc5a-198">Toda vez que um fluxo é reiniciado, a política de proteção deve ser definida novamente no fluxo.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-198">Every time a stream is restarted, the protection policy must be set again on the stream.</span></span> <span data-ttu-id="9dc5a-199">O procedimento é descrito na etapa 5-d.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-199">The procedure is described in step 5-d.</span></span>

    ```cpp
    pMFOutputTrustAuthority->Release()
    pMFTrustedOutput->Release()
    ```
  

<span data-ttu-id="9dc5a-200">Os exemplos de código a seguir mostram uma implementação de exemplo da política e dos objetos de esquema.</span><span class="sxs-lookup"><span data-stu-id="9dc5a-200">The following code examples show a sample implementation of the policy and schema objects.</span></span>


```cpp
//OTADsoundSample.cpp
#include <stdio.h>
#include <tchar.h>
#include <initguid.h>
#include <windows.h>
#include <mmreg.h>
#include <dsound.h>

#include <mfidl.h>
#include <Mmdeviceapi.h>
#include <AVEndpointKeys.h>
#include "OTADSoundSample.h"

#define STATIC_KSDATAFORMAT_SUBTYPE_AC3\
    DEFINE_WAVEFORMATEX_GUID(WAVE_FORMAT_DOLBY_AC3_SPDIF)
DEFINE_GUIDSTRUCT("00000092-0000-0010-8000-00aa00389b71", KSDATAFORMAT_SUBTYPE_AC3);
#define KSDATAFORMAT_SUBTYPE_AC3 DEFINE_GUIDNAMED(KSDATAFORMAT_SUBTYPE_AC3)


HRESULT SetOTAPolicy(IMMDevice *_pMMDevice,
                     DWORD _dwConfigData,
                     IMFTrustedOutput **_ppMFTrustedOutput,
                     IMFOutputTrustAuthority **ppMFOutputTrustAuthority,
                     IMFOutputPolicy **_ppMFOutputPolicy);
HRESULT ClearOTAPolicy(IMFTrustedOutput *_pMFTrustedOutput,
                       IMFOutputTrustAuthority *_pMFOutputTrustAuthority,
                       IMFOutputPolicy *_pMFOutputPolicy);


const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

BOOL IsDigitalEndpoint(IMMDevice *pDevice)
{
    PROPVARIANT         var;
    IPropertyStore      *pProperties = NULL;
    EndpointFormFactor  formfactor;
    BOOL                bResult = FALSE;
    HRESULT             hr = S_OK;
    PropVariantInit(&var);

    // Open endpoint properties
    hr = pDevice->OpenPropertyStore(STGM_READ, &pProperties);
    IF_FAILED_JUMP(hr, Exit);

    // get form factor 
    hr = pProperties->GetValue(PKEY_AudioEndpoint_FormFactor, &var);
    IF_FAILED_JUMP(hr, Exit);

    formfactor = (EndpointFormFactor)var.uiVal;
    if ((SPDIF == formfactor) || (DigitalAudioDisplayDevice == formfactor))
    {
        bResult = TRUE;
    }

Exit:
    PropVariantClear(&var);
    SAFE_RELEASE(pProperties);

    return bResult;
}


HRESULT GetDigitalAudioEndpoint(IMMDevice** ppDevice)
{
    IMMDeviceEnumerator    *pEnumerator = NULL;
    IMMDevice              *pDevice = NULL;
    IMMDeviceCollection    *pEndpoints = NULL;
    UINT                    cEndpoints = 0;
    HRESULT hr = S_OK;

    *ppDevice = NULL;
    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(CLSID_MMDeviceEnumerator, NULL,
                          CLSCTX_ALL, IID_IMMDeviceEnumerator,
                          (void**)&pEnumerator);
    IF_FAILED_JUMP(hr, Exit);

    // Enumerate all active render endpoints, 
    hr = pEnumerator->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pEndpoints);
    IF_FAILED_JUMP(hr, Exit);

    hr = pEndpoints->GetCount(&cEndpoints);
    IF_FAILED_JUMP(hr, Exit);

    for (UINT i = 0; i < cEndpoints; i++)
    {
        hr = pEndpoints->Item(i, &pDevice);
        IF_FAILED_JUMP(hr, Exit);
        // Select the endpoint that meets the requirements.
        // For example, SPDIF analog output or HDMI
        // Not Shown.
        if (IsDigitalEndpoint(pDevice))
        {
            *ppDevice = pDevice;
            (*ppDevice)->AddRef();
            break;
        }
        SAFE_RELEASE(pDevice);
    }
Exit:
    if (FAILED(hr))
    {
        // Notify error.
        // Not Shown.
    }
    SAFE_RELEASE(pEndpoints);
    SAFE_RELEASE(pEnumerator);
    return hr; 
}


//-------------------------------------------------------------------
int __cdecl wmain(int argc, char* argv[])
{
    IMMDevice *pEndpoint=NULL;
    HRESULT hr = S_OK;

    // DSound related variables
    IDirectSound8*          DSSound8 = NULL; 
    IDirectSoundBuffer*     DSBuffer = NULL; 
    DSBUFFERDESC            DSBufferDesc;
    WAVEFORMATEXTENSIBLE    wfext;
    WORD nChannels = 2;
    DWORD nSamplesPerSec = 48000;
    WORD wBitsPerSample = 16;

    // OTA related variables
    IMFTrustedOutput *pMFTrustedOutput=NULL;
    IMFOutputPolicy *pMFOutputPolicy=NULL;
    IMFOutputTrustAuthority *pMFOutputTrustAuthority=NULL;
    DWORD dwConfigData=0;

    // Initialize COM
    hr = CoInitialize(NULL);
    IF_FAILED_JUMP(hr, Exit);

    printf("OTA test app for DSound\n");

    hr = GetDigitalAudioEndpoint(&pEndpoint);
    IF_FAILED_JUMP(hr, Exit);

    if (pEndpoint)
    {
        printf("Found digital audio endpoint.\n");
    }
    //
    // Active DSound interface
    //
    hr = pEndpoint->Activate(IID_IDirectSound8, CLSCTX_INPROC_SERVER, NULL, reinterpret_cast<void **>(&DSSound8));
    IF_FAILED_JUMP(hr, Exit);

    nChannels = 2;
    nSamplesPerSec = 48000;
    wBitsPerSample = 16;

    ZeroMemory(&wfext, sizeof(wfext));
    wfext.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
    wfext.Format.nChannels = nChannels;
    wfext.Format.nSamplesPerSec = nSamplesPerSec;
    wfext.Format.wBitsPerSample = wBitsPerSample;
    wfext.Format.nBlockAlign = (nChannels * wBitsPerSample) / 8;
    wfext.Format.nAvgBytesPerSec = nSamplesPerSec * ((nChannels * wBitsPerSample) / 8);
    wfext.Format.cbSize = 22;
    wfext.Samples.wValidBitsPerSample = wBitsPerSample;
    wfext.dwChannelMask = 0x3;
    wfext.SubFormat = KSDATAFORMAT_SUBTYPE_PCM;
#if 1 
    wfext.SubFormat = KSDATAFORMAT_SUBTYPE_AC3;
#endif

    ZeroMemory(&DSBufferDesc, sizeof(DSBufferDesc));
    DSBufferDesc.dwSize = sizeof(DSBufferDesc);
    DSBufferDesc.dwFlags = DSBCAPS_GLOBALFOCUS | DSBCAPS_LOCSOFTWARE | DSBCAPS_GETCURRENTPOSITION2;
    DSBufferDesc.lpwfxFormat = (WAVEFORMATEX *)&wfext;
    DSBufferDesc.dwBufferBytes = wfext.Format.nAvgBytesPerSec / 100;

    HWND hwnd = GetForegroundWindow();
    hr = DSSound8->SetCooperativeLevel(hwnd, DSSCL_PRIORITY);
    IF_FAILED_JUMP(hr, Exit);

    hr = DSSound8->CreateSoundBuffer(&DSBufferDesc, &DSBuffer, NULL);
    IF_FAILED_JUMP(hr, Exit);

    hr = DSBuffer->Play(0, 0, DSBPLAY_LOOPING);
    IF_FAILED_JUMP(hr, Exit);

    printf("Will set the following audio policy:\n");
    printf("Test Certificate Enable: %s\n", TRUE ? "True" : "False");
    printf("Copy OK: %s\n", FALSE ? "True" : "False");
    printf("Digital Output Disable: %s\n", FALSE ? "True" : "False");
    printf("DRM Level: %u\n", 1300);

    // Set policy when the stream is in RUN state
    dwConfigData = MAKE_MFPROTECTIONDATA_TRUSTEDAUDIODRIVERS2(TRUE, /*_bTestCertificateEnable*/ 
                                                              FALSE, /*_bDigitalOutputDisable*/ 
                                                              FALSE, /*_bCopyOK*/ 
                                                              1300 /*_dwDrmLevel*/);

    hr = SetOTAPolicy(pEndpoint,dwConfigData, &pMFTrustedOutput, &pMFOutputTrustAuthority,&pMFOutputPolicy); 
    IF_FAILED_JUMP(hr, Exit);

    //
    // Perform all the necessary streaming operations here.
    //

    // stop audio streaming
    DSBuffer->Stop();

    // In order for the stream to restart successfully 
    // Need to release the following OutputTrust* interface to release audio endpoint
    hr = ClearOTAPolicy(pMFTrustedOutput,pMFOutputTrustAuthority,pMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    // After above release operations, the following Play() will succeed without without device-in-use error message 0x8889000A
    DSBuffer->SetCurrentPosition(0);
    hr = DSBuffer->Play(0, 0, DSBPLAY_LOOPING);
    IF_FAILED_JUMP(hr, Exit);

    // Need to reset the new audio protection state because previous settings were gone with the ClearOTAPolicy call.
    dwConfigData = MAKE_MFPROTECTIONDATA_TRUSTEDAUDIODRIVERS2(TRUE, /*_bTestCertificateEnable*/ 
                                                              FALSE, /*_bDigitalOutputDisable*/ 
                                                              FALSE, /*_bCopyOK*/ 
                                                              1300 /*_dwDrmLevel*/);

    hr = SetOTAPolicy(pEndpoint,dwConfigData, &pMFTrustedOutput, &pMFOutputTrustAuthority,&pMFOutputPolicy); 
    IF_FAILED_JUMP(hr, Exit);

    // Clean up setting before leaving your streaming app.
    hr = ClearOTAPolicy(pMFTrustedOutput,pMFOutputTrustAuthority,pMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    DSBuffer->SetCurrentPosition(0);

Exit:
    SAFE_RELEASE(DSBuffer);
    SAFE_RELEASE(DSSound8);

    SAFE_RELEASE(pEndpoint);

    CoUninitialize();

    return 0;
}
```




```cpp
//OTADSoundSample.h
// Macro defines
#define IF_FAILED_JUMP(_hresult, label)                         \
    if(FAILED(_hresult))                                        \
    {                                                           \
        goto label;                                             \
    }

#define SAFE_RELEASE(p) \
    if (NULL != p) { \
        (p)->Release(); \
        (p) = NULL; \
    }

#define IF_TRUE_ACTION_JUMP(condition, action, label)           \
    if(condition)                                               \
    {                                                           \
        action;                                                 \
        goto label;                                             \
    }
```




```cpp
// outputpolicy.h

class CTrustedAudioDriversOutputPolicy : public CMFAttributesImpl<IMFOutputPolicy> 
{
friend
    HRESULT CreateTrustedAudioDriversOutputPolicy(DWORD dwConfigData, IMFOutputPolicy **ppMFOutputPolicy);
private:
    ULONG m_cRefCount;
    DWORD m_dwConfigData;
    GUID m_guidOriginator;
    IMFOutputSchema *m_pOutputSchema;
    
    CTrustedAudioDriversOutputPolicy(DWORD dwConfigData, HRESULT &hr);
    ~CTrustedAudioDriversOutputPolicy();

public:
    // IUnknown methods
    HRESULT STDMETHODCALLTYPE QueryInterface(/* [in] */ REFIID riid,/* [out] */ LPVOID *ppvObject);
    ULONG STDMETHODCALLTYPE AddRef();
    ULONG STDMETHODCALLTYPE Release();
    
    // IMFOutputPolicy methods
    HRESULT STDMETHODCALLTYPE
        GenerateRequiredSchemas( 
            /* [in] */ DWORD dwAttributes,
            /* [in] */ GUID guidOutputSubType,
            /* [in] */ GUID *rgGuidProtectionSchemasSupported,
            /* [in] */ DWORD cProtectionSchemasSupported,
            /* [annotation][out] */ 
            __out  IMFCollection **ppRequiredProtectionSchemas);

    HRESULT STDMETHODCALLTYPE GetOriginatorID(/* [annotation][out] */ __out  GUID *pguidOriginatorID);

    HRESULT STDMETHODCALLTYPE GetMinimumGRLVersion(/* [annotation][out] */ __out  DWORD *pdwMinimumGRLVersion);
}; // CTrustedAudioDriversOutputPolicy

class CTrustedAudioDriversOutputSchema : public CMFAttributesImpl<IMFOutputSchema> 
{

friend
    HRESULT CreateTrustedAudioDriversOutputSchema(
        DWORD dwConfigData,
        GUID guidOriginatorID,
        IMFOutputSchema **ppMFOutputSchema
    );

private:
    CTrustedAudioDriversOutputSchema(DWORD dwConfigData, GUID guidOriginatorID);
    ~CTrustedAudioDriversOutputSchema();

    ULONG m_cRefCount;
    DWORD m_dwConfigData;
    GUID m_guidOriginatorID;
    
public:
    // IUnknown methods
    HRESULT STDMETHODCALLTYPE QueryInterface(
       /* [in] */ REFIID riid,
       /* [out] */ LPVOID *ppvObject
    );
    ULONG STDMETHODCALLTYPE AddRef();
    ULONG STDMETHODCALLTYPE Release();

    // IMFOutputSchema methods
    HRESULT STDMETHODCALLTYPE GetConfigurationData(__out DWORD *pdwVal);
    HRESULT STDMETHODCALLTYPE GetOriginatorID(__out GUID *pguidOriginatorID);
    HRESULT STDMETHODCALLTYPE GetSchemaType(__out GUID *pguidSchemaType);

}; // CTrustedAudioDriversOutputSchema
```




```cpp
// outputpolicy.cpp

#include <windows.h>
#include <tchar.h>
#include <mfidl.h>
#include <atlstr.h>
#include <attributesbase.h>
#include "OTADSoundSample.h"

#include <Mmdeviceapi.h>
#include "OutputPolicy.h"

#define RETURN_INTERFACE(T, iid, ppOut) \
    if (IsEqualIID(__uuidof(T), (iid))) { \
        this->AddRef(); \
        *(ppOut) = static_cast<T *>(this); \
        return S_OK; \
    } else {} (void)0

//--------------------------------------------------------------------------
// Implementation for CTrustedAudioDriversOutputPolicy
//--------------------------------------------------------------------------
// constructor
CTrustedAudioDriversOutputPolicy::CTrustedAudioDriversOutputPolicy(DWORD dwConfigData, HRESULT &hr)
: m_cRefCount(1), m_dwConfigData(dwConfigData), m_pOutputSchema(NULL)
{
    hr = CoCreateGuid(&m_guidOriginator);
    IF_FAILED_JUMP(hr, Exit);

    hr = CreateTrustedAudioDriversOutputSchema(dwConfigData, m_guidOriginator, &m_pOutputSchema);
    IF_FAILED_JUMP(hr, Exit);

Exit:
    if (FAILED(hr))
    {
        printf("CreateTrustedAudioDriversOutputSchema failed: hr = 0x%08x", hr);
    }
    return;
}

// destructor
CTrustedAudioDriversOutputPolicy::~CTrustedAudioDriversOutputPolicy()
{
    if (NULL != m_pOutputSchema) 
    {
        m_pOutputSchema->Release();
    }
}


// IUnknown::QueryInterface
HRESULT STDMETHODCALLTYPE
    CTrustedAudioDriversOutputPolicy::QueryInterface(
        /* [in] */ REFIID riid,
        /* [out] */ LPVOID *ppvObject)
{
    HRESULT hr = E_NOINTERFACE;

    IF_TRUE_ACTION_JUMP((NULL == ppvObject), hr = E_POINTER, Exit);

    *ppvObject = NULL;

    RETURN_INTERFACE(IUnknown, riid, ppvObject);
    RETURN_INTERFACE(IMFAttributes, riid, ppvObject);
    RETURN_INTERFACE(IMFOutputPolicy, riid, ppvObject);    

Exit:
    return hr;
}

// IUnknown::AddRef
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::AddRef() 
{
    ULONG uNewRefCount = InterlockedIncrement(&m_cRefCount);
    return uNewRefCount;
}

// IUnknown::Release
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::Release() 
{
    ULONG uNewRefCount = InterlockedDecrement(&m_cRefCount);
    if (0 == uNewRefCount) 
    {
        delete this;
    }
    return uNewRefCount;
}

// IMFOutputPolicy::GenerateRequiredSchemas
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GenerateRequiredSchemas
( 
        /* [in] */ DWORD dwAttributes,
        /* [in] */ GUID guidOutputSubType,
        /* [in] */ GUID *rgGuidProtectionSchemasSupported,
        /* [in] */ DWORD cProtectionSchemasSupported,
        /* [annotation][out] */ 
        __out  IMFCollection **ppRequiredProtectionSchemas
)
{
    HRESULT hr = S_OK;
    bool bTrustedAudioDriversSupported = false;
    // if we've made it this far then the Output Trust Authority supports Trusted Audio Drivers
    // create a collection and put our output policy in it
    // then give that collection to the caller
    CComPtr<IMFCollection> pMFCollection;

    // sanity checks
    IF_TRUE_ACTION_JUMP((NULL == ppRequiredProtectionSchemas), hr = E_POINTER, Exit); 
    *ppRequiredProtectionSchemas = NULL;

    IF_TRUE_ACTION_JUMP((NULL == rgGuidProtectionSchemasSupported) && (0 != cProtectionSchemasSupported), 
                    hr = E_POINTER, Exit); 

    // log all the supported protection schemas
    for (DWORD i = 0; i < cProtectionSchemasSupported; i++) 
    {
        if (IsEqualIID(MFPROTECTION_TRUSTEDAUDIODRIVERS, rgGuidProtectionSchemasSupported[i])) 
        {
            bTrustedAudioDriversSupported = true;
        }
    }

    if (!bTrustedAudioDriversSupported) 
    {
        return HRESULT_FROM_WIN32(ERROR_RANGE_NOT_FOUND);
    }


    // create the collection
    hr = MFCreateCollection(&pMFCollection);
    if (FAILED(hr)) 
    {
        return hr;
    }

    // add our output policy to the collection
    hr = pMFCollection->AddElement(m_pOutputSchema);
    if (FAILED(hr)) 
    {
        return hr;
    }
Exit:
    // give the collection to the caller
    return pMFCollection.CopyTo(ppRequiredProtectionSchemas); // increments refcount
}// GenerateRequiredSchemas

HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GetOriginatorID(__out  GUID *pguidOriginatorID) 
{
    if (NULL == pguidOriginatorID) 
    {
        return E_POINTER;
    }
    *pguidOriginatorID = m_guidOriginator;
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GetMinimumGRLVersion(__out  DWORD *pdwMinimumGRLVersion) 
{
    if (NULL == pdwMinimumGRLVersion) 
    {
        return E_POINTER;
    }
    *pdwMinimumGRLVersion = 0;
    return S_OK;
}

//--------------------------------------------------------------------------
// Implementation for CTrustedAudioDriversOutputSchema
//--------------------------------------------------------------------------
// constructor
CTrustedAudioDriversOutputSchema::CTrustedAudioDriversOutputSchema
(    
    DWORD dwConfigData, 
    GUID guidOriginatorID
)
: m_cRefCount(1)
, m_dwConfigData(dwConfigData)
, m_guidOriginatorID(guidOriginatorID)
{}

// destructor
CTrustedAudioDriversOutputSchema::~CTrustedAudioDriversOutputSchema() {}

// IUnknown::QueryInterface
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::QueryInterface
(
        /* [in] */ REFIID riid,
        /* [out] */ LPVOID *ppvObject
) 
{
    HRESULT hr = E_NOINTERFACE;

    IF_TRUE_ACTION_JUMP((NULL == ppvObject), hr = E_POINTER, Exit);
    *ppvObject = NULL;

    RETURN_INTERFACE(IUnknown, riid, ppvObject);
    RETURN_INTERFACE(IMFAttributes, riid, ppvObject);
    RETURN_INTERFACE(IMFOutputSchema, riid, ppvObject);

Exit:
    return hr;
}

// IUnknown::AddRef
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::AddRef() 
{
    ULONG uNewRefCount = InterlockedIncrement(&m_cRefCount);
    return uNewRefCount;
}

// IUnknown::Release
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::Release() 
{
    ULONG uNewRefCount = InterlockedDecrement(&m_cRefCount);
    if (0 == uNewRefCount) 
    {
        delete this;
    }
    return uNewRefCount;
}
// IMFOutputSchema::GetConfigurationData
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetConfigurationData(__out DWORD *pdwVal) 
{
    if (NULL == pdwVal) { return E_POINTER; }
    *pdwVal = m_dwConfigData;
    return S_OK;
}

// IMFOutputSchema::GetOriginatorID
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetOriginatorID(__out GUID *pguidOriginatorID) 
{
    if (NULL == pguidOriginatorID) { return E_POINTER; }
    *pguidOriginatorID = m_guidOriginatorID;
    return S_OK;
}
// IMFOutputSchema::GetSchemaType
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetSchemaType(__out GUID *pguidSchemaType) 
{
    if (NULL == pguidSchemaType) { return E_POINTER; }
    *pguidSchemaType = MFPROTECTION_TRUSTEDAUDIODRIVERS;
    return S_OK;
}

//---------------------------------------------------------------------------------------------------
//
// Other subroutine declarations
//
//---------------------------------------------------------------------------------------------------
HRESULT CreateTrustedAudioDriversOutputPolicy(DWORD dwConfigData, IMFOutputPolicy **ppMFOutputPolicy) 
{
    if (NULL == ppMFOutputPolicy) 
    {
        return E_POINTER;
    }

    *ppMFOutputPolicy = NULL;

    HRESULT hr = S_OK;
    CTrustedAudioDriversOutputPolicy *pPolicy = new CTrustedAudioDriversOutputPolicy(dwConfigData, hr);
    if (NULL == pPolicy) 
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr)) 
    {
        delete pPolicy;
        return hr;
    }
    *ppMFOutputPolicy = static_cast<IMFOutputPolicy *>(pPolicy);
    return S_OK;
}// CreateTrustedAudioDriversOutputPolicy

HRESULT CreateTrustedAudioDriversOutputSchema
(
    DWORD dwConfigData,
    GUID guidOriginatorID,
    IMFOutputSchema **ppMFOutputSchema) 
{
    if (NULL == ppMFOutputSchema) 
    {
        return E_POINTER;
    }

    *ppMFOutputSchema = NULL;

    CTrustedAudioDriversOutputSchema *pSchema =
        new CTrustedAudioDriversOutputSchema(dwConfigData, guidOriginatorID);

    if (NULL == pSchema) 
    {
        return E_OUTOFMEMORY;
    }

    *ppMFOutputSchema = static_cast<IMFOutputSchema *>(pSchema);

    return S_OK;
}// CreateTrustedAudioDriversOutputSchema



HRESULT SetOTAPolicy(IMMDevice *_pMMDevice,
                     DWORD _dwConfigData,
                     IMFTrustedOutput **_ppMFTrustedOutput,
                     IMFOutputTrustAuthority **ppMFOutputTrustAuthority,
                     IMFOutputPolicy **_ppMFOutputPolicy)
{
    HRESULT hr = S_OK;

    DWORD dwCountOfOTAs = 0;
    bool bRet = false;

    hr = CreateTrustedAudioDriversOutputPolicy(_dwConfigData, _ppMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    // activate IMFTrustedOutput
    hr = _pMMDevice->Activate(__uuidof(IMFTrustedOutput), CLSCTX_ALL, NULL,
                             (void**)_ppMFTrustedOutput);
    IF_FAILED_JUMP(hr, Exit);

    // get count of Output Trust Authorities on this trusted output
    hr = (*_ppMFTrustedOutput)->GetOutputTrustAuthorityCount(&dwCountOfOTAs);
    IF_FAILED_JUMP(hr, Exit);

    // sanity check - fail on endpoints with no output trust authorities
    IF_TRUE_ACTION_JUMP((0 == dwCountOfOTAs), hr = E_NOTFOUND, Exit);

    printf("dwCountOfOTAs = %d\n", dwCountOfOTAs);

     
    // loop over each output trust authority on the endpoint
    for (DWORD i = 0; i < dwCountOfOTAs; i++) 
    {
        // get the output trust authority
        hr = (*_ppMFTrustedOutput)->GetOutputTrustAuthorityByIndex(i, ppMFOutputTrustAuthority);
        IF_FAILED_JUMP(hr, Exit);


        // log the purpose of the output trust authority
        MFPOLICYMANAGER_ACTION action;
        hr = (*ppMFOutputTrustAuthority)->GetAction(&action);
        if (FAILED(hr)) 
        {
            return hr;
        }

        printf(" It's %s.", (PEACTION_PLAY==action) ? "PEACTION_PLAY" :
                            (PEACTION_COPY==action) ? "PEACTION_COPY" :
                            "Others");
 
        // only PEACTION_PLAY Output Trust Authorities are relevant
        if (PEACTION_PLAY != action) 
        {
            printf("Skipping as the OTA action is not PEACTION_PLAY");
            SAFE_RELEASE(*ppMFOutputTrustAuthority);
            continue;
        }

        BYTE *pbTicket = NULL;
        DWORD cbTicket = 0;
        // audio ota does not support ticket, leaving it NULL is ok.
        hr = (*ppMFOutputTrustAuthority)->SetPolicy(_ppMFOutputPolicy, 1, &pbTicket, &cbTicket);
        IF_FAILED_JUMP(hr, Exit);
        printf("SetPolicy succeeded.\n");

        bRet = true;
        break;

    }// for each output trust authority

Exit:
    if (bRet)
    {
        hr = S_OK;
    }
    if (FAILED(hr))
    {
        printf("failure code is 0x%0x\n", hr);
        SAFE_RELEASE(*ppMFOutputTrustAuthority);
        SAFE_RELEASE(*_ppMFTrustedOutput);
        if (*_ppMFOutputPolicy)
        {
            delete (*_ppMFOutputPolicy);
        }
    }

    return hr;
}


HRESULT ClearOTAPolicy(IMFTrustedOutput *_pMFTrustedOutput,
                       IMFOutputTrustAuthority *_pMFOutputTrustAuthority,
                       IMFOutputPolicy *_pMFOutputPolicy)
{
    SAFE_RELEASE(_pMFOutputTrustAuthority);
    SAFE_RELEASE(_pMFTrustedOutput);
    if (_pMFOutputPolicy)
    {
        delete _pMFOutputPolicy;
    }
    return S_OK;
}
```




```cpp
//OTADSoundSample.rc
#include "windows.h"

/////////////////////////////////////////////////////////////////////////////
// Version
#include <ntverp.h>

#define VER_FILETYPE                VFT_DLL
#define VER_FILESUBTYPE             VFT2_UNKNOWN
#define VER_FILEDESCRIPTION_STR     "Default Device Heuristic Dumper"
#define VER_INTERNALNAME_STR        "DefaultDeviceDump.exe"
#define VER_ORIGINALFILENAME_STR    "DefaultDeviceDump.exe"

#include "common.ver"
```




```cpp
Sources file:

TARGETNAME=OTADSoundSample
TARGETTYPE=PROGRAM
TARGET_DESTINATION=retail
UMTYPE=console
UMENTRY=wmain
UMBASE=0x1000000
#_NT_TARGET_VERSION=$(_NT_TARGET_VERSION_VISTA)
MSC_WARNING_LEVEL=$(MSC_WARNING_LEVEL) /WX
USE_ATL=1
ATL_VER=70
USE_NATIVE_EH=1
USE_MSVCRT=1
C_DEFINES=-DUNICODE -D_UNICODE
INCLUDES=$(INCLUDES);  

SOURCES=OTADSoundSample.cpp \
        OTADSoundSample.rc \
        outputpolicy.cpp\

TARGETLIBS=\
       $(SDK_LIB_PATH)\advapi32.lib         \
       $(SDK_LIB_PATH)\kernel32.lib         \
       $(SDK_LIB_PATH)\User32.lib           \
       $(SDK_LIB_PATH)\shlwapi.lib          \
       $(SDK_LIB_PATH)\ole32.lib            \
       $(SDK_LIB_PATH)\oleaut32.lib         \
       $(SDK_LIB_PATH)\rpcrt4.lib           \
       $(SDK_LIB_PATH)\strmiids.lib         \
       $(SDK_LIB_PATH)\uuid.lib             \
       $(SDK_LIB_PATH)\SetupAPI.lib         \
       $(SDK_LIB_PATH)\mfplat.lib \
```



## <a name="related-topics"></a><span data-ttu-id="9dc5a-201">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9dc5a-201">Related topics</span></span>

[<span data-ttu-id="9dc5a-202">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="9dc5a-202">Programming Guide</span></span>](programming-guide.md)

[<span data-ttu-id="9dc5a-203">Componentes de áudio do modo de usuário</span><span class="sxs-lookup"><span data-stu-id="9dc5a-203">User-Mode Audio Components</span></span>](user-mode-audio-components.md)
