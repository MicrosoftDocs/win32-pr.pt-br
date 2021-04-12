---
title: Visão geral da camada do modelo de serviço
description: A API do modelo de serviço WWSAPI modela a comunicação entre um cliente e um serviço como chamadas de método, em vez de como mensagens de dados.
ms.assetid: a1ed1e3c-94ae-4383-9251-83caf2e3ebf3
keywords:
- Serviços Web de visão geral da camada do modelo de serviço para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74861f0e2ed13b35e308d1314aec2a33dc28c31
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104297872"
---
# <a name="service-model-layer-overview"></a><span data-ttu-id="e6321-106">Visão geral da camada do modelo de serviço</span><span class="sxs-lookup"><span data-stu-id="e6321-106">Service Model Layer Overview</span></span>

<span data-ttu-id="e6321-107">A API do modelo de serviço WWSAPI modela a comunicação entre um cliente e um serviço como chamadas de método, em vez de como mensagens de dados.</span><span class="sxs-lookup"><span data-stu-id="e6321-107">The WWSAPI Service Model API models the communication between a client and a service as method calls, rather than as data messages.</span></span> <span data-ttu-id="e6321-108">Ao contrário da [camada de canal](channel-layer-overview.md), que dá suporte a trocas de [mensagens](message.md) mais tradicionais entre o cliente e o serviço, o modelo de serviço gerencia automaticamente a comunicação por meio de um proxy de serviço no cliente e um host de serviço no serviço.</span><span class="sxs-lookup"><span data-stu-id="e6321-108">In contrast to the [channel layer](channel-layer-overview.md), which supports more traditional [message](message.md) exchanges between client and service, the Service Model automatically manages communication by means of a service proxy on the client and a service host on the service.</span></span> <span data-ttu-id="e6321-109">Isso significa que o cliente chama as funções geradas e o servidor implementa retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="e6321-109">This means that the client calls generated functions and the server implements callbacks.</span></span>


<span data-ttu-id="e6321-110">Por exemplo, considere um serviço de calculadora que executa adição e subtração em dois números.</span><span class="sxs-lookup"><span data-stu-id="e6321-110">For example, consider a calculator service which performs addition and subtraction on two numbers.</span></span> <span data-ttu-id="e6321-111">Adição e subtração são operações naturalmente representadas como chamadas de método.</span><span class="sxs-lookup"><span data-stu-id="e6321-111">Addition and subtraction are operations naturally represented as method calls.</span></span>

![Diagrama mostrando como um serviço de calculadora se comunica com um cliente usando chamadas de método para adição e subtração.](images/servicemodelintro.png)

<span data-ttu-id="e6321-113">O modelo de serviço representa a comunicação entre o cliente e o serviço como chamadas de método declaradas e, portanto, oculta os detalhes de comunicação da camada de canal subjacente do aplicativo, facilitando a implementação do serviço.</span><span class="sxs-lookup"><span data-stu-id="e6321-113">The service model represents the communication between client and the service as declared method calls, and so conceals the communication details of the underlying channel layer from the application, making the service easier to implement.</span></span>

## <a name="specifying-a-service"></a><span data-ttu-id="e6321-114">Especificando um serviço</span><span class="sxs-lookup"><span data-stu-id="e6321-114">Specifying a Service</span></span>

<span data-ttu-id="e6321-115">Um serviço deve ser especificado em termos de seus padrões de troca de mensagens, bem como sua representação de dados de rede.</span><span class="sxs-lookup"><span data-stu-id="e6321-115">A service must be specified in terms of its message exchange patterns as well as its network data representation.</span></span> <span data-ttu-id="e6321-116">Para serviços, essa especificação geralmente é fornecida como documentos WSDL e de esquema XML.</span><span class="sxs-lookup"><span data-stu-id="e6321-116">For services, this specification is usually provided as WSDL and XML schema documents.</span></span>

<span data-ttu-id="e6321-117">O documento WSDL é um documento XML que contém a associação de canal e os padrões de troca de mensagens do serviço, enquanto o documento de esquema XML é um documento XML que define a representação de dados das mensagens individuais.</span><span class="sxs-lookup"><span data-stu-id="e6321-117">The WSDL document is an XML document which contains the channel binding and the message exchange patterns of the service, whereas the XML schema document is an XML document that defines the data representation of the individual messages.</span></span>

<span data-ttu-id="e6321-118">Para o serviço de calculadora e suas operações de adição e subtração, o documento WSDL pode ser semelhante ao exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="e6321-118">For the calculator service and its addition and subtraction operations, the WSDL document might look like the following example:</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="http://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

<span data-ttu-id="e6321-119">Da mesma forma, seu esquema XML pode ser definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e6321-119">Likewise, its XML schema can be defined as follows:</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="Add">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:element name="AddResponse">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="result" type="xs:int" 
    />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema> 
```

## <a name="converting-metadata-to-code"></a><span data-ttu-id="e6321-120">Convertendo metadados para código</span><span class="sxs-lookup"><span data-stu-id="e6321-120">Converting Metadata to Code</span></span>

<span data-ttu-id="e6321-121">O modelo de serviço fornece o [WsUtil.exe](web-service-compiler-tool.md) como uma ferramenta para processar esses documentos de metadados, convertendo um arquivo WSDL em um cabeçalho C e em arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="e6321-121">The service model provides the [WsUtil.exe](web-service-compiler-tool.md) as a tool to process these metadata documents, converting a WSDL file into a C header and source files.</span></span>

![Diagrama mostrando como WsUtil.exe converte um arquivo WSDL em um cabeçalho C e em arquivos de origem.](images/doctotool.png)

<span data-ttu-id="e6321-123">O [WsUtil.exe](web-service-compiler-tool.md) gera cabeçalho e fontes para implementação de serviço, bem como operações de serviço do lado do cliente para o cliente.</span><span class="sxs-lookup"><span data-stu-id="e6321-123">The [WsUtil.exe](web-service-compiler-tool.md) generates header and sources for service implementation as well as client-side service operations for the client .</span></span>

## <a name="calling-the-calculator-service-from-a-client"></a><span data-ttu-id="e6321-124">Chamando o serviço de calculadora de um cliente</span><span class="sxs-lookup"><span data-stu-id="e6321-124">Calling the Calculator Service From a Client</span></span>

<span data-ttu-id="e6321-125">Assim como acontece com a implementação do serviço, o cliente deve incluir o cabeçalho ou os cabeçalhos gerados.</span><span class="sxs-lookup"><span data-stu-id="e6321-125">As with the service implementation, the client must include the generated header or headers.</span></span>

``` syntax
#include "CalculatorProxyStub.h"
```

<span data-ttu-id="e6321-126">Agora, o aplicativo cliente pode criar e abrir um proxy de serviço para iniciar a comunicação com o serviço de calculadora.</span><span class="sxs-lookup"><span data-stu-id="e6321-126">Now, The client application can create and open a service proxy to begin communication with the calculator service.</span></span>

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L"http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

<span data-ttu-id="e6321-127">O aplicativo pode chamar a operação de adição no serviço de calculadora com o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="e6321-127">The application can call the Add operation on the calculator service with the following code:</span></span>

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

<span data-ttu-id="e6321-128">Consulte o exemplo de código em [HttpCalculatorClientExample](httpcalculatorclientexample.md) para obter a implementação completa do serviço de calculadora.</span><span class="sxs-lookup"><span data-stu-id="e6321-128">Please refer to the code example at [HttpCalculatorClientExample](httpcalculatorclientexample.md) for full implementation of the calculator service.</span></span>

## <a name="service-model-components"></a><span data-ttu-id="e6321-129">Componentes do modelo de serviço</span><span class="sxs-lookup"><span data-stu-id="e6321-129">Service Model Components</span></span>

<span data-ttu-id="e6321-130">A interação dos componentes individuais do modelo de serviço WWSAPI dentro do exemplo de calculadora é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="e6321-130">The interaction of the individual WWSAPI Service Model components within the Calculator example is as follows:</span></span>

-   <span data-ttu-id="e6321-131">O cliente cria um [proxy de serviço](service-proxy.md) e o abre.</span><span class="sxs-lookup"><span data-stu-id="e6321-131">The client creates a [service proxy](service-proxy.md) and opens it.</span></span>
-   <span data-ttu-id="e6321-132">O cliente chama a função Add do serviço e passa o proxy de serviço.</span><span class="sxs-lookup"><span data-stu-id="e6321-132">The client calls the Add function of the service, and passes in the service proxy.</span></span>
-   <span data-ttu-id="e6321-133">A mensagem é serializada de acordo com os metadados de serialização no cabeçalho e nos arquivos de origem gerados pela ferramenta de metadados ([WsUtil.exe](web-service-compiler-tool.md)).</span><span class="sxs-lookup"><span data-stu-id="e6321-133">The message is serialized according to the serialization metadata in the header and source files generated by the metadata tool ([WsUtil.exe](web-service-compiler-tool.md)).</span></span>
-   <span data-ttu-id="e6321-134">A mensagem é gravada no canal e é transmitida pela rede para o serviço.</span><span class="sxs-lookup"><span data-stu-id="e6321-134">The message is written to the channel and is transmitted over the network to the service.</span></span>
-   <span data-ttu-id="e6321-135">No lado do servidor, o serviço é hospedado dentro de um host de serviço e tem um ponto de extremidade ouvindo o contrato ICalculator.</span><span class="sxs-lookup"><span data-stu-id="e6321-135">On the server side, the service is hosted inside a service host, and has an endpoint listening for the ICalculator contract.</span></span>
-   <span data-ttu-id="e6321-136">Usando os metadados do modelo de serviço no stub, o serviço desserializa a mensagem do cliente e a despacha para o stub.</span><span class="sxs-lookup"><span data-stu-id="e6321-136">Using the Service Model metadata in the stub, the service deserializes the message from the client and dispatches it to the stub.</span></span>
-   <span data-ttu-id="e6321-137">O serviço do lado do servidor chama o método Add, passando-o para o contexto da operação.</span><span class="sxs-lookup"><span data-stu-id="e6321-137">The server-side service calls the Add method, passing it the operation context.</span></span> <span data-ttu-id="e6321-138">Este contexto de operação contém a referência à mensagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="e6321-138">This operation context contains the reference to the incoming message.</span></span>

![Diagrama mostrando a interação dos componentes individuais do modelo do serviço WWSAPI.](images/servicemodellayout.png)

<span data-ttu-id="e6321-140">Componentes</span><span class="sxs-lookup"><span data-stu-id="e6321-140">Components</span></span>

-   <span data-ttu-id="e6321-141">[Host de serviço](service-host.md): hospeda um serviço.</span><span class="sxs-lookup"><span data-stu-id="e6321-141">[Service host](service-host.md): Hosts a service.</span></span>
-   <span data-ttu-id="e6321-142">[Proxy de serviço](service-proxy.md): define como um cliente se comunica com um serviço.</span><span class="sxs-lookup"><span data-stu-id="e6321-142">[Service proxy](service-proxy.md): Defines how a client communicates with a service.</span></span>
-   <span data-ttu-id="e6321-143">[Contexto](context.md): recipiente de propriedades para disponibilizar informações específicas de estado para uma operação de serviço.</span><span class="sxs-lookup"><span data-stu-id="e6321-143">[Context](context.md): Property bag for making state-specific information available to a service operation.</span></span>
-   <span data-ttu-id="e6321-144">[Contrato](contract.md): a definição de interface de um serviço.</span><span class="sxs-lookup"><span data-stu-id="e6321-144">[Contract](contract.md): The interface definition of a service.</span></span> <span data-ttu-id="e6321-145">Por exemplo, ICalculator representa um contrato para o serviço de calculadora em nosso código de exemplo.</span><span class="sxs-lookup"><span data-stu-id="e6321-145">For example, ICalculator represents a contract for the calculator service in our example code.</span></span>
-   <span data-ttu-id="e6321-146">[WsUtil.exe](web-service-compiler-tool.md): a ferramenta de metadados do modelo de serviço para gerar proxies e stubs.</span><span class="sxs-lookup"><span data-stu-id="e6321-146">[WsUtil.exe](web-service-compiler-tool.md): The Service Model metadata tool for generating proxies and stubs.</span></span>

 

 




