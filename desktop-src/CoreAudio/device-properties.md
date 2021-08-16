---
description: Propriedades do Dispositivo
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: Propriedades do dispositivo (APIs de áudio principal)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e1a5068329ea2da794b68b777aa989a2e8b4a665df082982916942aa15b56e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407014"
---
# <a name="device-properties-core-audio-apis"></a>Propriedades do dispositivo (APIs de áudio principal)

Durante o processo de enumeração de [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md), um aplicativo cliente pode interrogar os objetos de ponto de extremidade para suas propriedades de dispositivo. As propriedades do dispositivo são expostas na implementação da API do MMDevice da interface **IPropertyStore** . Dada uma referência à interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) de um objeto de ponto de extremidade, um cliente pode obter uma referência ao repositório de propriedades do objeto de ponto de extremidade chamando o método [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) .

O objeto de repositório de propriedades expõe uma interface **IPropertyStore** . Os dois métodos principais nessa interface são **IPropertyStore:: GetValue**, que obtém um valor de propriedade de dispositivo e **IPropertyStore:: SetValue**, que define um valor de propriedade de dispositivo. para obter mais informações sobre o **IPropertyStore**, consulte a documentação do SDK do Windows.

A implementação da API do MMDevice do repositório de propriedades é diferente do objeto de armazenamento de Propriedade do shell padrão. Para alterar um valor de propriedade, o aplicativo cliente deve chamar o método **IPropertyStore:: SetValue** . Durante essa chamada, os novos valores são definidos e gravados no registro. Portanto, o aplicativo não precisa chamar o método **IPropertyStore:: Commit** após a chamada **SetValue** . O identificador para o registro é fechado somente quando o cliente libera o ponteiro de interface.

Normalmente, aplicativos cliente de terceiros chamam o método **GetValue** , mas não o método **SetValue** . O Gerenciador de pontos de extremidade define as propriedades básicas do dispositivo para pontos de extremidade. o gerenciador de pontos de extremidade é o componente Windows do Vista que é responsável por detectar a presença de dispositivos de ponto de extremidade de áudio.

Cada \_ identificador de propriedade PKEY xxx na lista a seguir é uma constante do tipo **PROPERTYKEY** que é definida no arquivo de cabeçalho Functiondiscoverykeys \_ devpkey. h. Todos os dispositivos de ponto de extremidade de áudio têm essas três propriedades de dispositivo.



| Propriedade                                                                         | Descrição                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ DeviceInterface \_ FriendlyName**](pkey-deviceinterface-friendlyname.md) | O nome amigável do adaptador de áudio ao qual o dispositivo de ponto de extremidade está anexado (por exemplo, "adaptador de áudio XYZ"). **PROPVARIANT** member **VT** está definido como VT \_ LPWSTR e member **pwszVal** aponta para uma cadeia de caracteres largos terminada em nulo que contém o nome amigável. |
| [**PKEY \_ dispositivo \_ DeviceDesc**](pkey-device-devicedesc.md)                       | A descrição do dispositivo do ponto de extremidade do dispositivo (por exemplo, "alto-falantes"). **PROPVARIANT** member **VT** está definido como VT \_ LPWSTR e member **pwszVal** aponta para uma cadeia de caracteres largos terminada em nulo que contém a descrição do dispositivo.                                       |
| [**PKEY do \_ dispositivo \_ amigável**](pkey-device-friendlyname.md)                   | O nome amigável do dispositivo de ponto de extremidade (por exemplo, "alto-falantes (adaptador de áudio XYZ)"). **PROPVARIANT** member **VT** está definido como VT \_ LPWSTR e member **pwszVal** aponta para uma cadeia de caracteres largos terminada em nulo que contém o nome amigável.                             |



 

Alguns dispositivos de ponto de extremidade de áudio podem ter propriedades adicionais que não aparecem na lista anterior. Para obter mais informações sobre propriedades adicionais, consulte [Propriedades do ponto de extremidade de áudio](audio-endpoint-properties.md). para obter mais informações sobre o **PROPERTYKEY**, consulte a documentação do SDK do Windows.

O exemplo de código a seguir imprime os nomes de exibição de todos os dispositivos de ponto de extremidade de renderização de áudio no sistema:


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



A macro com falha no exemplo de código anterior é definida no arquivo de cabeçalho Winerror. h.

No exemplo de código anterior, o corpo **de loop for** na função fotoendpointnames chama o método [**IMMDevice:: GetID**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obter a cadeia de caracteres de ID do ponto de [extremidade](endpoint-id-strings.md) para o dispositivo de ponto de extremidade de áudio representado pela instância da interface **IMMDevice** . A cadeia de caracteres identifica exclusivamente o dispositivo em relação a todos os outros dispositivos de ponto de extremidade de áudio no sistema. Um cliente pode usar a cadeia de caracteres de ID do ponto de extremidade para criar uma instância do dispositivo de ponto de extremidade de áudio em um momento posterior ou em um processo diferente chamando o método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) . Os clientes devem tratar o conteúdo da cadeia de caracteres de ID do ponto de extremidade como opaco. Ou seja, os clientes não devem tentar analisar o conteúdo da cadeia de caracteres para obter informações sobre o dispositivo. O motivo é que o formato da cadeia de caracteres é indefinido e pode mudar de uma implementação da API MMDevice para a próxima.

Os nomes de dispositivo amigáveis e as cadeias de caracteres de ID de ponto de extremidade obtidos pela função fotoendpointnames no exemplo de código anterior são idênticos aos nomes de dispositivo amigáveis e cadeias de caracteres de ID de ponto de extremidade fornecidos pelo DirectSound durante a enumeração do dispositivo. Para obter mais informações, consulte [eventos de áudio para aplicativos de áudio herdados](audio-events-for-legacy-audio-applications.md).

No exemplo de código anterior, a função fotoendpointnames chama a função **CoCreateInstance** para criar um enumerador para os dispositivos de ponto de extremidade de áudio no sistema. A menos que o programa de chamada chamou anteriormente a função **CoInitialize** ou **CoInitializeEx** para inicializar a biblioteca com, a chamada **CoCreateInstance** falhará. para obter mais informações sobre **CoCreateInstance**, **coinitialize** e **CoInitializeEx**, consulte a documentação do SDK do Windows.

Para obter mais informações sobre as interfaces **IMMDeviceEnumerator**, **IMMDeviceCollection** e **IMMDevice** , consulte [MMDevice API](mmdevice-api.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md)
</dt> </dl>

 

 



