---
description: Eventos de dispositivo
ms.assetid: b31500d6-a79d-4e6e-878e-6bd77055f1ad
title: Eventos de dispositivo (APIs de áudio de núcleo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0513fc49ee5f3cb2bfe95ca2330cb79b74720923
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748850"
---
# <a name="device-events-core-audio-apis"></a>Eventos de dispositivo (APIs de áudio de núcleo)

Um evento de dispositivo notifica os clientes sobre uma alteração no status de um [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md) no sistema. Veja a seguir exemplos de eventos de dispositivo:

-   O usuário habilita ou desabilita um dispositivo de ponto de extremidade de áudio de Gerenciador de Dispositivos ou do painel de controle multimídia do Windows Mmsys.cpl.
-   O usuário adiciona um adaptador de áudio ao sistema ou remove um adaptador de áudio do sistema.
-   O usuário conecta um dispositivo de ponto de extremidade de áudio em uma tomada de áudio com detecção de presença de Jack ou remove um dispositivo de ponto de extremidade de áudio desse conector.
-   O usuário altera a [função de dispositivo](device-roles.md) atribuída a um dispositivo.
-   O valor de uma [propriedade de um dispositivo](device-properties.md) é alterado.

A adição ou remoção de um adaptador de áudio gera eventos de dispositivo para todos os dispositivos de ponto de extremidade de áudio que se conectam ao adaptador. Os primeiros quatro itens na lista anterior são exemplos de alterações de estado do dispositivo. Para obter mais informações sobre os Estados do dispositivo de dispositivos de ponto de extremidade de áudio, consulte [constantes do estado do dispositivo \_ \_ xxx](device-state-xxx-constants.md). Para obter mais informações sobre a detecção de presença de Jack, consulte [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md).

Um cliente pode se registrar para ser notificado quando ocorrerem eventos de dispositivo. Em resposta a essas notificações, o cliente pode alterar dinamicamente a forma como ele usa um dispositivo específico ou selecionar um dispositivo diferente a ser usado para uma finalidade específica.

Por exemplo, se um aplicativo estiver reproduzindo uma faixa de áudio por meio de um conjunto de alto-falantes USB e o usuário desconectar os alto-falantes do conector USB, o aplicativo receberá uma notificação de evento do dispositivo. Em resposta ao evento, se o aplicativo detectar que um conjunto de alto-falantes da área de trabalho está conectado ao adaptador de áudio integrado na placa-mãe do sistema, o aplicativo poderá continuar jogando a faixa de áudio nos alto-falantes da área de trabalho. Neste exemplo, a transição de alto-falantes USB para alto-falantes de área de trabalho ocorre automaticamente, sem a necessidade de o usuário intervir redirecionando explicitamente o aplicativo.

Para se registrar para receber notificações de dispositivo, um cliente chama o método [**IMMDeviceEnumerator:: RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) . Quando o cliente não requer mais notificações, ele os cancela chamando o método [**IMMDeviceEnumerator:: UnregisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) . Ambos os métodos usam um parâmetro de entrada, chamado *pNotify*, que é um ponteiro para uma instância de interface [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) .

A interface **IMMNotificationClient** é implementada por um cliente. A interface contém vários métodos, sendo que cada um serve como uma rotina de retorno de chamada para um determinado tipo de evento de dispositivo. Quando um evento de dispositivo ocorre em um dispositivo de ponto de extremidade de áudio, o módulo MMDevice chama o método apropriado na interface **IMMNotificationClient** de cada cliente que está atualmente registrado para receber notificações de eventos de dispositivo. Essas chamadas passam uma descrição do evento para os clientes. Para obter mais informações, consulte [**interface IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).

Um cliente registrado para receber notificações de eventos de dispositivo receberá notificações de todos os tipos de eventos de dispositivo que ocorrem em todos os dispositivos de ponto de extremidade de áudio no sistema. Se um cliente estiver interessado apenas em determinados tipos de evento ou em determinados dispositivos, os métodos em sua implementação **IMMNotificationClient** deverão filtrar os eventos adequadamente.

O SDK do Windows fornece exemplos que incluem várias implementações para a [**interface IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient). Para obter mais informações, consulte [exemplos de SDK que usam as APIs de áudio de núcleo](sdk-samples-that-use-the-core-audio-apis.md).

O exemplo de código a seguir mostra uma implementação possível da interface **IMMNotificationClient** :


```C++
//-----------------------------------------------------------
// Example implementation of IMMNotificationClient interface.
// When the status of audio endpoint devices change, the
// MMDevice module calls these methods to notify the client.
//-----------------------------------------------------------

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class CMMNotificationClient : public IMMNotificationClient
{
    LONG _cRef;
    IMMDeviceEnumerator *_pEnumerator;

    // Private function to print device-friendly name
    HRESULT _PrintDeviceName(LPCWSTR  pwstrId);

public:
    CMMNotificationClient() :
        _cRef(1),
        _pEnumerator(NULL)
    {
    }

    ~CMMNotificationClient()
    {
        SAFE_RELEASE(_pEnumerator)
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IMMNotificationClient) == riid)
        {
            AddRef();
            *ppvInterface = (IMMNotificationClient*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback methods for device-event notifications.

    HRESULT STDMETHODCALLTYPE OnDefaultDeviceChanged(
                                EDataFlow flow, ERole role,
                                LPCWSTR pwstrDeviceId)
    {
        char  *pszFlow = "?????";
        char  *pszRole = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (flow)
        {
        case eRender:
            pszFlow = "eRender";
            break;
        case eCapture:
            pszFlow = "eCapture";
            break;
        }

        switch (role)
        {
        case eConsole:
            pszRole = "eConsole";
            break;
        case eMultimedia:
            pszRole = "eMultimedia";
            break;
        case eCommunications:
            pszRole = "eCommunications";
            break;
        }

        printf("  -->New default device: flow = %s, role = %s\n",
               pszFlow, pszRole);
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceAdded(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Added device\n");
        return S_OK;
    };

    HRESULT STDMETHODCALLTYPE OnDeviceRemoved(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Removed device\n");
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceStateChanged(
                                LPCWSTR pwstrDeviceId,
                                DWORD dwNewState)
    {
        char  *pszState = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (dwNewState)
        {
        case DEVICE_STATE_ACTIVE:
            pszState = "ACTIVE";
            break;
        case DEVICE_STATE_DISABLED:
            pszState = "DISABLED";
            break;
        case DEVICE_STATE_NOTPRESENT:
            pszState = "NOTPRESENT";
            break;
        case DEVICE_STATE_UNPLUGGED:
            pszState = "UNPLUGGED";
            break;
        }

        printf("  -->New device state is DEVICE_STATE_%s (0x%8.8x)\n",
               pszState, dwNewState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnPropertyValueChanged(
                                LPCWSTR pwstrDeviceId,
                                const PROPERTYKEY key)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Changed device property "
               "{%8.8x-%4.4x-%4.4x-%2.2x%2.2x-%2.2x%2.2x%2.2x%2.2x%2.2x%2.2x}#%d\n",
               key.fmtid.Data1, key.fmtid.Data2, key.fmtid.Data3,
               key.fmtid.Data4[0], key.fmtid.Data4[1],
               key.fmtid.Data4[2], key.fmtid.Data4[3],
               key.fmtid.Data4[4], key.fmtid.Data4[5],
               key.fmtid.Data4[6], key.fmtid.Data4[7],
               key.pid);
        return S_OK;
    }
};

// Given an endpoint ID string, print the friendly device name.
HRESULT CMMNotificationClient::_PrintDeviceName(LPCWSTR pwstrId)
{
    HRESULT hr = S_OK;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;
    PROPVARIANT varString;

    CoInitialize(NULL);
    PropVariantInit(&varString);

    if (_pEnumerator == NULL)
    {
        // Get enumerator for audio endpoint devices.
        hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                              NULL, CLSCTX_INPROC_SERVER,
                              __uuidof(IMMDeviceEnumerator),
                              (void**)&_pEnumerator);
    }
    if (hr == S_OK)
    {
        hr = _pEnumerator->GetDevice(pwstrId, &pDevice);
    }
    if (hr == S_OK)
    {
        hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    }
    if (hr == S_OK)
    {
        // Get the endpoint device's friendly-name property.
        hr = pProps->GetValue(PKEY_Device_FriendlyName, &varString);
    }
    printf("----------------------\nDevice name: \"%S\"\n"
           "  Endpoint ID string: \"%S\"\n",
           (hr == S_OK) ? varString.pwszVal : L"null device",
           (pwstrId != NULL) ? pwstrId : L"null ID");

    PropVariantClear(&varString);

    SAFE_RELEASE(pProps)
    SAFE_RELEASE(pDevice)
    CoUninitialize();
    return hr;
}
```



A classe CMMNotificationClient no exemplo de código anterior é uma implementação da interface **IMMNotificationClient** . Como **IMMNotificationClient** é herdado de **IUnknown**, a definição de classe contém implementações dos métodos **IUnknown** **AddRef**, **Release** e **QueryInterface**. Os métodos públicos restantes na definição de classe são específicos para a interface **IMMNotificationClient** . Esses métodos são:

-   **OnDefaultDeviceChanged**, que é chamado quando o usuário altera a função de dispositivo de um dispositivo de ponto de extremidade de áudio.
-   **OnDeviceAdded**, que é chamado quando o usuário adiciona um dispositivo de ponto de extremidade de áudio ao sistema.
-   **OnDeviceRemoved**, que é chamado quando o usuário remove um dispositivo de ponto de extremidade de áudio do sistema.
-   **OnDeviceStateChanged**, que é chamado quando o estado do dispositivo de um dispositivo de ponto de extremidade de áudio é alterado. (Para obter mais informações sobre os Estados do dispositivo, consulte [constantes do estado do dispositivo \_ \_ xxx](device-state-xxx-constants.md).)
-   **Onvalordapropriedadechanged**, que é chamado quando o valor de uma propriedade de um dispositivo de ponto de extremidade de áudio é alterado.

Cada um desses métodos usa um parâmetro de entrada, *pwstrDeviceId*, que é um ponteiro para uma cadeia de caracteres de ID de ponto de extremidade. A cadeia de caracteres identifica o dispositivo de ponto de extremidade de áudio no qual o evento do dispositivo ocorreu.

No exemplo de código anterior, \_ printName é um método particular na classe CMMNotificationClient que imprime o nome amigável do dispositivo. \_O filedevicename usa a cadeia de caracteres de ID do ponto de extremidade como um parâmetro de entrada. Ele passa a cadeia de caracteres para o método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) . **GetDevice** cria um objeto de dispositivo de ponto de extremidade para representar o dispositivo e fornece a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) para esse objeto. Em seguida, o \_ Revicename chama o método [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) para recuperar a interface **IPropertyStore** para o armazenamento de propriedades do dispositivo. Por fim, o renome do \_ dispositivo chama o método **IPropertyStore:: GetItem** para obter a propriedade friendly-Name do dispositivo. Para obter mais informações sobre o **IPropertyStore**, consulte a documentação do SDK do Windows.

Além dos eventos de dispositivo, os clientes podem se registrar para receber notificações de eventos de sessão de áudio e eventos de volume de ponto de extremidade. Para obter mais informações, consulte [**interface IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e [**interface IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md)
</dt> </dl>

 

 



