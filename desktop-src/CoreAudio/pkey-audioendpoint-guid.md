---
description: A \_ \_ Propriedade GUID PKEY AudioEndpoint fornece o identificador de dispositivo DirectSound que corresponde ao dispositivo de ponto de extremidade de áudio.
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: PKEY_AudioEndpoint_GUID (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45405cd2350777e535b50859e77aa56755d191fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749534"
---
# <a name="pkey_audioendpoint_guid"></a><span data-ttu-id="45613-103">PKEY \_ AudioEndpoint \_ GUID</span><span class="sxs-lookup"><span data-stu-id="45613-103">PKEY\_AudioEndpoint\_GUID</span></span>

<span data-ttu-id="45613-104">A **propriedade \_ \_ GUID PKEY AudioEndpoint** fornece o identificador de dispositivo DirectSound que corresponde ao dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="45613-104">The **PKEY\_AudioEndpoint\_GUID** property supplies the DirectSound device identifier that corresponds to the audio endpoint device.</span></span> <span data-ttu-id="45613-105">O valor da propriedade é um GUID que o cliente pode fornecer como o identificador do dispositivo para a função **DirectSoundCreate** ou **DirectSoundCaptureCreate** na API do DirectSound.</span><span class="sxs-lookup"><span data-stu-id="45613-105">The property value is a GUID that the client can supply as the device identifier to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function in the DirectSound API.</span></span> <span data-ttu-id="45613-106">Esse valor identifica exclusivamente o dispositivo de ponto de extremidade de áudio em todos os dispositivos de ponto de extremidade de áudio no sistema.</span><span class="sxs-lookup"><span data-stu-id="45613-106">This value uniquely identifies the audio endpoint device across all audio endpoint devices in the system.</span></span> <span data-ttu-id="45613-107">Para obter mais informações sobre o DirectSound, consulte a documentação do SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="45613-107">For more information about DirectSound, see the DirectX SDK documentation.</span></span>

<span data-ttu-id="45613-108">O membro **VT** da estrutura **PROPVARIANT** é definido como VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="45613-108">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="45613-109">O membro **pwszVal** da estrutura **PROPVARIANT** aponta para uma cadeia de caracteres largos terminada em nulo que contém um GUID que identifica o dispositivo de ponto de extremidade de áudio no DirectSound.</span><span class="sxs-lookup"><span data-stu-id="45613-109">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a GUID that identifies the audio endpoint device in DirectSound.</span></span>

<span data-ttu-id="45613-110">Conforme explicado anteriormente, a [API do MMDevice](mmdevice-api.md) dá suporte a funções de [dispositivo](device-roles.md).</span><span class="sxs-lookup"><span data-stu-id="45613-110">As explained previously, the [MMDevice API](mmdevice-api.md) supports [device roles](device-roles.md).</span></span> <span data-ttu-id="45613-111">Embora o DirectSound não ofereça suporte direto a funções de dispositivo, um cliente DirectSound pode usar a \_ propriedade de GUID PKEY AudioEndpoint \_ para selecionar um dispositivo de captura ou processamento DirectSound com base em sua função de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45613-111">Although DirectSound does not directly support device roles, a DirectSound client can use the PKEY\_AudioEndpoint\_GUID property to select a DirectSound rendering or capture device based on its device role.</span></span>

<span data-ttu-id="45613-112">Por exemplo, um aplicativo DirectSound executa as seguintes etapas para criar um dispositivo DirectSound que corresponde ao dispositivo de ponto de extremidade de renderização ao qual o usuário atribuiu a função eMultimedia:</span><span class="sxs-lookup"><span data-stu-id="45613-112">For example, a DirectSound application performs the following steps to create a DirectSound device that corresponds to the rendering endpoint device that the user has assigned the eMultimedia role to:</span></span>

1.  <span data-ttu-id="45613-113">Chame o método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obter a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) do dispositivo de ponto de extremidade de renderização que tem a função eMultimedia.</span><span class="sxs-lookup"><span data-stu-id="45613-113">Call the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to get the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the rendering endpoint device that has the eMultimedia role.</span></span>
2.  <span data-ttu-id="45613-114">Chame o método [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) para obter a interface **IPropertyStore** do dispositivo eMultimedia.</span><span class="sxs-lookup"><span data-stu-id="45613-114">Call the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method to obtain the **IPropertyStore** interface of the eMultimedia device.</span></span> <span data-ttu-id="45613-115">Para obter mais informações sobre o **IPropertyStore**, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="45613-115">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>
3.  <span data-ttu-id="45613-116">Chame o método **IPropertyStore:: GetValue** para obter o \_ valor da propriedade PKEY AudioEndpoint \_ GUID.</span><span class="sxs-lookup"><span data-stu-id="45613-116">Call the **IPropertyStore::GetValue** method to obtain the PKEY\_AudioEndpoint\_GUID property value.</span></span>
4.  <span data-ttu-id="45613-117">Converta o valor da propriedade de um GUID no formato de cadeia de caracteres em uma estrutura de GUID de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="45613-117">Convert the property value from a GUID in string format to a 16-byte GUID structure.</span></span>
5.  <span data-ttu-id="45613-118">Chame a função **DirectSoundCreate** com o GUID para criar o dispositivo com a função eMultimedia.</span><span class="sxs-lookup"><span data-stu-id="45613-118">Call the **DirectSoundCreate** function with the GUID to create the device with the eMultimedia role.</span></span>

> [!Note]  
> <span data-ttu-id="45613-119">**PKEY \_ AudioEndpoint \_ GUID** é uma propriedade somente leitura, independentemente do modo de acesso de armazenamento solicitado pelo aplicativo em [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore).</span><span class="sxs-lookup"><span data-stu-id="45613-119">**PKEY\_AudioEndpoint\_GUID** is a read-only property regardless of the storage-access mode requested by the application in [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore).</span></span> <span data-ttu-id="45613-120">Se um aplicativo tentar definir um valor usando **IPropertyStore:: SetValue**, essa chamada falhará com o código de \_ erro E ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="45613-120">If an application attempts to set a value by using **IPropertyStore::SetValue**, this call fails with the E\_ACCESSDENIED error code.</span></span>

 

<span data-ttu-id="45613-121">Observe que o GUID de 16 bytes gerado na etapa 4 corresponde ao GUID do dispositivo que identifica o dispositivo durante a enumeração do dispositivo DirectSound.</span><span class="sxs-lookup"><span data-stu-id="45613-121">Note that the 16-byte GUID generated in step 4 matches the device GUID that identifies the device during DirectSound device enumeration.</span></span> <span data-ttu-id="45613-122">A função **DirectSoundEnumerate** enumera os dispositivos de ponto de extremidade de renderização e a função **DirectSoundCaptureEnumerate** enumera os dispositivos de ponto de extremidade de captura.</span><span class="sxs-lookup"><span data-stu-id="45613-122">The **DirectSoundEnumerate** function enumerates rendering endpoint devices, and the **DirectSoundCaptureEnumerate** function enumerates capture endpoint devices.</span></span> <span data-ttu-id="45613-123">Em ambos os casos, o GUID do dispositivo é o primeiro parâmetro passado para a função de retorno de chamada de enumeração.</span><span class="sxs-lookup"><span data-stu-id="45613-123">In either case, the device GUID is the first parameter passed to the enumeration callback function.</span></span> <span data-ttu-id="45613-124">Para obter mais informações sobre a enumeração do DirectSound, consulte a documentação do SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="45613-124">For more information about DirectSound enumeration, see the DirectX SDK documentation.</span></span>

<span data-ttu-id="45613-125">Para obter um exemplo de código que usa a \_ propriedade de GUID PKEY AudioEndpoint \_ , consulte [funções de dispositivo para aplicativos DirectSound](device-roles-for-directsound-applications.md).</span><span class="sxs-lookup"><span data-stu-id="45613-125">For a code example that uses the PKEY\_AudioEndpoint\_GUID property, see [Device Roles for DirectSound Applications](device-roles-for-directsound-applications.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="45613-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45613-126">Requirements</span></span>



| <span data-ttu-id="45613-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="45613-127">Requirement</span></span> | <span data-ttu-id="45613-128">Valor</span><span class="sxs-lookup"><span data-stu-id="45613-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="45613-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45613-129">Minimum supported client</span></span><br/> | <span data-ttu-id="45613-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45613-130">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="45613-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45613-131">Minimum supported server</span></span><br/> | <span data-ttu-id="45613-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="45613-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="45613-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45613-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="45613-134"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="45613-134"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45613-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="45613-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45613-136">**Propriedades do ponto de extremidade de áudio**</span><span class="sxs-lookup"><span data-stu-id="45613-136">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="45613-137">Propriedades de áudio de núcleo</span><span class="sxs-lookup"><span data-stu-id="45613-137">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




