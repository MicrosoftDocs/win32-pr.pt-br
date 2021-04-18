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
# <a name="implementing-a-custom-audio-endpoint-enumerator"></a>Implementando um enumerador de ponto de extremidade de áudio personalizado

A partir do Windows Server 2008 R2, você pode implementar um enumerador personalizado de ponto de extremidade de áudio remoto como parte de um provedor de protocolo Área de Trabalho Remota. Um provedor de protocolo Área de Trabalho Remota pode usar um enumerador de ponto de extremidade de áudio personalizado para recuperar uma coleção de pontos de extremidades de áudio que têm um conjunto específico de recursos.

**Para implementar um enumerador personalizado de ponto de extremidade de áudio remoto**

1.  Sua solução de enumerador de ponto de extremidade personalizado deve implementar quatro tipos principais de objetos: objetos de enumerador de dispositivo, objetos de coleção de dispositivos, objetos de dispositivo e objetos de armazenamento de propriedades.

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Tipo de Objeto</th>
    <th>Descrição</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Objeto enumerador de dispositivo<br/></td>
    <td>Um objeto de enumerador de dispositivo fornece a funcionalidade de enumerador de ponto de extremidade. Ele expõe métodos que retornam um ponto de extremidade padrão e coleções especificadas de pontos de extremidades. Por exemplo, dependendo dos critérios especificados, o enumerador pode retornar pontos de extremidade de comunicação, pontos de extremidade de reprodução ou capturar pontos de extremidade. O objeto enumerador de dispositivo deve implementar a interface <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator</strong></a> .<br/></td>
    </tr>
    <tr class="even">
    <td>Objeto de coleção de dispositivos<br/></td>
    <td>Um objeto de coleção de dispositivos representa uma coleção de dispositivos de áudio. Ele deve implementar a interface <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection</strong></a> .<br/></td>
    </tr>
    <tr class="odd">
    <td>Objeto de dispositivo<br/></td>
    <td>Um objeto de dispositivo representa um dispositivo de áudio específico. Ele fornece acesso ao armazenamento de propriedades do dispositivo de áudio e expõe as interfaces de reprodução e de captura de áudio disponíveis no dispositivo. O objeto de dispositivo deve implementar as interfaces <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>IMMDevice</strong></a> e <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> .<br/></td>
    </tr>
    <tr class="even">
    <td>Objeto de repositório de propriedades<br/></td>
    <td>Um objeto de repositório de propriedades expõe as propriedades associadas a um dispositivo de áudio. Algumas dessas propriedades são usadas pelo sistema, mas os aplicativos também podem armazenar propriedades arbitrárias com o ponto de extremidade de áudio.<br/> Todos os dispositivos de áudio têm as três propriedades a seguir:<br/>
    <ul>
    <li><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></li>
    <li><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></li>
    <li><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></li>
    </ul>
O objeto de repositório de propriedades deve implementar a interface <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> .<br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  O enumerador de ponto de extremidade personalizado deve ser implementado em uma DLL que pode ser carregada no sistema de áudio e em outros aplicativos. A DLL deve ser assinada para que processos seguros possam carregá-lo. A DLL deve implementar e exportar a função [**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md) , que atua como um ponto de entrada para o enumerador de ponto de extremidade personalizado.

O serviço de Serviços de Área de Trabalho Remota chama o método [**queryproperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) e define o parâmetro *QueryType* como **WTS \_ Query \_ AUDIOENUM \_ dll** para recuperar o nome do objeto enumerador.

Os objetos de enumerador personalizados usam interfaces semelhantes a COM e um mecanismo de contagem de referência semelhante a, mas não são objetos COM verdadeiros. O enumerador de ponto de extremidade personalizado deve ter a capacidade de trabalhar com interfaces de áudio herdadas usadas por aplicativos que não dão suporte a COM. Por esse motivo, o enumerador de ponto de extremidade personalizado não deve depender do mecanismo de gerenciamento do ciclo de vida do COM. Os consumidores do enumerador de ponto de extremidade de áudio, como MMDevAPI.dll, carregam a DLL do enumerador de ponto de extremidade personalizado quando exigido pelos aplicativos do usuário e não descarregam o enumerador, enquanto o enumerador mantém uma referência a um objeto de enumerador de dispositivo, objeto de coleção de dispositivos, objeto de dispositivo ou objeto de repositório de propriedades. No entanto, não é possível que esses consumidores acompanhem referências a outros tipos de objetos pertencentes ao enumerador de ponto de extremidade personalizado. Da mesma forma, recomendamos que seu enumerador de ponto de extremidade personalizado não crie nenhum objeto que possa sobreviver além esses quatro tipos de objetos.

## <a name="to-implement-a-custom-audio-endpoint"></a>Para implementar um ponto de extremidade de áudio personalizado

Para implementar um enumerador de dispositivo de áudio personalizado, você deve implementar um ponto de extremidade de áudio personalizado. A maneira como os dispositivos de áudio personalizados são vinculados é usando as duas instruções a seguir:

-   `IMMDevice::Activate(IAudioOutputEndpointRT)`
-   `IMMDevice::Activate(IAudioInputEndpointRT)`

Não esperamos que você implemente a lista completa de [**IMMDevice:: Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) interfaces no seu enumerador de dispositivo de áudio personalizado. Em vez disso, você deve implementar [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) e [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt). Opcionalmente, você pode implementar mais alguns, como [**IAudioEndpointVolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume). Para qualquer interface que você não implementar, você deve retornar **E \_ nointerface** (você deve usar esse código de falha específico). Em seguida, o Windows retornará a uma implementação de estoque da interface (por exemplo, [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).

Para obter mais documentação de referência sobre como implementar e registrar pontos de extremidade de áudio, consulte [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt). Para um diagrama que mostra como o WASAPI funciona, consulte [componentes de áudio do modo de usuário](/windows/desktop/CoreAudio/user-mode-audio-components). Observe que todo o áudio do modo de usuário é novo, começando com o Windows Server 2008.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um provedor de protocolo RDP](creating-a-custom-remote-protocol.md)
</dt> <dt>

[**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md)
</dt> <dt>

[**IMMDevice**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**IMMDeviceCollection**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
</dt> <dt>

[**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**IMMEndpoint**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint)
</dt> <dt>

[IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> </dl>