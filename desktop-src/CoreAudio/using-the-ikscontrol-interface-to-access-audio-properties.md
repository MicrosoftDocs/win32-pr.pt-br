---
description: Usando a interface IKsControl para acessar as propriedades de áudio
ms.assetid: 72bf9164-96c6-4543-b858-19480b032fdb
title: Usando a interface IKsControl para acessar as propriedades de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a67639a0e51334da80b7bff88293414a58bb204c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164081"
---
# <a name="using-the-ikscontrol-interface-to-access-audio-properties"></a>Usando a interface IKsControl para acessar as propriedades de áudio

Em casos raros, um aplicativo de áudio especializado pode precisar usar a interface [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) para acessar determinados recursos de hardware de um adaptador de áudio que não são expostos pela [API do DEVICETOPOLOGY](devicetopology-api.md) ou pela API do [MMDevice](mmdevice-api.md). A interface **IKsControl** torna as propriedades, os eventos e os métodos de dispositivos de streaming de kernel (KS) disponíveis para aplicativos de modo de usuário. De interesse principal para aplicativos de áudio são propriedades KS. A interface **IKsControl** pode ser usada em conjunto com a API DeviceTopology e a API MMDevice para acessar as propriedades KS dos adaptadores de áudio.

A interface [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) é destinada principalmente para uso por fornecedores de hardware que escrevem aplicativos de painel de controle para gerenciar seu hardware de áudio. O **IKsControl** é menos útil para aplicativos de áudio de uso geral que não estão vinculados a dispositivos de hardware específicos. O motivo é que os fornecedores de hardware geralmente implementam mecanismos proprietários para acessar as propriedades de áudio de seus dispositivos. Ao contrário da API DeviceTopology, que oculta peculiaridades de driver específicas de hardware e fornece uma interface relativamente uniforme para acessar propriedades de áudio, os aplicativos usam o **IKsControl** para se comunicar diretamente com os drivers. Para obter mais informações sobre o **IKsControl**, consulte a documentação do Windows DDK.

Conforme discutido em [topologias de dispositivo](device-topologies.md), uma subunidade na topologia de um dispositivo de adaptador pode dar suporte a uma ou mais das interfaces de controle específicas de função mostradas na coluna à esquerda da tabela a seguir. Cada entrada na coluna à direita da tabela é a propriedade KS que corresponde à interface de controle à esquerda. A interface de controle fornece acesso conveniente à propriedade. A maioria dos drivers de áudio usa propriedades KS para representar os recursos de processamento específicos da função das subunidades (também chamadas de nós KS) nas topologias de seus adaptadores de áudio. Para obter mais informações sobre as propriedades KS e os nós KS, consulte a documentação do Windows DDK.



| Interface de controle                                          | Propriedade KS                        |
|------------------------------------------------------------|------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | KSPROPERTY de \_ áudio \_ AGC             |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | \_áudio KSPROPERTY \_ Bass            |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | \_configuração do \_ canal de áudio KSPROPERTY \_ |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | \_origem do \_ MUX de áudio KSPROPERTY \_     |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | \_intensidade de áudio KSPROPERTY \_        |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | KSPROPERTY de \_ áudio \_ mid             |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | \_áudio KSPROPERTY \_ mudo            |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | DEST KSPROPERTY de \_ áudio \_ Demux \_     |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | KSPROPERTY de \_ áudio \_ PEAKMETER       |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | KSPROPERTY de \_ áudio \_ agudo          |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | KSPROPERTY de \_ áudio \_ VOLUMELEVEL     |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | KSPROPERTY \_ de \_ desenvolvimento de áudio \_ específico   |



 

As topologias de alguns adaptadores de áudio podem conter subunidades que têm propriedades KS que não estão listadas na tabela anterior. Por exemplo, suponha que uma chamada para o método [**IPart:: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) para uma determinada subunidade recupere o valor de GUID KSNODETYPE \_ Tom. Esse GUID de subtipo indica que a subunidade dá suporte a uma ou mais das seguintes propriedades KS:

-   \_áudio KSPROPERTY \_ Bass
-   KSPROPERTY de \_ áudio \_ mid
-   KSPROPERTY de \_ áudio \_ agudo
-   \_aumento de \_ graves de áudio KSPROPERTY \_

As três primeiras propriedades dessa lista podem ser acessadas por meio das interfaces de controle que aparecem na tabela anterior, mas a \_ propriedade de aumento de graves de áudio KSPROPERTY \_ \_ não tem nenhuma interface de controle correspondente na API DeviceTopology. No entanto, um aplicativo pode usar a interface [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) para acessar essa propriedade, se a subunidade der suporte à propriedade.

As etapas a seguir são necessárias para acessar a \_ \_ propriedade de aumento de graves de áudio KSPROPERTY \_ de uma subunidade do Tom KSNODETYPE de subtipo \_ :

1.  Chame o método [**IConnector:: GetDeviceIdConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getdeviceidconnectedto) ou [**IDeviceTopology:: DeviceID**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) para obter a cadeia de caracteres de ID do dispositivo que identifica o dispositivo adaptador. Essa cadeia de caracteres é semelhante a uma [cadeia de caracteres de ID de ponto de extremidade](endpoint-id-strings.md), exceto que identifica um dispositivo de adaptador em vez de um dispositivo de ponto de extremidade Para obter mais informações sobre a diferença entre um dispositivo de adaptador e um dispositivo de ponto de extremidade, consulte [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md).
2.  Obtenha a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) do dispositivo de adaptador chamando o método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) com a cadeia de caracteres de ID do dispositivo. Essa interface **IMMDevice** é igual à interface descrita na **interface IMMDevice**, mas representa um dispositivo de adaptador em vez de um dispositivo de ponto de extremidade.
3.  Obtenha a interface [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) na subunidade chamando o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) com o parâmetro *IID* definido como **REFIID** IID \_ IKsControl. Observe que as interfaces suportadas por esse método **Activate** , que é para um dispositivo de adaptador, são diferentes das interfaces suportadas pelo método **Activate** para um dispositivo de ponto de extremidade. Em particular, o método **Activate** para um dispositivo de adaptador dá suporte a **IKsControl**.
4.  Chame o método [**IPart:: Getlocalid**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getlocalid) para obter a ID local da subunidade.
5.  Construa uma solicitação de propriedade KS. A ID do nó KS necessária para a solicitação está contida nos 16 bits menos significativos da ID local obtida na etapa anterior.
6.  Envie a solicitação de propriedade KS para o driver de áudio chamando o método [**IKsControl:: KsProperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) . Para obter mais informações sobre esse método, consulte a documentação do Windows DDK.

O exemplo de código a seguir recupera o valor da \_ propriedade de aumento de graves de áudio KSPROPERTY \_ \_ de uma subunidade do Tom KSNODETYPE de subtipo \_ :


```C++
//-----------------------------------------------------------
// This function calls the IKsControl::Property method to get
// the value of the KSPROPERTY_AUDIO_BASS_BOOST property of
// a subunit. Parameter pPart should point to a part that is
// a subunit with a subtype GUID value of KSNODETYPE_TONE.
//-----------------------------------------------------------
#define PARTID_MASK 0x0000ffff
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IKsControl = __uuidof(IKsControl);

HRESULT GetBassBoost(IMMDeviceEnumerator *pEnumerator,
                     IPart *pPart, BOOL *pbValue)
{
    HRESULT hr;
    IDeviceTopology *pTopology = NULL;
    IMMDevice *pPnpDevice = NULL;
    IKsControl *pKsControl = NULL;
    LPWSTR pwszDeviceId = NULL;

    if (pEnumerator == NULL || pPart == NULL || pbValue == NULL)
    {
        return E_INVALIDARG;
    }

    // Get the topology object for the adapter device that contains
    // the subunit represented by the IPart interface.
    hr = pPart->GetTopologyObject(&pTopology);
    EXIT_ON_ERROR(hr)

    // Get the device ID string that identifies the adapter device.
    hr = pTopology->GetDeviceId(&pwszDeviceId);
    EXIT_ON_ERROR(hr)

    // Get the IMMDevice interface of the adapter device object.
    hr = pEnumerator->GetDevice(pwszDeviceId, &pPnpDevice);
    EXIT_ON_ERROR(hr)

    // Activate an IKsControl interface on the adapter device object.
    hr = pPnpDevice->Activate(IID_IKsControl, CLSCTX_ALL, NULL, (void**)&pKsControl);
    EXIT_ON_ERROR(hr)

    // Get the local ID of the subunit (contains the KS node ID).
    UINT localId = 0;
    hr = pPart->GetLocalId(&localId);
    EXIT_ON_ERROR(hr)

    KSNODEPROPERTY_AUDIO_CHANNEL ksprop;
    ZeroMemory(&ksprop, sizeof(ksprop));
    ksprop.NodeProperty.Property.Set = KSPROPSETID_Audio;
    ksprop.NodeProperty.Property.Id = KSPROPERTY_AUDIO_BASS_BOOST;
    ksprop.NodeProperty.Property.Flags = KSPROPERTY_TYPE_GET | KSPROPERTY_TYPE_TOPOLOGY;
    ksprop.NodeProperty.NodeId = localId & PARTID_MASK;
    ksprop.Channel = 0;

    // Send the property request.to the device driver.
    BOOL bValue = FALSE;
    ULONG valueSize;
    hr = pKsControl->KsProperty(
                         &ksprop.NodeProperty.Property, sizeof(ksprop),
                         &bValue, sizeof(bValue), &valueSize);
    EXIT_ON_ERROR(hr)

    *pbValue = bValue;

Exit:
    SAFE_RELEASE(pTopology)
    SAFE_RELEASE(pPnpDevice)
    SAFE_RELEASE(pKsControl)
    CoTaskMemFree(pwszDeviceId);
    return hr;
}

```



No exemplo de código anterior, a função GetBassBoost usa os três parâmetros a seguir:

-   `pEnumerator` aponta para a interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) de um enumerador de ponto de extremidade de áudio.
-   `pPart` aponta para a interface [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) de uma subunidade que tem um subtipo de \_ Tom KSNODETYPE.
-   `pbValue` aponta para uma variável **bool** na qual a função grava o valor da propriedade.

Um programa chama GetBassBoost somente depois de chamar [**IPart:: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) e determina que o subtipo da subunidade é KSNODETYPE \_ Tom. O valor da propriedade será **true** se o aumento de graves estiver habilitado. Será **false** se o aumento de graves estiver desabilitado.

No início da função GetBassBoost, a chamada para o método [**IPart:: Gettopologiaobject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) Obtém a interface [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) do dispositivo de adaptador que contém a \_ subunidade de Tom KSNODETYPE. A chamada do método [**IDeviceTopology:: DeviceID**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) recupera a cadeia de caracteres de ID do dispositivo que identifica o dispositivo adaptador. A chamada do método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) usa a cadeia de caracteres de ID do dispositivo como um parâmetro de entrada e recupera a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) do dispositivo adaptador. Em seguida, a chamada de método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) recupera a interface [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) da subunidade. Para obter mais informações sobre a interface **IKsControl** , consulte a documentação do Windows DDK.

Em seguida, o exemplo de código anterior cria uma estrutura de [**\_ \_ canal de áudio KSNODEPROPERTY**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) que descreve a propriedade de aumento de graves. O exemplo de código passa um ponteiro para a estrutura para o método [**IKsControl:: KsProperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) , que usa as informações na estrutura para recuperar o valor da propriedade. Para obter mais informações sobre a estrutura do **\_ \_ canal de áudio KSNODEPROPERTY** e o método **IKsControl:: KsProperty** , consulte a documentação do Windows DDK.

O hardware de áudio normalmente atribui um estado de aumento de graves e separado a cada canal em um fluxo de áudio. Em princípio, o aumento dos graves pode ser habilitado para alguns canais e desabilitado para outros. A estrutura do [**\_ \_ canal de áudio KSNODEPROPERTY**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) contém um membro do **canal** que especifica o número do canal. Se um fluxo contiver *N* canais, os canais serão numerados de 0 a *N*– 1. O exemplo de código anterior Obtém o valor da propriedade Bass-Boost somente para o canal 0. Essa implementação implicitamente supõe que as propriedades de aumento de graves para todos os canais são definidas uniformemente para o mesmo estado. Assim, a leitura da propriedade Bass-Boost para o canal 0 é suficiente para determinar o valor da propriedade Bass-Boost para o fluxo. Para ser consistente com essa suposição, uma função correspondente para definir a propriedade Bass-Boost definiria todos os canais com o mesmo valor da propriedade Bass-Boost. Essas são convenções razoáveis, mas nem todos os fornecedores de hardware as seguem necessariamente. Por exemplo, um fornecedor pode fornecer um aplicativo de painel de controle que permita o aumento de graves apenas para canais que conduzem os alto-falantes do espectro completo. (Um palestrante de intervalo completo é capaz de reproduzir sons em todo o intervalo de baixo a agudos.) Nesse caso, o valor da propriedade recuperado pelo exemplo de código anterior pode não representar com precisão o estado de aumento de graves do fluxo.

Os clientes que usam as interfaces de controle listadas na tabela anterior podem chamar o método [**IPart:: RegisterControlChangeCallback**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-registercontrolchangecallback) para se registrarem para notificações quando o valor de um parâmetro de controle for alterado. Observe que a interface [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) não fornece um meio semelhante para os clientes se registrarem para notificações quando um valor de propriedade for alterado. Se **IKsControl** tiver suportado as notificações de alteração de propriedade, ele poderia informar um aplicativo quando outro aplicativo alterou um valor de propriedade. No entanto, ao contrário dos controles mais comumente usados que são monitorados por meio de notificações [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) , as propriedades gerenciadas pelo **IKsControl** são destinadas principalmente para uso por fornecedores de hardware, e essas propriedades provavelmente serão alteradas apenas por aplicativos do painel de controle gravados pelos fornecedores. Se um aplicativo precisar detectar alterações de propriedade feitas por outro aplicativo, ele poderá detectar as alterações periodicamente sondando o valor da propriedade por meio de **IKsControl**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação](programming-guide.md)
</dt> </dl>

 

 
