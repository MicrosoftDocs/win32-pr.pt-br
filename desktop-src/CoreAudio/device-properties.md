---
description: Propriedades do Dispositivo
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: Propriedades do dispositivo (APIs de áudio principal)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a868e4bb806bd49d934febed164bcd70fba39f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755644"
---
# <a name="device-properties-core-audio-apis"></a><span data-ttu-id="71880-103">Propriedades do dispositivo (APIs de áudio principal)</span><span class="sxs-lookup"><span data-stu-id="71880-103">Device Properties (Core Audio APIs)</span></span>

<span data-ttu-id="71880-104">Durante o processo de enumeração de [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md), um aplicativo cliente pode interrogar os objetos de ponto de extremidade para suas propriedades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71880-104">During the process of enumerating [audio endpoint devices](audio-endpoint-devices.md), a client application can interrogate the endpoint objects for their device properties.</span></span> <span data-ttu-id="71880-105">As propriedades do dispositivo são expostas na implementação da API do MMDevice da interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="71880-105">The device properties are exposed in MMDevice API's implementation of the **IPropertyStore** interface.</span></span> <span data-ttu-id="71880-106">Dada uma referência à interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) de um objeto de ponto de extremidade, um cliente pode obter uma referência ao repositório de propriedades do objeto de ponto de extremidade chamando o método [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) .</span><span class="sxs-lookup"><span data-stu-id="71880-106">Given a reference to the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of an endpoint object, a client can obtain a reference to the endpoint object's property store by calling the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method.</span></span>

<span data-ttu-id="71880-107">O objeto de repositório de propriedades expõe uma interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="71880-107">The property-store object exposes an **IPropertyStore** interface.</span></span> <span data-ttu-id="71880-108">Os dois métodos principais nessa interface são **IPropertyStore:: GetValue**, que obtém um valor de propriedade de dispositivo e **IPropertyStore:: SetValue**, que define um valor de propriedade de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71880-108">The two primary methods in this interface are **IPropertyStore::GetValue**, which gets a device property value, and **IPropertyStore::SetValue**, which sets a device property value.</span></span> <span data-ttu-id="71880-109">Para obter mais informações sobre o **IPropertyStore**, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="71880-109">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="71880-110">A implementação da API do MMDevice do repositório de propriedades é diferente do objeto de armazenamento de Propriedade do shell padrão.</span><span class="sxs-lookup"><span data-stu-id="71880-110">The MMDevice API's implementation of the property store is different from the standard shell property store object.</span></span> <span data-ttu-id="71880-111">Para alterar um valor de propriedade, o aplicativo cliente deve chamar o método **IPropertyStore:: SetValue** .</span><span class="sxs-lookup"><span data-stu-id="71880-111">To change a property value, the client application must call the **IPropertyStore::SetValue** method.</span></span> <span data-ttu-id="71880-112">Durante essa chamada, os novos valores são definidos e gravados no registro.</span><span class="sxs-lookup"><span data-stu-id="71880-112">During this call, the new values are set and written in the registry.</span></span> <span data-ttu-id="71880-113">Portanto, o aplicativo não precisa chamar o método **IPropertyStore:: Commit** após a chamada **SetValue** .</span><span class="sxs-lookup"><span data-stu-id="71880-113">Therefore, the application does not need to call the **IPropertyStore::Commit** method after the **SetValue** call.</span></span> <span data-ttu-id="71880-114">O identificador para o registro é fechado somente quando o cliente libera o ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="71880-114">The handle to the registry is closed only when the client releases the interface pointer.</span></span>

<span data-ttu-id="71880-115">Normalmente, aplicativos cliente de terceiros chamam o método **GetValue** , mas não o método **SetValue** .</span><span class="sxs-lookup"><span data-stu-id="71880-115">Typically, third-party client applications call the **GetValue** method but not the **SetValue** method.</span></span> <span data-ttu-id="71880-116">O Gerenciador de pontos de extremidade define as propriedades básicas do dispositivo para pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="71880-116">The endpoint manager sets the basic device properties for endpoints.</span></span> <span data-ttu-id="71880-117">O Gerenciador de pontos de extremidade é o componente do Windows Vista que é responsável por detectar a presença de dispositivos de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="71880-117">The endpoint manager is the Windows Vista component that is responsible for detecting the presence of audio endpoint devices.</span></span>

<span data-ttu-id="71880-118">Cada \_ identificador de propriedade PKEY xxx na lista a seguir é uma constante do tipo **PROPERTYKEY** que é definida no arquivo de cabeçalho Functiondiscoverykeys \_ devpkey. h.</span><span class="sxs-lookup"><span data-stu-id="71880-118">Each PKEY\_Xxx property identifier in the following list is a constant of type **PROPERTYKEY** that is defined in header file Functiondiscoverykeys\_devpkey.h.</span></span> <span data-ttu-id="71880-119">Todos os dispositivos de ponto de extremidade de áudio têm essas três propriedades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71880-119">All audio endpoint devices have these three device properties.</span></span>



| <span data-ttu-id="71880-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="71880-120">Property</span></span>                                                                         | <span data-ttu-id="71880-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="71880-121">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71880-122">**PKEY \_ DeviceInterface \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="71880-122">**PKEY\_DeviceInterface\_FriendlyName**</span></span>](pkey-deviceinterface-friendlyname.md) | <span data-ttu-id="71880-123">O nome amigável do adaptador de áudio ao qual o dispositivo de ponto de extremidade está anexado (por exemplo, "adaptador de áudio XYZ").</span><span class="sxs-lookup"><span data-stu-id="71880-123">The friendly name of the audio adapter to which the endpoint device is attached (for example, "XYZ Audio Adapter").</span></span> <span data-ttu-id="71880-124">**PROPVARIANT** member **VT** está definido como VT \_ LPWSTR e member **pwszVal** aponta para uma cadeia de caracteres largos terminada em nulo que contém o nome amigável.</span><span class="sxs-lookup"><span data-stu-id="71880-124">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the friendly name.</span></span> |
| [<span data-ttu-id="71880-125">**PKEY \_ dispositivo \_ DeviceDesc**</span><span class="sxs-lookup"><span data-stu-id="71880-125">**PKEY\_Device\_DeviceDesc**</span></span>](pkey-device-devicedesc.md)                       | <span data-ttu-id="71880-126">A descrição do dispositivo do ponto de extremidade do dispositivo (por exemplo, "alto-falantes").</span><span class="sxs-lookup"><span data-stu-id="71880-126">The device description of the endpoint device (for example, "Speakers").</span></span> <span data-ttu-id="71880-127">**PROPVARIANT** member **VT** está definido como VT \_ LPWSTR e member **pwszVal** aponta para uma cadeia de caracteres largos terminada em nulo que contém a descrição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71880-127">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the device description.</span></span>                                       |
| [<span data-ttu-id="71880-128">**PKEY do \_ dispositivo \_ amigável**</span><span class="sxs-lookup"><span data-stu-id="71880-128">**PKEY\_Device\_FriendlyName**</span></span>](pkey-device-friendlyname.md)                   | <span data-ttu-id="71880-129">O nome amigável do dispositivo de ponto de extremidade (por exemplo, "alto-falantes (adaptador de áudio XYZ)").</span><span class="sxs-lookup"><span data-stu-id="71880-129">The friendly name of the endpoint device (for example, "Speakers (XYZ Audio Adapter)").</span></span> <span data-ttu-id="71880-130">**PROPVARIANT** member **VT** está definido como VT \_ LPWSTR e member **pwszVal** aponta para uma cadeia de caracteres largos terminada em nulo que contém o nome amigável.</span><span class="sxs-lookup"><span data-stu-id="71880-130">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the friendly name.</span></span>                             |



 

<span data-ttu-id="71880-131">Alguns dispositivos de ponto de extremidade de áudio podem ter propriedades adicionais que não aparecem na lista anterior.</span><span class="sxs-lookup"><span data-stu-id="71880-131">Some audio endpoint devices might have additional properties that do not appear in the preceding list.</span></span> <span data-ttu-id="71880-132">Para obter mais informações sobre propriedades adicionais, consulte [Propriedades do ponto de extremidade de áudio](audio-endpoint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="71880-132">For more information about additional properties, see [Audio Endpoint Properties](audio-endpoint-properties.md).</span></span> <span data-ttu-id="71880-133">Para obter mais informações sobre o **PROPERTYKEY**, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="71880-133">For more information about **PROPERTYKEY**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="71880-134">O exemplo de código a seguir imprime os nomes de exibição de todos os dispositivos de ponto de extremidade de renderização de áudio no sistema:</span><span class="sxs-lookup"><span data-stu-id="71880-134">The following code example prints the display names of all audio-rendering endpoint devices in the system:</span></span>


```C++
//-----------------------------------------------------------
// This function enumerates all active (plugged in) audio
// rendering endpoint devices. It prints the friendly name
// and endpoint ID string of each endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

void PrintEndpointNames()
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDeviceCollection *pCollection = NULL;
    IMMDevice *pEndpoint = NULL;
    IPropertyStore *pProps = NULL;
    LPWSTR pwszID = NULL;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->EnumAudioEndpoints(
                        eRender, DEVICE_STATE_ACTIVE,
                        &pCollection);
    EXIT_ON_ERROR(hr)

    UINT  count;
    hr = pCollection->GetCount(&count);
    EXIT_ON_ERROR(hr)

    if (count == 0)
    {
        printf("No endpoints found.\n");
    }

    // Each loop prints the name of an endpoint device.
    for (ULONG i = 0; i < count; i++)
    {
        // Get pointer to endpoint number i.
        hr = pCollection->Item(i, &pEndpoint);
        EXIT_ON_ERROR(hr)

        // Get the endpoint ID string.
        hr = pEndpoint->GetId(&pwszID);
        EXIT_ON_ERROR(hr)
        
        hr = pEndpoint->OpenPropertyStore(
                          STGM_READ, &pProps);
        EXIT_ON_ERROR(hr)

        PROPVARIANT varName;
        // Initialize container for property value.
        PropVariantInit(&varName);

        // Get the endpoint's friendly-name property.
        hr = pProps->GetValue(
                       PKEY_Device_FriendlyName, &varName);
        EXIT_ON_ERROR(hr)

        // Print endpoint friendly name and endpoint ID.
        printf("Endpoint %d: \"%S\" (%S)\n",
               i, varName.pwszVal, pwszID);

        CoTaskMemFree(pwszID);
        pwszID = NULL;
        PropVariantClear(&varName);
        SAFE_RELEASE(pProps)
        SAFE_RELEASE(pEndpoint)
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    return;

Exit:
    printf("Error!\n");
    CoTaskMemFree(pwszID);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    SAFE_RELEASE(pEndpoint)
    SAFE_RELEASE(pProps)
}
```



<span data-ttu-id="71880-135">A macro com falha no exemplo de código anterior é definida no arquivo de cabeçalho Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="71880-135">The FAILED macro in the preceding code example is defined in header file Winerror.h.</span></span>

<span data-ttu-id="71880-136">No exemplo de código anterior, o corpo **de loop for** na função fotoendpointnames chama o método [**IMMDevice:: GetID**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obter a cadeia de caracteres de ID do ponto de [extremidade](endpoint-id-strings.md) para o dispositivo de ponto de extremidade de áudio representado pela instância da interface **IMMDevice** .</span><span class="sxs-lookup"><span data-stu-id="71880-136">In the preceding code example, the **for**-loop body in the PrintEndpointNames function calls the [**IMMDevice::GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) method to obtain the [endpoint ID string](endpoint-id-strings.md) for the audio endpoint device that is represented by the **IMMDevice** interface instance.</span></span> <span data-ttu-id="71880-137">A cadeia de caracteres identifica exclusivamente o dispositivo em relação a todos os outros dispositivos de ponto de extremidade de áudio no sistema.</span><span class="sxs-lookup"><span data-stu-id="71880-137">The string uniquely identifies the device with respect to all of the other audio endpoint devices in the system.</span></span> <span data-ttu-id="71880-138">Um cliente pode usar a cadeia de caracteres de ID do ponto de extremidade para criar uma instância do dispositivo de ponto de extremidade de áudio em um momento posterior ou em um processo diferente chamando o método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .</span><span class="sxs-lookup"><span data-stu-id="71880-138">A client can use the endpoint ID string to create an instance of the audio endpoint device at a later time or in a different process by calling the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="71880-139">Os clientes devem tratar o conteúdo da cadeia de caracteres de ID do ponto de extremidade como opaco.</span><span class="sxs-lookup"><span data-stu-id="71880-139">Clients should treat the contents of the endpoint ID string as opaque.</span></span> <span data-ttu-id="71880-140">Ou seja, os clientes não devem tentar analisar o conteúdo da cadeia de caracteres para obter informações sobre o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71880-140">That is, clients should not attempt to parse the contents of the string to obtain information about the device.</span></span> <span data-ttu-id="71880-141">O motivo é que o formato da cadeia de caracteres é indefinido e pode mudar de uma implementação da API MMDevice para a próxima.</span><span class="sxs-lookup"><span data-stu-id="71880-141">The reason is that the string format is undefined and might change from one implementation of the MMDevice API to the next.</span></span>

<span data-ttu-id="71880-142">Os nomes de dispositivo amigáveis e as cadeias de caracteres de ID de ponto de extremidade obtidos pela função fotoendpointnames no exemplo de código anterior são idênticos aos nomes de dispositivo amigáveis e cadeias de caracteres de ID de ponto de extremidade fornecidos pelo DirectSound durante a enumeração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71880-142">The friendly device names and endpoint ID strings that are obtained by the PrintEndpointNames function in the preceding code example are identical to the friendly device names and endpoint ID strings that are provided by DirectSound during device enumeration.</span></span> <span data-ttu-id="71880-143">Para obter mais informações, consulte [eventos de áudio para aplicativos de áudio herdados](audio-events-for-legacy-audio-applications.md).</span><span class="sxs-lookup"><span data-stu-id="71880-143">For more information, see [Audio Events for Legacy Audio Applications](audio-events-for-legacy-audio-applications.md).</span></span>

<span data-ttu-id="71880-144">No exemplo de código anterior, a função fotoendpointnames chama a função **CoCreateInstance** para criar um enumerador para os dispositivos de ponto de extremidade de áudio no sistema.</span><span class="sxs-lookup"><span data-stu-id="71880-144">In the preceding code example, the PrintEndpointNames function calls the **CoCreateInstance** function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="71880-145">A menos que o programa de chamada chamou anteriormente a função **CoInitialize** ou **CoInitializeEx** para inicializar a biblioteca com, a chamada **CoCreateInstance** falhará.</span><span class="sxs-lookup"><span data-stu-id="71880-145">Unless the calling program previously called either the **CoInitialize** or **CoInitializeEx** function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="71880-146">Para obter mais informações sobre **CoCreateInstance**, **CoInitialize** e **CoInitializeEx**, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="71880-146">For more information about **CoCreateInstance**, **CoInitialize**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="71880-147">Para obter mais informações sobre as interfaces **IMMDeviceEnumerator**, **IMMDeviceCollection** e **IMMDevice** , consulte [MMDevice API](mmdevice-api.md).</span><span class="sxs-lookup"><span data-stu-id="71880-147">For more information about the **IMMDeviceEnumerator**, **IMMDeviceCollection**, and **IMMDevice** interfaces, see [MMDevice API](mmdevice-api.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="71880-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71880-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71880-149">Dispositivos de ponto de extremidade de áudio</span><span class="sxs-lookup"><span data-stu-id="71880-149">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> </dl>

 

 



