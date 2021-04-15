---
description: Topologias de dispositivo
ms.assetid: 5ac421e5-74a4-40e8-af6f-a99a05ebc3e0
title: Topologias de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e0af267bb4a0fa924ee23d36a2a615ac5ae7fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501101"
---
# <a name="device-topologies"></a>Topologias de dispositivo

A [API DeviceTopology](devicetopology-api.md) fornece aos clientes controle sobre uma variedade de funções internas de adaptadores de áudio que eles não podem acessar por meio da [API do MMDevice](mmdevice-api.md), do [WASAPI](wasapi.md)ou da [API do EndpointVolume](endpointvolume-api.md).

Conforme explicado anteriormente, a [API MMDevice](mmdevice-api.md), a [WASAPI](wasapi.md)e a [API EndpointVolume](endpointvolume-api.md) apresentam microfones, alto-falantes, fones de ouvido e outros dispositivos de entrada e saída de áudio para clientes como [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md). O modelo de dispositivo de ponto de extremidade fornece aos clientes acesso conveniente aos controles de volume e mudo em dispositivos de áudio. Os clientes que exigem apenas esses controles simples podem evitar percorrer as topologias internas de dispositivos de hardware em adaptadores de áudio.

No Windows Vista, o mecanismo de áudio configura automaticamente as topologias de dispositivos de áudio para uso por aplicativos de áudio. Assim, os aplicativos raramente, se nunca, precisam usar a API DeviceTopology para essa finalidade. Por exemplo, suponha que um adaptador de áudio contenha um multiplexador de entrada que possa capturar um fluxo de uma entrada de linha ou de um microfone, mas que não possa capturar fluxos de ambos os dispositivos de ponto de extremidade ao mesmo tempo. Suponha que o usuário habilitou aplicativos de modo exclusivo para apropriar o uso de um dispositivo de ponto de extremidade de áudio por aplicativos de modo compartilhado, conforme descrito em [fluxos de modo exclusivo](exclusive-mode-streams.md). Se um aplicativo de modo compartilhado estiver gravando um fluxo da entrada de linha no momento em que um aplicativo de modo exclusivo começar a gravar um fluxo do microfone, o mecanismo de áudio alternará automaticamente o multiplexador da entrada de linha para o microfone. Por outro lado, em versões anteriores do Windows, incluindo o Windows XP, o aplicativo de modo exclusivo neste exemplo usaria as funções **mixerXxx** na API de multimídia do Windows para atravessar as topologias dos dispositivos de adaptador, descobrir o multiplexador e configurar o multiplexador para selecionar a entrada do microfone. No Windows Vista, essas etapas não são mais necessárias.

No entanto, alguns clientes podem exigir controle explícito sobre os tipos de controles de hardware de áudio que não podem ser acessados por meio da API do MMDevice, do WASAPI ou da API do EndpointVolume. Para esses clientes, a API DeviceTopology fornece a capacidade de atravessar as topologias de dispositivos de adaptador para descobrir e gerenciar os controles de áudio nos dispositivos. Os aplicativos que usam a API DeviceTopology devem ser criados com cuidado para evitar interferir na política de áudio do Windows e perturbar as configurações internas de dispositivos de áudio que são compartilhados com outros aplicativos. Para obter mais informações sobre a política de áudio do Windows, consulte [componentes de áudio do modo de usuário](user-mode-audio-components.md).

A API DeviceTopology fornece interfaces para descobrir e gerenciar os seguintes tipos de controles de áudio em uma topologia de dispositivo:

-   Controle de lucro automático
-   Controle de baixo
-   Seletor de entrada (multiplexador)
-   Controle de intensidade
-   Controle de midrange
-   Controle sem áudio
-   Seletor de saída (demultiplexador)
-   Medidor de pico
-   Controle de agudos
-   Controle de volume

Além disso, a API do DeviceTopology permite que os clientes consultem os dispositivos do adaptador para obter informações sobre os formatos de fluxo para os quais dão suporte. O arquivo de cabeçalho Devicetopology. h define as interfaces na API DeviceTopology.

O diagrama a seguir mostra um exemplo de várias topologias de dispositivo conectadas para a parte de um adaptador PCI que captura áudio de um microfone, entrada de linha e CD player.

![exemplo de quatro topologias de dispositivo conectadas](images/fig2.jpg)

O diagrama anterior mostra os caminhos de dados que levam das entradas analógicas para o barramento do sistema. Cada um dos seguintes dispositivos é representado como um objeto de topologia de dispositivo com uma interface [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) :

-   Dispositivo de captura de som wave
-   Dispositivo Multiplexador de entrada
-   Dispositivo de ponto de extremidade A
-   Ponto de extremidade dispositivo B

Observe que o diagrama de topologia combina dispositivos de adaptador (os dispositivos de captura de onda e multiplexador de entrada) com dispositivos de ponto de extremidade. Através das conexões entre dispositivos, os dados de áudio passam de um dispositivo para o outro. Em cada lado de uma conexão, há um conector (rotulado como con no diagrama) por meio do qual os dados entram ou saem de um dispositivo.

Na borda esquerda do diagrama, os sinais da entrada de linha e dos conectores de microfone inserem os dispositivos de ponto de extremidade.

Dentro do dispositivo de captura de som wave e do dispositivo Multiplexador de entrada estão as funções de processamento de fluxo, que, na terminologia da API DeviceTopology, são chamadas de subunidades. Os seguintes tipos de subunidades aparecem no diagrama anterior:

-   Controle de volume (rotulado como vol)
-   Controle sem áudio (rotulado sem som)
-   Multiplexador (ou seletor de entrada; rotulado como MUX)
-   Conversor de analógico para digital (rotulado como ADC)

As configurações nas subunidades de volume, mudo e multiplexador podem ser controladas por clientes e a API DeviceTopology fornece interfaces de controle aos clientes para controlá-las. Neste exemplo, a subunidade ADC não tem configurações de controle. Assim, a API DeviceTopology não fornece nenhuma interface de controle para o ADC.

Na terminologia da API do DeviceTopology, os conectores e as subunidades pertencem à mesma categoria geral – partes. Todas as partes, independentemente de serem conectores ou subunidades, fornecem um conjunto comum de funções. A API DeviceTopology implementa uma interface [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) para representar as funções genéricas que são comuns a conectores e subunidades. A API implementa as interfaces [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) e [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) para representar os aspectos específicos de conectores e subunidades.

A API DeviceTopology constrói as topologias do dispositivo de captura de onda e do dispositivo Multiplexador de entrada dos filtros de streaming de kernel (KS) que o driver de áudio expõe ao sistema operacional para representar esses dispositivos. (O driver do adaptador de áudio implementa as interfaces **IMiniportWaveXxx** e **IMiniportTopology** para representar as partes dependentes de hardware desses filtros; para obter mais informações sobre essas interfaces e sobre filtros KS, consulte a documentação do Windows DDK.)

A API DeviceTopology constrói topologias triviais para representar os dispositivos de ponto de extremidade A e B no diagrama anterior. A topologia do dispositivo de um dispositivo de ponto de extremidade consiste em um único conector. Essa topologia é meramente um espaço reservado para o dispositivo de ponto de extremidade e não contém nenhuma subunidade para o processamento de dados de áudio. Na verdade, os dispositivos de adaptador contêm todas as subunidades que os aplicativos cliente usam para controlar o processamento de áudio. A topologia do dispositivo de um dispositivo de ponto de extremidade serve principalmente como um ponto de partida para explorar as topologias de dispositivo dos dispositivos de adaptador.

Conexões internas entre duas partes em uma topologia de dispositivo são chamadas de links. A API DeviceTopology fornece métodos para atravessar links de uma parte para a próxima em uma topologia de dispositivo. A API também fornece métodos para percorrer as conexões entre as topologias de dispositivo.

Para iniciar a exploração de um conjunto de topologias de dispositivo conectadas, um aplicativo cliente ativa a interface **IDeviceTopology** de um dispositivo de ponto de extremidade de áudio. O conector em um dispositivo de ponto de extremidade se conecta a um conector em um adaptador de áudio ou a uma rede. Se o ponto de extremidade se conectar a um dispositivo em um adaptador de áudio, os métodos na API DeviceTopology permitirão que o aplicativo passe pela conexão do ponto de extremidade para o adaptador, obtendo uma referência à interface **IDeviceTopology** do dispositivo adaptador no outro lado da conexão. Uma rede, por outro lado, não tem nenhuma topologia de dispositivo. Uma conexão de rede canaliza um fluxo de áudio para um cliente que está acessando o sistema remotamente.

A API DeviceTopology fornece acesso apenas às topologias dos dispositivos de hardware em um adaptador de áudio. Os dispositivos externos na borda esquerda do diagrama e os componentes de software na borda direita estão além do escopo da API. As linhas tracejadas em cada lado do diagrama representam os limites da API DeviceTopology. O cliente pode usar a API para explorar um caminho de dados que se estende do conector de entrada para o barramento do sistema, mas a API não pode penetrar além desses limites.

Cada conector no diagrama anterior tem um tipo de conexão associado que indica o tipo de conexão que o conector faz. Assim, os conectores nos dois lados de uma conexão sempre têm tipos de conexão idênticos. O tipo de conexão é indicado por um valor de enumeração [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) — físico \_ externo, físico \_ interno, software \_ fixo, \_ e/s de software ou rede. As conexões entre o dispositivo Multiplexador de entrada e os dispositivos de ponto de extremidade A e B são do tipo físico \_ externo, o que significa que a conexão representa uma conexão física com um dispositivo externo (em outras palavras, uma tomada de áudio acessível pelo usuário). A conexão com o sinal analógico do CD player interno é do tipo físico \_ interno, que indica uma conexão física com um dispositivo auxiliar que é instalado dentro do chassi do sistema. A conexão entre o dispositivo de captura de onda e o dispositivo Multiplexador de entrada é do tipo software \_ fixo, que indica uma conexão permanente que é fixa e não pode ser configurada no controle de software. Por fim, a conexão com o barramento do sistema no lado direito do diagrama é do tipo software \_ Io, que indica que a e/s de dados para a conexão é implementada por um mecanismo de DMA sob controle de software. (O diagrama não inclui um exemplo de tipo de conexão de rede.)

O cliente começa a atravessar um caminho de dados no dispositivo de ponto de extremidade. Primeiro, o cliente obtém uma interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) que representa o dispositivo de ponto de extremidade, conforme explicado em [enumerando dispositivos de áudio](enumerating-audio-devices.md). Para obter a interface **IDeviceTopology** para o dispositivo de ponto de extremidade, o cliente chama o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) com o parâmetro *IID* definido como REFIID IID \_ IDeviceTopology.

No exemplo no diagrama anterior, o dispositivo Multiplexador de entrada contém todos os controles de hardware (volume, mudo e multiplexador) para os fluxos de captura da entrada de linha e dos conectores de microfone. O exemplo de código a seguir mostra como obter a interface **IDeviceTopology** para o dispositivo Multiplexador de entrada da interface **IMMDevice** para o dispositivo de ponto de extremidade para a entrada de linha ou microfone:


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface of an endpoint device. The function
// outputs a pointer (counted reference) to the
// IDeviceTopology interface of the adapter device that
// connects to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);

HRESULT GetHardwareDeviceTopology(
            IMMDevice *pEndptDev,
            IDeviceTopology **ppDevTopo)
{
    HRESULT hr = S_OK;
    IDeviceTopology *pDevTopoEndpt = NULL;
    IConnector *pConnEndpt = NULL;
    IConnector *pConnHWDev = NULL;
    IPart *pPartConn = NULL;

    // Get the endpoint device's IDeviceTopology interface.

    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL,
                      NULL, (void**)&pDevTopoEndpt);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).

    hr = pDevTopoEndpt->GetConnector(0, &pConnEndpt);
    EXIT_ON_ERROR(hr)

    // Use the connector in the endpoint device to get the
    // connector in the adapter device.

    hr = pConnEndpt->GetConnectedTo(&pConnHWDev);
    EXIT_ON_ERROR(hr)

    // Query the connector in the adapter device for
    // its IPart interface.

    hr = pConnHWDev->QueryInterface(
                         IID_IPart, (void**)&pPartConn);
    EXIT_ON_ERROR(hr)

    // Use the connector's IPart interface to get the
    // IDeviceTopology interface for the adapter device.

    hr = pPartConn->GetTopologyObject(ppDevTopo);

Exit:
    SAFE_RELEASE(pDevTopoEndpt)
    SAFE_RELEASE(pConnEndpt)
    SAFE_RELEASE(pConnHWDev)
    SAFE_RELEASE(pPartConn)

    return hr;
}
```



A função GetHardwareDeviceTopology no exemplo de código anterior executa as seguintes etapas para obter a interface **IDeviceTopology** para o dispositivo Multiplexador de entrada:

1.  Chame o método **IMMDevice:: Activate** para obter a interface **IDeviceTopology** para o dispositivo de ponto de extremidade.
2.  Com a interface **IDeviceTopology** obtida na etapa anterior, chame o método [**IDeviceTopology:: getconnecter**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) para obter a interface **IConnector** do conector único (número de conector 0) no dispositivo de ponto de extremidade.
3.  Com a interface **IConnector** obtida na etapa anterior, chame o método [**IConnector:: getconnectto**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) para obter a interface **IConnector** do conector no dispositivo Multiplexador de entrada.
4.  Consulte a interface **IConnector** obtida na etapa anterior para sua interface **IPart** .
5.  Com a interface **IPart** obtida na etapa anterior, chame o método [**IPart:: gettopologiaobject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) para obter a interface **IDeviceTopology** para o dispositivo Multiplexador de entrada.

Antes que o usuário possa gravar a partir do microfone no diagrama anterior, o aplicativo cliente deve certificar-se de que o multiplexador selecione a entrada do microfone. O exemplo de código a seguir mostra como um cliente pode atravessar o caminho de dados do microfone até encontrar o multiplexador, que, em seguida, programa para selecionar a entrada do microfone:


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface for a capture endpoint device. The
// function traverses the data path that extends from the
// endpoint device to the system bus (for example, PCI)
// or external bus (USB). If the function discovers a MUX
// (input selector) in the path, it selects the MUX input
// that connects to the stream from the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);
const IID IID_IConnector = __uuidof(IConnector);
const IID IID_IAudioInputSelector = __uuidof(IAudioInputSelector);

HRESULT SelectCaptureDevice(IMMDevice *pEndptDev)
{
    HRESULT hr = S_OK;
    DataFlow flow;
    IDeviceTopology *pDeviceTopology = NULL;
    IConnector *pConnFrom = NULL;
    IConnector *pConnTo = NULL;
    IPart *pPartPrev = NULL;
    IPart *pPartNext = NULL;
    IAudioInputSelector *pSelector = NULL;

    if (pEndptDev == NULL)
    {
        EXIT_ON_ERROR(hr = E_POINTER)
    }

    // Get the endpoint device's IDeviceTopology interface.
    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL, NULL,
                      (void**)&pDeviceTopology);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).
    hr = pDeviceTopology->GetConnector(0, &pConnFrom);
    SAFE_RELEASE(pDeviceTopology)
    EXIT_ON_ERROR(hr)

    // Make sure that this is a capture device.
    hr = pConnFrom->GetDataFlow(&flow);
    EXIT_ON_ERROR(hr)

    if (flow != Out)
    {
        // Error -- this is a rendering device.
        EXIT_ON_ERROR(hr = AUDCLNT_E_WRONG_ENDPOINT_TYPE)
    }

    // Outer loop: Each iteration traverses the data path
    // through a device topology starting at the input
    // connector and ending at the output connector.
    while (TRUE)
    {
        BOOL bConnected;
        hr = pConnFrom->IsConnected(&bConnected);
        EXIT_ON_ERROR(hr)

        // Does this connector connect to another device?
        if (bConnected == FALSE)
        {
            // This is the end of the data path that
            // stretches from the endpoint device to the
            // system bus or external bus. Verify that
            // the connection type is Software_IO.
            ConnectorType  connType;
            hr = pConnFrom->GetType(&connType);
            EXIT_ON_ERROR(hr)

            if (connType == Software_IO)
            {
                break;  // finished
            }
            EXIT_ON_ERROR(hr = E_FAIL)
        }

        // Get the connector in the next device topology,
        // which lies on the other side of the connection.
        hr = pConnFrom->GetConnectedTo(&pConnTo);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnFrom)

        // Get the connector's IPart interface.
        hr = pConnTo->QueryInterface(
                        IID_IPart, (void**)&pPartPrev);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnTo)

        // Inner loop: Each iteration traverses one link in a
        // device topology and looks for input multiplexers.
        while (TRUE)
        {
            PartType parttype;
            UINT localId;
            IPartsList *pParts;

            // Follow downstream link to next part.
            hr = pPartPrev->EnumPartsOutgoing(&pParts);
            EXIT_ON_ERROR(hr)

            hr = pParts->GetPart(0, &pPartNext);
            pParts->Release();
            EXIT_ON_ERROR(hr)

            hr = pPartNext->GetPartType(&parttype);
            EXIT_ON_ERROR(hr)

            if (parttype == Connector)
            {
                // We've reached the output connector that
                // lies at the end of this device topology.
                hr = pPartNext->QueryInterface(
                                  IID_IConnector,
                                  (void**)&pConnFrom);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pPartPrev)
                SAFE_RELEASE(pPartNext)
                break;
            }

            // Failure of the following call means only that
            // the part is not a MUX (input selector).
            hr = pPartNext->Activate(
                              CLSCTX_ALL,
                              IID_IAudioInputSelector,
                              (void**)&pSelector);
            if (hr == S_OK)
            {
                // We found a MUX (input selector), so select
                // the input from our endpoint device.
                hr = pPartPrev->GetLocalId(&localId);
                EXIT_ON_ERROR(hr)

                hr = pSelector->SetSelection(localId, NULL);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pSelector)
            }

            SAFE_RELEASE(pPartPrev)
            pPartPrev = pPartNext;
            pPartNext = NULL;
        }
    }

Exit:
    SAFE_RELEASE(pConnFrom)
    SAFE_RELEASE(pConnTo)
    SAFE_RELEASE(pPartPrev)
    SAFE_RELEASE(pPartNext)
    SAFE_RELEASE(pSelector)
    return hr;
}
```



A API DeviceTopology implementa uma interface [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) para encapsular um multiplexador, como aquele no diagrama anterior. (Uma interface [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) encapsula um demultiplexador.) No exemplo de código anterior, o loop interno da função SelectCaptureDevice consulta cada subunidade que encontra para descobrir se a subunidade é um multiplexador. Se a subunidade for um multiplexador, a função chamará o método [**IAudioInputSelector:: setseleções**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) para selecionar a entrada que se conecta ao fluxo do dispositivo de ponto de extremidade.

No exemplo de código anterior, cada iteração do loop externo atravessa uma topologia de dispositivo. Ao percorrer as topologias de dispositivo no diagrama anterior, a primeira iteração atravessa o dispositivo Multiplexador de entrada e a segunda iteração atravessa o dispositivo de captura de onda. A função será encerrada quando atingir o conector na borda direita do diagrama. A terminação ocorre quando a função detecta um conector com um \_ tipo de conexão de e/s de software. Esse tipo de conexão identifica o ponto em que o dispositivo adaptador se conecta ao barramento do sistema.

A chamada para o método [**IPart:: Getparttype**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) no exemplo de código anterior Obtém um valor de enumeração **IPartType** que indica se a parte atual é um conector ou uma subunidade de processamento de áudio.

O loop interno no exemplo de código anterior percorre o link de uma parte para a próxima chamando o método [**IPart:: EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) . (Há também um método [**IPart:: EnumPartsIncoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) para a depuração na direção oposta.) Esse método recupera um objeto [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) que contém uma lista de todas as partes de saída. No entanto, qualquer parte que a função SelectCaptureDevice espera encontrar em um dispositivo de captura sempre terá exatamente uma parte de saída. Assim, a chamada subsequente para [**IPartsList:: GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) sempre solicita a primeira parte da lista, Part Number 0, porque a função pressupõe que essa é a única parte da lista.

Se a função SelectCaptureDevice encontrar uma topologia para a qual essa pressuposição não é válida, a função poderá falhar ao configurar o dispositivo corretamente. Para evitar essa falha, uma versão de finalidade mais geral da função pode fazer o seguinte:

-   Chame o método [**IPartsList:: GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) para determinar o número de partes de saída.
-   Para cada parte de saída, chame **IPartsList:: GetPart** para começar a atravessar o caminho de dados que leva da parte.

Alguns, mas não necessariamente todos, as partes têm controles de hardware associados que os clientes podem definir ou obter. Uma determinada parte pode ter zero, um ou mais controles de hardware. Um controle de hardware é representado pelo seguinte par de interfaces:

-   Uma interface de controle genérica, [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), que tem métodos comuns a todos os controles de hardware.
-   Uma interface específica de função (por exemplo, [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)) que expõe os parâmetros de controle para um tipo específico de controle de hardware (por exemplo, um controle de volume).

Para enumerar os controles de hardware para uma parte, o cliente primeiro chama o método [**IPart:: GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) para determinar o número de controles de hardware associados à parte. Em seguida, o cliente faz uma série de chamadas para o método [**IPart:: GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) para obter a interface **IControlInterface** para cada controle de hardware. Por fim, o cliente obtém a interface específica da função para cada controle de hardware chamando o método [**IControlInterface:: GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) para obter a ID da interface. O cliente chama o método [**IPart:: Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) com essa ID para obter a interface específica da função.

Uma parte que é um conector pode dar suporte a uma das seguintes interfaces de controle específicas de função:

-   [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)
-   [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)

Uma parte que é uma subunidade pode oferecer suporte a uma ou mais das seguintes interfaces de controle específicas de função:

-   [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)
-   [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)
-   [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)
-   [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)
-   [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)
-   [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)
-   [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)
-   [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)
-   [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)
-   [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)
-   [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)
-   [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)

Uma parte dá suporte à interface **IDeviceSpecificProperty** somente se o controle de hardware subjacente tiver um valor de controle específico do dispositivo e o controle não puder ser adequadamente representado por qualquer outra interface específica da função na lista anterior. Normalmente, uma propriedade específica do dispositivo é útil somente para um cliente que pode inferir o significado do valor da propriedade de informações como o tipo de parte, subtipo de parte e nome da parte. O cliente pode obter essas informações chamando os métodos [**IPart:: Getparttype**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**IPart:: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype)e [**IPart:: GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação](programming-guide.md)
</dt> </dl>

 

 
