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
# <a name="device-topologies"></a><span data-ttu-id="25466-103">Topologias de dispositivo</span><span class="sxs-lookup"><span data-stu-id="25466-103">Device Topologies</span></span>

<span data-ttu-id="25466-104">A [API DeviceTopology](devicetopology-api.md) fornece aos clientes controle sobre uma variedade de funções internas de adaptadores de áudio que eles não podem acessar por meio da [API do MMDevice](mmdevice-api.md), do [WASAPI](wasapi.md)ou da [API do EndpointVolume](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="25466-104">The [DeviceTopology API](devicetopology-api.md) gives clients control over a variety of internal functions of audio adapters that they cannot access through the [MMDevice API](mmdevice-api.md), [WASAPI](wasapi.md), or the [EndpointVolume API](endpointvolume-api.md).</span></span>

<span data-ttu-id="25466-105">Conforme explicado anteriormente, a [API MMDevice](mmdevice-api.md), a [WASAPI](wasapi.md)e a [API EndpointVolume](endpointvolume-api.md) apresentam microfones, alto-falantes, fones de ouvido e outros dispositivos de entrada e saída de áudio para clientes como [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="25466-105">As explained previously, the [MMDevice API](mmdevice-api.md), [WASAPI](wasapi.md), and the [EndpointVolume API](endpointvolume-api.md) present microphones, speakers, headphones, and other audio input and output devices to clients as [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="25466-106">O modelo de dispositivo de ponto de extremidade fornece aos clientes acesso conveniente aos controles de volume e mudo em dispositivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="25466-106">The endpoint device model provides clients with convenient access to volume and mute controls in audio devices.</span></span> <span data-ttu-id="25466-107">Os clientes que exigem apenas esses controles simples podem evitar percorrer as topologias internas de dispositivos de hardware em adaptadores de áudio.</span><span class="sxs-lookup"><span data-stu-id="25466-107">Clients that require only these simple controls can avoid traversing the internal topologies of hardware devices in audio adapters.</span></span>

<span data-ttu-id="25466-108">No Windows Vista, o mecanismo de áudio configura automaticamente as topologias de dispositivos de áudio para uso por aplicativos de áudio.</span><span class="sxs-lookup"><span data-stu-id="25466-108">In Windows Vista, the audio engine automatically configures the topologies of audio devices for use by audio applications.</span></span> <span data-ttu-id="25466-109">Assim, os aplicativos raramente, se nunca, precisam usar a API DeviceTopology para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="25466-109">Thus, applications rarely, if ever, need to use the DeviceTopology API for this purpose.</span></span> <span data-ttu-id="25466-110">Por exemplo, suponha que um adaptador de áudio contenha um multiplexador de entrada que possa capturar um fluxo de uma entrada de linha ou de um microfone, mas que não possa capturar fluxos de ambos os dispositivos de ponto de extremidade ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="25466-110">For example, assume that an audio adapter contains an input multiplexer that can capture a stream from either a line input or a microphone, but that cannot capture streams from both endpoint devices at the same time.</span></span> <span data-ttu-id="25466-111">Suponha que o usuário habilitou aplicativos de modo exclusivo para apropriar o uso de um dispositivo de ponto de extremidade de áudio por aplicativos de modo compartilhado, conforme descrito em [fluxos de modo exclusivo](exclusive-mode-streams.md).</span><span class="sxs-lookup"><span data-stu-id="25466-111">Assume that the user has enabled exclusive-mode applications to preempt the use of an audio endpoint device by shared-mode applications, as described in [Exclusive-Mode Streams](exclusive-mode-streams.md).</span></span> <span data-ttu-id="25466-112">Se um aplicativo de modo compartilhado estiver gravando um fluxo da entrada de linha no momento em que um aplicativo de modo exclusivo começar a gravar um fluxo do microfone, o mecanismo de áudio alternará automaticamente o multiplexador da entrada de linha para o microfone.</span><span class="sxs-lookup"><span data-stu-id="25466-112">If a shared-mode application is recording a stream from the line input at the time that an exclusive-mode application begins recording a stream from the microphone, the audio engine automatically switches the multiplexer from the line input to the microphone.</span></span> <span data-ttu-id="25466-113">Por outro lado, em versões anteriores do Windows, incluindo o Windows XP, o aplicativo de modo exclusivo neste exemplo usaria as funções **mixerXxx** na API de multimídia do Windows para atravessar as topologias dos dispositivos de adaptador, descobrir o multiplexador e configurar o multiplexador para selecionar a entrada do microfone.</span><span class="sxs-lookup"><span data-stu-id="25466-113">In contrast, in earlier versions of Windows, including Windows XP, the exclusive-mode application in this example would use the **mixerXxx** functions in the Windows multimedia API to traverse the topologies of the adapter devices, discover the multiplexer, and configure the multiplexer to select the microphone input.</span></span> <span data-ttu-id="25466-114">No Windows Vista, essas etapas não são mais necessárias.</span><span class="sxs-lookup"><span data-stu-id="25466-114">In Windows Vista, these steps are no longer required.</span></span>

<span data-ttu-id="25466-115">No entanto, alguns clientes podem exigir controle explícito sobre os tipos de controles de hardware de áudio que não podem ser acessados por meio da API do MMDevice, do WASAPI ou da API do EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="25466-115">However, some clients might require explicit control over types of audio hardware controls that cannot be accessed through the MMDevice API, WASAPI, or the EndpointVolume API.</span></span> <span data-ttu-id="25466-116">Para esses clientes, a API DeviceTopology fornece a capacidade de atravessar as topologias de dispositivos de adaptador para descobrir e gerenciar os controles de áudio nos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="25466-116">For these clients, the DeviceTopology API provides the ability to traverse the topologies of adapter devices to discover and manage the audio controls in the devices.</span></span> <span data-ttu-id="25466-117">Os aplicativos que usam a API DeviceTopology devem ser criados com cuidado para evitar interferir na política de áudio do Windows e perturbar as configurações internas de dispositivos de áudio que são compartilhados com outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="25466-117">Applications that use the DeviceTopology API must be designed with care to avoid interfering with Windows audio policy and disturbing the internal configurations of audio devices that are shared with other applications.</span></span> <span data-ttu-id="25466-118">Para obter mais informações sobre a política de áudio do Windows, consulte [componentes de áudio do modo de usuário](user-mode-audio-components.md).</span><span class="sxs-lookup"><span data-stu-id="25466-118">For more information about Windows audio policy, see [User-Mode Audio Components](user-mode-audio-components.md).</span></span>

<span data-ttu-id="25466-119">A API DeviceTopology fornece interfaces para descobrir e gerenciar os seguintes tipos de controles de áudio em uma topologia de dispositivo:</span><span class="sxs-lookup"><span data-stu-id="25466-119">The DeviceTopology API provides interfaces for discovering and managing the following types of audio controls in a device topology:</span></span>

-   <span data-ttu-id="25466-120">Controle de lucro automático</span><span class="sxs-lookup"><span data-stu-id="25466-120">Automatic gain control</span></span>
-   <span data-ttu-id="25466-121">Controle de baixo</span><span class="sxs-lookup"><span data-stu-id="25466-121">Bass control</span></span>
-   <span data-ttu-id="25466-122">Seletor de entrada (multiplexador)</span><span class="sxs-lookup"><span data-stu-id="25466-122">Input selector (multiplexer)</span></span>
-   <span data-ttu-id="25466-123">Controle de intensidade</span><span class="sxs-lookup"><span data-stu-id="25466-123">Loudness control</span></span>
-   <span data-ttu-id="25466-124">Controle de midrange</span><span class="sxs-lookup"><span data-stu-id="25466-124">Midrange control</span></span>
-   <span data-ttu-id="25466-125">Controle sem áudio</span><span class="sxs-lookup"><span data-stu-id="25466-125">Mute control</span></span>
-   <span data-ttu-id="25466-126">Seletor de saída (demultiplexador)</span><span class="sxs-lookup"><span data-stu-id="25466-126">Output selector (demultiplexer)</span></span>
-   <span data-ttu-id="25466-127">Medidor de pico</span><span class="sxs-lookup"><span data-stu-id="25466-127">Peak meter</span></span>
-   <span data-ttu-id="25466-128">Controle de agudos</span><span class="sxs-lookup"><span data-stu-id="25466-128">Treble control</span></span>
-   <span data-ttu-id="25466-129">Controle de volume</span><span class="sxs-lookup"><span data-stu-id="25466-129">Volume control</span></span>

<span data-ttu-id="25466-130">Além disso, a API do DeviceTopology permite que os clientes consultem os dispositivos do adaptador para obter informações sobre os formatos de fluxo para os quais dão suporte.</span><span class="sxs-lookup"><span data-stu-id="25466-130">In addition, the DeviceTopology API enables clients to query adapter devices for information about the stream formats that they support.</span></span> <span data-ttu-id="25466-131">O arquivo de cabeçalho Devicetopology. h define as interfaces na API DeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="25466-131">The header file Devicetopology.h defines the interfaces in the DeviceTopology API.</span></span>

<span data-ttu-id="25466-132">O diagrama a seguir mostra um exemplo de várias topologias de dispositivo conectadas para a parte de um adaptador PCI que captura áudio de um microfone, entrada de linha e CD player.</span><span class="sxs-lookup"><span data-stu-id="25466-132">The following diagram shows an example of several connected device topologies for the portion of a PCI adapter that captures audio from a microphone, line input, and CD player.</span></span>

![exemplo de quatro topologias de dispositivo conectadas](images/fig2.jpg)

<span data-ttu-id="25466-134">O diagrama anterior mostra os caminhos de dados que levam das entradas analógicas para o barramento do sistema.</span><span class="sxs-lookup"><span data-stu-id="25466-134">The preceding diagram shows the data paths that lead from the analog inputs to the system bus.</span></span> <span data-ttu-id="25466-135">Cada um dos seguintes dispositivos é representado como um objeto de topologia de dispositivo com uma interface [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) :</span><span class="sxs-lookup"><span data-stu-id="25466-135">Each of the following devices is represented as a device-topology object with an [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) interface:</span></span>

-   <span data-ttu-id="25466-136">Dispositivo de captura de som wave</span><span class="sxs-lookup"><span data-stu-id="25466-136">Wave capture device</span></span>
-   <span data-ttu-id="25466-137">Dispositivo Multiplexador de entrada</span><span class="sxs-lookup"><span data-stu-id="25466-137">Input multiplexer device</span></span>
-   <span data-ttu-id="25466-138">Dispositivo de ponto de extremidade A</span><span class="sxs-lookup"><span data-stu-id="25466-138">Endpoint device A</span></span>
-   <span data-ttu-id="25466-139">Ponto de extremidade dispositivo B</span><span class="sxs-lookup"><span data-stu-id="25466-139">Endpoint device B</span></span>

<span data-ttu-id="25466-140">Observe que o diagrama de topologia combina dispositivos de adaptador (os dispositivos de captura de onda e multiplexador de entrada) com dispositivos de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="25466-140">Note that the topology diagram combines adapter devices (the wave capture and input multiplexer devices) with endpoint devices.</span></span> <span data-ttu-id="25466-141">Através das conexões entre dispositivos, os dados de áudio passam de um dispositivo para o outro.</span><span class="sxs-lookup"><span data-stu-id="25466-141">Through the connections between devices, audio data passes from one device to the next.</span></span> <span data-ttu-id="25466-142">Em cada lado de uma conexão, há um conector (rotulado como con no diagrama) por meio do qual os dados entram ou saem de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25466-142">On each side of a connection is a connector (labeled Con in the diagram) through which data enters or leaves a device.</span></span>

<span data-ttu-id="25466-143">Na borda esquerda do diagrama, os sinais da entrada de linha e dos conectores de microfone inserem os dispositivos de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="25466-143">On the left edge of the diagram, signals from the line-input and microphone jacks enter the endpoint devices.</span></span>

<span data-ttu-id="25466-144">Dentro do dispositivo de captura de som wave e do dispositivo Multiplexador de entrada estão as funções de processamento de fluxo, que, na terminologia da API DeviceTopology, são chamadas de subunidades.</span><span class="sxs-lookup"><span data-stu-id="25466-144">Inside the wave capture device and input multiplexer device are stream-processing functions, which, in the terminology of the DeviceTopology API, are called subunits.</span></span> <span data-ttu-id="25466-145">Os seguintes tipos de subunidades aparecem no diagrama anterior:</span><span class="sxs-lookup"><span data-stu-id="25466-145">The following types of subunits appear in the preceding diagram:</span></span>

-   <span data-ttu-id="25466-146">Controle de volume (rotulado como vol)</span><span class="sxs-lookup"><span data-stu-id="25466-146">Volume control (labeled Vol)</span></span>
-   <span data-ttu-id="25466-147">Controle sem áudio (rotulado sem som)</span><span class="sxs-lookup"><span data-stu-id="25466-147">Mute control (labeled Mute)</span></span>
-   <span data-ttu-id="25466-148">Multiplexador (ou seletor de entrada; rotulado como MUX)</span><span class="sxs-lookup"><span data-stu-id="25466-148">Multiplexer (or input selector; labeled MUX)</span></span>
-   <span data-ttu-id="25466-149">Conversor de analógico para digital (rotulado como ADC)</span><span class="sxs-lookup"><span data-stu-id="25466-149">Analog-to-digital converter (labeled ADC)</span></span>

<span data-ttu-id="25466-150">As configurações nas subunidades de volume, mudo e multiplexador podem ser controladas por clientes e a API DeviceTopology fornece interfaces de controle aos clientes para controlá-las.</span><span class="sxs-lookup"><span data-stu-id="25466-150">The settings in the volume, mute, and multiplexer subunits can be controlled by clients, and the DeviceTopology API provides control interfaces to clients for controlling them.</span></span> <span data-ttu-id="25466-151">Neste exemplo, a subunidade ADC não tem configurações de controle.</span><span class="sxs-lookup"><span data-stu-id="25466-151">In this example, the ADC subunit has no control settings.</span></span> <span data-ttu-id="25466-152">Assim, a API DeviceTopology não fornece nenhuma interface de controle para o ADC.</span><span class="sxs-lookup"><span data-stu-id="25466-152">Thus, the DeviceTopology API provides no control interface for the ADC.</span></span>

<span data-ttu-id="25466-153">Na terminologia da API do DeviceTopology, os conectores e as subunidades pertencem à mesma categoria geral – partes.</span><span class="sxs-lookup"><span data-stu-id="25466-153">In the terminology of the DeviceTopology API, connectors and subunits belong to the same general category—parts.</span></span> <span data-ttu-id="25466-154">Todas as partes, independentemente de serem conectores ou subunidades, fornecem um conjunto comum de funções.</span><span class="sxs-lookup"><span data-stu-id="25466-154">All parts, regardless of whether they are connectors or subunits, provide a common set of functions.</span></span> <span data-ttu-id="25466-155">A API DeviceTopology implementa uma interface [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) para representar as funções genéricas que são comuns a conectores e subunidades.</span><span class="sxs-lookup"><span data-stu-id="25466-155">The DeviceTopology API implements an [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) interface to represent the generic functions that are common to connectors and subunits.</span></span> <span data-ttu-id="25466-156">A API implementa as interfaces [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) e [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) para representar os aspectos específicos de conectores e subunidades.</span><span class="sxs-lookup"><span data-stu-id="25466-156">The API implements the [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) and [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) interfaces to represent the specific aspects of connectors and subunits.</span></span>

<span data-ttu-id="25466-157">A API DeviceTopology constrói as topologias do dispositivo de captura de onda e do dispositivo Multiplexador de entrada dos filtros de streaming de kernel (KS) que o driver de áudio expõe ao sistema operacional para representar esses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="25466-157">The DeviceTopology API constructs the topologies of the wave capture device and input multiplexer device from the kernel-streaming (KS) filters that the audio driver exposes to the operating system to represent these devices.</span></span> <span data-ttu-id="25466-158">(O driver do adaptador de áudio implementa as interfaces **IMiniportWaveXxx** e **IMiniportTopology** para representar as partes dependentes de hardware desses filtros; para obter mais informações sobre essas interfaces e sobre filtros KS, consulte a documentação do Windows DDK.)</span><span class="sxs-lookup"><span data-stu-id="25466-158">(The audio adapter driver implements **IMiniportWaveXxx** and **IMiniportTopology** interfaces to represent the hardware-dependent portions of these filters; for more information about these interfaces and about KS filters, see the Windows DDK documentation.)</span></span>

<span data-ttu-id="25466-159">A API DeviceTopology constrói topologias triviais para representar os dispositivos de ponto de extremidade A e B no diagrama anterior.</span><span class="sxs-lookup"><span data-stu-id="25466-159">The DeviceTopology API constructs trivial topologies to represent endpoint devices A and B in the preceding diagram.</span></span> <span data-ttu-id="25466-160">A topologia do dispositivo de um dispositivo de ponto de extremidade consiste em um único conector.</span><span class="sxs-lookup"><span data-stu-id="25466-160">The device topology of an endpoint device consists of a single connector.</span></span> <span data-ttu-id="25466-161">Essa topologia é meramente um espaço reservado para o dispositivo de ponto de extremidade e não contém nenhuma subunidade para o processamento de dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="25466-161">This topology is merely a placeholder for the endpoint device and contains no subunits for processing audio data.</span></span> <span data-ttu-id="25466-162">Na verdade, os dispositivos de adaptador contêm todas as subunidades que os aplicativos cliente usam para controlar o processamento de áudio.</span><span class="sxs-lookup"><span data-stu-id="25466-162">In fact, adapter devices contain all of the subunits that client applications use to control audio processing.</span></span> <span data-ttu-id="25466-163">A topologia do dispositivo de um dispositivo de ponto de extremidade serve principalmente como um ponto de partida para explorar as topologias de dispositivo dos dispositivos de adaptador.</span><span class="sxs-lookup"><span data-stu-id="25466-163">The device topology of an endpoint device serves primarily as a starting point for exploring the device topologies of adapter devices.</span></span>

<span data-ttu-id="25466-164">Conexões internas entre duas partes em uma topologia de dispositivo são chamadas de links.</span><span class="sxs-lookup"><span data-stu-id="25466-164">Internal connections between two parts in a device topology are called links.</span></span> <span data-ttu-id="25466-165">A API DeviceTopology fornece métodos para atravessar links de uma parte para a próxima em uma topologia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25466-165">The DeviceTopology API provides methods for traversing links from one part to the next in a device topology.</span></span> <span data-ttu-id="25466-166">A API também fornece métodos para percorrer as conexões entre as topologias de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25466-166">The API also provides methods for traversing the connections between device topologies.</span></span>

<span data-ttu-id="25466-167">Para iniciar a exploração de um conjunto de topologias de dispositivo conectadas, um aplicativo cliente ativa a interface **IDeviceTopology** de um dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="25466-167">To begin exploration of a set of connected device topologies, a client application activates the **IDeviceTopology** interface of an audio endpoint device.</span></span> <span data-ttu-id="25466-168">O conector em um dispositivo de ponto de extremidade se conecta a um conector em um adaptador de áudio ou a uma rede.</span><span class="sxs-lookup"><span data-stu-id="25466-168">The connector in an endpoint device connects either to a connector in an audio adapter or to a network.</span></span> <span data-ttu-id="25466-169">Se o ponto de extremidade se conectar a um dispositivo em um adaptador de áudio, os métodos na API DeviceTopology permitirão que o aplicativo passe pela conexão do ponto de extremidade para o adaptador, obtendo uma referência à interface **IDeviceTopology** do dispositivo adaptador no outro lado da conexão.</span><span class="sxs-lookup"><span data-stu-id="25466-169">If the endpoint connects to a device on an audio adapter, then the methods in the DeviceTopology API enable the application to step across the connection from the endpoint to the adapter by obtaining a reference to the **IDeviceTopology** interface of the adapter device on the other side of the connection.</span></span> <span data-ttu-id="25466-170">Uma rede, por outro lado, não tem nenhuma topologia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25466-170">A network, on the other hand, has no device topology.</span></span> <span data-ttu-id="25466-171">Uma conexão de rede canaliza um fluxo de áudio para um cliente que está acessando o sistema remotamente.</span><span class="sxs-lookup"><span data-stu-id="25466-171">A network connection pipes an audio stream to a client that is accessing the system remotely.</span></span>

<span data-ttu-id="25466-172">A API DeviceTopology fornece acesso apenas às topologias dos dispositivos de hardware em um adaptador de áudio.</span><span class="sxs-lookup"><span data-stu-id="25466-172">The DeviceTopology API provides access only to the topologies of the hardware devices in an audio adapter.</span></span> <span data-ttu-id="25466-173">Os dispositivos externos na borda esquerda do diagrama e os componentes de software na borda direita estão além do escopo da API.</span><span class="sxs-lookup"><span data-stu-id="25466-173">The external devices on the left edge of the diagram and the software components on the right edge are beyond the scope of the API.</span></span> <span data-ttu-id="25466-174">As linhas tracejadas em cada lado do diagrama representam os limites da API DeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="25466-174">The dashed lines on either side of the diagram represent the limits of the DeviceTopology API.</span></span> <span data-ttu-id="25466-175">O cliente pode usar a API para explorar um caminho de dados que se estende do conector de entrada para o barramento do sistema, mas a API não pode penetrar além desses limites.</span><span class="sxs-lookup"><span data-stu-id="25466-175">The client can use the API to explore a data path that stretches from the input jack to the system bus, but the API cannot penetrate beyond these boundaries.</span></span>

<span data-ttu-id="25466-176">Cada conector no diagrama anterior tem um tipo de conexão associado que indica o tipo de conexão que o conector faz.</span><span class="sxs-lookup"><span data-stu-id="25466-176">Each connector in the preceding diagram has an associated connection type that indicates the type of connection that the connector makes.</span></span> <span data-ttu-id="25466-177">Assim, os conectores nos dois lados de uma conexão sempre têm tipos de conexão idênticos.</span><span class="sxs-lookup"><span data-stu-id="25466-177">Thus, the connectors on the two sides of a connection always have identical connection types.</span></span> <span data-ttu-id="25466-178">O tipo de conexão é indicado por um valor de enumeração [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) — físico \_ externo, físico \_ interno, software \_ fixo, \_ e/s de software ou rede.</span><span class="sxs-lookup"><span data-stu-id="25466-178">The connection type is indicated by a [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) enumeration value—Physical\_External, Physical\_Internal, Software\_Fixed, Software\_IO, or Network.</span></span> <span data-ttu-id="25466-179">As conexões entre o dispositivo Multiplexador de entrada e os dispositivos de ponto de extremidade A e B são do tipo físico \_ externo, o que significa que a conexão representa uma conexão física com um dispositivo externo (em outras palavras, uma tomada de áudio acessível pelo usuário).</span><span class="sxs-lookup"><span data-stu-id="25466-179">The connections between the input multiplexer device and endpoint devices A and B are of type Physical\_External, which means that the connection represents a physical connection to an external device (in other words, a user-accessible audio jack).</span></span> <span data-ttu-id="25466-180">A conexão com o sinal analógico do CD player interno é do tipo físico \_ interno, que indica uma conexão física com um dispositivo auxiliar que é instalado dentro do chassi do sistema.</span><span class="sxs-lookup"><span data-stu-id="25466-180">The connection to the analog signal from the internal CD player is of type Physical\_Internal, which indicates a physical connection to an auxiliary device that is installed inside the system chassis.</span></span> <span data-ttu-id="25466-181">A conexão entre o dispositivo de captura de onda e o dispositivo Multiplexador de entrada é do tipo software \_ fixo, que indica uma conexão permanente que é fixa e não pode ser configurada no controle de software.</span><span class="sxs-lookup"><span data-stu-id="25466-181">The connection between the wave capture device and input multiplexer device is of type Software\_Fixed, which indicates a permanent connection that is fixed and cannot be configured under software control.</span></span> <span data-ttu-id="25466-182">Por fim, a conexão com o barramento do sistema no lado direito do diagrama é do tipo software \_ Io, que indica que a e/s de dados para a conexão é implementada por um mecanismo de DMA sob controle de software.</span><span class="sxs-lookup"><span data-stu-id="25466-182">Finally, the connection to the system bus on the right side of the diagram is of type Software\_IO, which indicates that the data I/O for the connection is implemented by a DMA engine under software control.</span></span> <span data-ttu-id="25466-183">(O diagrama não inclui um exemplo de tipo de conexão de rede.)</span><span class="sxs-lookup"><span data-stu-id="25466-183">(The diagram does not include an example of a Network connection type.)</span></span>

<span data-ttu-id="25466-184">O cliente começa a atravessar um caminho de dados no dispositivo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="25466-184">The client begins traversing a data path at the endpoint device.</span></span> <span data-ttu-id="25466-185">Primeiro, o cliente obtém uma interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) que representa o dispositivo de ponto de extremidade, conforme explicado em [enumerando dispositivos de áudio](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="25466-185">First, the client obtains an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface that represents the endpoint device, as explained in [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span> <span data-ttu-id="25466-186">Para obter a interface **IDeviceTopology** para o dispositivo de ponto de extremidade, o cliente chama o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) com o parâmetro *IID* definido como REFIID IID \_ IDeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="25466-186">To obtain the **IDeviceTopology** interface for the endpoint device, the client calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method with parameter *iid* set to REFIID IID\_IDeviceTopology.</span></span>

<span data-ttu-id="25466-187">No exemplo no diagrama anterior, o dispositivo Multiplexador de entrada contém todos os controles de hardware (volume, mudo e multiplexador) para os fluxos de captura da entrada de linha e dos conectores de microfone.</span><span class="sxs-lookup"><span data-stu-id="25466-187">In the example in the preceding diagram, the input multiplexer device contains all the hardware controls (volume, mute, and multiplexer) for the capture streams from the line-input and microphone jacks.</span></span> <span data-ttu-id="25466-188">O exemplo de código a seguir mostra como obter a interface **IDeviceTopology** para o dispositivo Multiplexador de entrada da interface **IMMDevice** para o dispositivo de ponto de extremidade para a entrada de linha ou microfone:</span><span class="sxs-lookup"><span data-stu-id="25466-188">The following code example shows how to obtain the **IDeviceTopology** interface for the input multiplexer device from the **IMMDevice** interface for the endpoint device for the line input or microphone:</span></span>


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



<span data-ttu-id="25466-189">A função GetHardwareDeviceTopology no exemplo de código anterior executa as seguintes etapas para obter a interface **IDeviceTopology** para o dispositivo Multiplexador de entrada:</span><span class="sxs-lookup"><span data-stu-id="25466-189">The GetHardwareDeviceTopology function in the previous code example performs the following steps to obtain the **IDeviceTopology** interface for the input multiplexer device:</span></span>

1.  <span data-ttu-id="25466-190">Chame o método **IMMDevice:: Activate** para obter a interface **IDeviceTopology** para o dispositivo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="25466-190">Call the **IMMDevice::Activate** method to get the **IDeviceTopology** interface for the endpoint device.</span></span>
2.  <span data-ttu-id="25466-191">Com a interface **IDeviceTopology** obtida na etapa anterior, chame o método [**IDeviceTopology:: getconnecter**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) para obter a interface **IConnector** do conector único (número de conector 0) no dispositivo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="25466-191">With the **IDeviceTopology** interface obtained in the preceding step, call the [**IDeviceTopology::GetConnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) method to get the **IConnector** interface of the single connector (connector number 0) in the endpoint device.</span></span>
3.  <span data-ttu-id="25466-192">Com a interface **IConnector** obtida na etapa anterior, chame o método [**IConnector:: getconnectto**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) para obter a interface **IConnector** do conector no dispositivo Multiplexador de entrada.</span><span class="sxs-lookup"><span data-stu-id="25466-192">With the **IConnector** interface obtained in the preceding step, call the [**IConnector::GetConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) method to get the **IConnector** interface of the connector in the input multiplexer device.</span></span>
4.  <span data-ttu-id="25466-193">Consulte a interface **IConnector** obtida na etapa anterior para sua interface **IPart** .</span><span class="sxs-lookup"><span data-stu-id="25466-193">Query the **IConnector** interface obtained in the preceding step for its **IPart** interface.</span></span>
5.  <span data-ttu-id="25466-194">Com a interface **IPart** obtida na etapa anterior, chame o método [**IPart:: gettopologiaobject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) para obter a interface **IDeviceTopology** para o dispositivo Multiplexador de entrada.</span><span class="sxs-lookup"><span data-stu-id="25466-194">With the **IPart** interface obtained in the preceding step, call the [**IPart::GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) method to get the **IDeviceTopology** interface for the input multiplexer device.</span></span>

<span data-ttu-id="25466-195">Antes que o usuário possa gravar a partir do microfone no diagrama anterior, o aplicativo cliente deve certificar-se de que o multiplexador selecione a entrada do microfone.</span><span class="sxs-lookup"><span data-stu-id="25466-195">Before the user can record from the microphone in the preceding diagram, the client application must make certain that the multiplexer selects the microphone input.</span></span> <span data-ttu-id="25466-196">O exemplo de código a seguir mostra como um cliente pode atravessar o caminho de dados do microfone até encontrar o multiplexador, que, em seguida, programa para selecionar a entrada do microfone:</span><span class="sxs-lookup"><span data-stu-id="25466-196">The following code example shows how a client can traverse the data path from the microphone until it finds the multiplexer, which it then programs to select the microphone input:</span></span>


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



<span data-ttu-id="25466-197">A API DeviceTopology implementa uma interface [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) para encapsular um multiplexador, como aquele no diagrama anterior.</span><span class="sxs-lookup"><span data-stu-id="25466-197">The DeviceTopology API implements an [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) interface to encapsulate a multiplexer, such as the one in the preceding diagram.</span></span> <span data-ttu-id="25466-198">(Uma interface [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) encapsula um demultiplexador.) No exemplo de código anterior, o loop interno da função SelectCaptureDevice consulta cada subunidade que encontra para descobrir se a subunidade é um multiplexador.</span><span class="sxs-lookup"><span data-stu-id="25466-198">(An [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) interface encapsulates a demultiplexer.) In the preceding code example, the inner loop of the SelectCaptureDevice function queries each subunit that it finds to discover whether the subunit is a multiplexer.</span></span> <span data-ttu-id="25466-199">Se a subunidade for um multiplexador, a função chamará o método [**IAudioInputSelector:: setseleções**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) para selecionar a entrada que se conecta ao fluxo do dispositivo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="25466-199">If the subunit is a multiplexer, then the function calls the [**IAudioInputSelector::SetSelection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) method to select the input that connects to the stream from the endpoint device.</span></span>

<span data-ttu-id="25466-200">No exemplo de código anterior, cada iteração do loop externo atravessa uma topologia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25466-200">In the preceding code example, each iteration of the outer loop traverses one device topology.</span></span> <span data-ttu-id="25466-201">Ao percorrer as topologias de dispositivo no diagrama anterior, a primeira iteração atravessa o dispositivo Multiplexador de entrada e a segunda iteração atravessa o dispositivo de captura de onda.</span><span class="sxs-lookup"><span data-stu-id="25466-201">When traversing the device topologies in the preceding diagram, the first iteration traverses the input multiplexer device and the second iteration traverses the wave capture device.</span></span> <span data-ttu-id="25466-202">A função será encerrada quando atingir o conector na borda direita do diagrama.</span><span class="sxs-lookup"><span data-stu-id="25466-202">The function will terminate when it reaches the connector at the right edge of the diagram.</span></span> <span data-ttu-id="25466-203">A terminação ocorre quando a função detecta um conector com um \_ tipo de conexão de e/s de software.</span><span class="sxs-lookup"><span data-stu-id="25466-203">Termination occurs when the function detects a connector with a Software\_IO connection type.</span></span> <span data-ttu-id="25466-204">Esse tipo de conexão identifica o ponto em que o dispositivo adaptador se conecta ao barramento do sistema.</span><span class="sxs-lookup"><span data-stu-id="25466-204">This connection type identifies the point at which the adapter device connects to the system bus.</span></span>

<span data-ttu-id="25466-205">A chamada para o método [**IPart:: Getparttype**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) no exemplo de código anterior Obtém um valor de enumeração **IPartType** que indica se a parte atual é um conector ou uma subunidade de processamento de áudio.</span><span class="sxs-lookup"><span data-stu-id="25466-205">The call to the [**IPart::GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) method in the preceding code example obtains an **IPartType** enumeration value that indicates whether the current part is a connector or an audio-processing subunit.</span></span>

<span data-ttu-id="25466-206">O loop interno no exemplo de código anterior percorre o link de uma parte para a próxima chamando o método [**IPart:: EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) .</span><span class="sxs-lookup"><span data-stu-id="25466-206">The inner loop in the preceding code example steps across the link from one part to the next by calling the [**IPart::EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) method.</span></span> <span data-ttu-id="25466-207">(Há também um método [**IPart:: EnumPartsIncoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) para a depuração na direção oposta.) Esse método recupera um objeto [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) que contém uma lista de todas as partes de saída.</span><span class="sxs-lookup"><span data-stu-id="25466-207">(There's also an [**IPart::EnumPartsIncoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) method for stepping in the opposite direction.) This method retrieves an [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) object that contains a list of all the outgoing parts.</span></span> <span data-ttu-id="25466-208">No entanto, qualquer parte que a função SelectCaptureDevice espera encontrar em um dispositivo de captura sempre terá exatamente uma parte de saída.</span><span class="sxs-lookup"><span data-stu-id="25466-208">However, any part that the SelectCaptureDevice function expects to encounter in a capture device will always have exactly one outgoing part.</span></span> <span data-ttu-id="25466-209">Assim, a chamada subsequente para [**IPartsList:: GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) sempre solicita a primeira parte da lista, Part Number 0, porque a função pressupõe que essa é a única parte da lista.</span><span class="sxs-lookup"><span data-stu-id="25466-209">Thus, the subsequent call to [**IPartsList::GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) always requests the first part in the list, part number 0, because the function assumes that this is the only part in the list.</span></span>

<span data-ttu-id="25466-210">Se a função SelectCaptureDevice encontrar uma topologia para a qual essa pressuposição não é válida, a função poderá falhar ao configurar o dispositivo corretamente.</span><span class="sxs-lookup"><span data-stu-id="25466-210">If the SelectCaptureDevice function encounters a topology for which that assumption is not valid, the function might fail to configure the device correctly.</span></span> <span data-ttu-id="25466-211">Para evitar essa falha, uma versão de finalidade mais geral da função pode fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="25466-211">To avoid such a failure, a more general-purpose version of the function might do the following:</span></span>

-   <span data-ttu-id="25466-212">Chame o método [**IPartsList:: GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) para determinar o número de partes de saída.</span><span class="sxs-lookup"><span data-stu-id="25466-212">Call the [**IPartsList::GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) method to determine the number of outgoing parts.</span></span>
-   <span data-ttu-id="25466-213">Para cada parte de saída, chame **IPartsList:: GetPart** para começar a atravessar o caminho de dados que leva da parte.</span><span class="sxs-lookup"><span data-stu-id="25466-213">For each outgoing part, call **IPartsList::GetPart** to begin to traverse the data path that leads from the part.</span></span>

<span data-ttu-id="25466-214">Alguns, mas não necessariamente todos, as partes têm controles de hardware associados que os clientes podem definir ou obter.</span><span class="sxs-lookup"><span data-stu-id="25466-214">Some, but not necessarily all, parts have associated hardware controls that clients can set or get.</span></span> <span data-ttu-id="25466-215">Uma determinada parte pode ter zero, um ou mais controles de hardware.</span><span class="sxs-lookup"><span data-stu-id="25466-215">A particular part might have zero, one, or more hardware controls.</span></span> <span data-ttu-id="25466-216">Um controle de hardware é representado pelo seguinte par de interfaces:</span><span class="sxs-lookup"><span data-stu-id="25466-216">A hardware control is represented by the following pair of interfaces:</span></span>

-   <span data-ttu-id="25466-217">Uma interface de controle genérica, [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), que tem métodos comuns a todos os controles de hardware.</span><span class="sxs-lookup"><span data-stu-id="25466-217">A generic control interface, [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), which has methods that are common to all hardware controls.</span></span>
-   <span data-ttu-id="25466-218">Uma interface específica de função (por exemplo, [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)) que expõe os parâmetros de controle para um tipo específico de controle de hardware (por exemplo, um controle de volume).</span><span class="sxs-lookup"><span data-stu-id="25466-218">A function-specific interface (for example, [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)) that exposes the control parameters for a particular type of hardware control (for example, a volume control).</span></span>

<span data-ttu-id="25466-219">Para enumerar os controles de hardware para uma parte, o cliente primeiro chama o método [**IPart:: GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) para determinar o número de controles de hardware associados à parte.</span><span class="sxs-lookup"><span data-stu-id="25466-219">To enumerate the hardware controls for a part, the client first calls the [**IPart::GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) method to determine the number of hardware controls that are associated with the part.</span></span> <span data-ttu-id="25466-220">Em seguida, o cliente faz uma série de chamadas para o método [**IPart:: GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) para obter a interface **IControlInterface** para cada controle de hardware.</span><span class="sxs-lookup"><span data-stu-id="25466-220">Next, the client makes a series of calls to the [**IPart::GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) method to obtain the **IControlInterface** interface for each hardware control.</span></span> <span data-ttu-id="25466-221">Por fim, o cliente obtém a interface específica da função para cada controle de hardware chamando o método [**IControlInterface:: GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) para obter a ID da interface.</span><span class="sxs-lookup"><span data-stu-id="25466-221">Finally, the client obtains the function-specific interface for each hardware control by calling the [**IControlInterface::GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) method to obtain the interface ID.</span></span> <span data-ttu-id="25466-222">O cliente chama o método [**IPart:: Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) com essa ID para obter a interface específica da função.</span><span class="sxs-lookup"><span data-stu-id="25466-222">The client calls the [**IPart::Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) method with this ID to obtain the function-specific interface.</span></span>

<span data-ttu-id="25466-223">Uma parte que é um conector pode dar suporte a uma das seguintes interfaces de controle específicas de função:</span><span class="sxs-lookup"><span data-stu-id="25466-223">A part that is a connector might support one of the following function-specific control interfaces:</span></span>

-   [<span data-ttu-id="25466-224">**IKsFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="25466-224">**IKsFormatSupport**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)
-   [<span data-ttu-id="25466-225">**IKsJackDescription**</span><span class="sxs-lookup"><span data-stu-id="25466-225">**IKsJackDescription**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)

<span data-ttu-id="25466-226">Uma parte que é uma subunidade pode oferecer suporte a uma ou mais das seguintes interfaces de controle específicas de função:</span><span class="sxs-lookup"><span data-stu-id="25466-226">A part that is a subunit might support one or more of the following function-specific control interfaces:</span></span>

-   [<span data-ttu-id="25466-227">**IAudioAutoGainControl**</span><span class="sxs-lookup"><span data-stu-id="25466-227">**IAudioAutoGainControl**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)
-   [<span data-ttu-id="25466-228">**IAudioBass**</span><span class="sxs-lookup"><span data-stu-id="25466-228">**IAudioBass**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)
-   [<span data-ttu-id="25466-229">**IAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="25466-229">**IAudioChannelConfig**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)
-   [<span data-ttu-id="25466-230">**IAudioInputSelector**</span><span class="sxs-lookup"><span data-stu-id="25466-230">**IAudioInputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)
-   [<span data-ttu-id="25466-231">**IAudioLoudness**</span><span class="sxs-lookup"><span data-stu-id="25466-231">**IAudioLoudness**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)
-   [<span data-ttu-id="25466-232">**IAudioMidrange**</span><span class="sxs-lookup"><span data-stu-id="25466-232">**IAudioMidrange**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)
-   [<span data-ttu-id="25466-233">**IAudioMute**</span><span class="sxs-lookup"><span data-stu-id="25466-233">**IAudioMute**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)
-   [<span data-ttu-id="25466-234">**IAudioOutputSelector**</span><span class="sxs-lookup"><span data-stu-id="25466-234">**IAudioOutputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)
-   [<span data-ttu-id="25466-235">**IAudioPeakMeter**</span><span class="sxs-lookup"><span data-stu-id="25466-235">**IAudioPeakMeter**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)
-   [<span data-ttu-id="25466-236">**IAudioTreble**</span><span class="sxs-lookup"><span data-stu-id="25466-236">**IAudioTreble**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)
-   [<span data-ttu-id="25466-237">**IAudioVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="25466-237">**IAudioVolumeLevel**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)
-   [<span data-ttu-id="25466-238">**IDeviceSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="25466-238">**IDeviceSpecificProperty**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)

<span data-ttu-id="25466-239">Uma parte dá suporte à interface **IDeviceSpecificProperty** somente se o controle de hardware subjacente tiver um valor de controle específico do dispositivo e o controle não puder ser adequadamente representado por qualquer outra interface específica da função na lista anterior.</span><span class="sxs-lookup"><span data-stu-id="25466-239">A part supports the **IDeviceSpecificProperty** interface only if the underlying hardware control has a device-specific control value and the control cannot be adequately represented by any other function-specific interface in the preceding list.</span></span> <span data-ttu-id="25466-240">Normalmente, uma propriedade específica do dispositivo é útil somente para um cliente que pode inferir o significado do valor da propriedade de informações como o tipo de parte, subtipo de parte e nome da parte.</span><span class="sxs-lookup"><span data-stu-id="25466-240">Typically, a device-specific property is useful only to a client that can infer the meaning of the property value from information such as the part type, part subtype, and part name.</span></span> <span data-ttu-id="25466-241">O cliente pode obter essas informações chamando os métodos [**IPart:: Getparttype**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**IPart:: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype)e [**IPart:: GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) .</span><span class="sxs-lookup"><span data-stu-id="25466-241">The client can obtain this information by calling the [**IPart::GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**IPart::GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype), and [**IPart::GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25466-242">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="25466-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25466-243">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="25466-243">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
