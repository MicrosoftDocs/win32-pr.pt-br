---
title: Criando um cliente
description: A criação de um cliente para serviços Web é bastante simplificada no WWSAPI pela API do modelo de serviço e pela ferramenta de WsUtil.exe.
ms.assetid: 09f489e8-958d-4bc5-a232-aa59bd75333a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606a68f574a9ad79d15f3ddd48247f93a5414250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364434"
---
# <a name="creating-a-client"></a><span data-ttu-id="18f21-103">Criando um cliente</span><span class="sxs-lookup"><span data-stu-id="18f21-103">Creating a Client</span></span>

<span data-ttu-id="18f21-104">A criação de um cliente para serviços Web é bastante simplificada no WWSAPI pela API do [modelo de serviço](service-model-layer-overview.md) e pela ferramenta de [WsUtil.exe](wsutil-compiler-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="18f21-104">Creating a client for Web services is greatly simplified in WWSAPI by the [Service Model](service-model-layer-overview.md) API and the [WsUtil.exe](wsutil-compiler-tool.md) tool.</span></span> <span data-ttu-id="18f21-105">O modelo de serviço fornece uma API que permite que o cliente envie e receba [mensagens](message.md) em um [canal](channel.md) como chamadas de método C.</span><span class="sxs-lookup"><span data-stu-id="18f21-105">The Service Model provides an API that enables the client to send and receive [messages](message.md) over a [channel](channel.md) as C method calls.</span></span> <span data-ttu-id="18f21-106">A ferramenta WsUtil gera cabeçalhos e auxiliares para implementar o cliente.</span><span class="sxs-lookup"><span data-stu-id="18f21-106">The WsUtil tool generates headers and helpers for implementing the client.</span></span> <span data-ttu-id="18f21-107">Esses cabeçalhos incluem os tipos e os protótipos de função para funções C que representam os serviços oferecidos pelo serviço Web de destino.</span><span class="sxs-lookup"><span data-stu-id="18f21-107">These headers include the types and function prototypes for C functions representing the services offered by the target Web service.</span></span> <span data-ttu-id="18f21-108">Os auxiliares são usados para criar o proxy de serviço, que contém as informações de associação e o [endereço do ponto de extremidade](endpoint-address.md) para o serviço.</span><span class="sxs-lookup"><span data-stu-id="18f21-108">The helpers are used to create the service proxy, which contains the binding information and [endpoint address](endpoint-address.md) for the service.</span></span>

## <a name="using-wsutil-to-generate-headers-and-helpers"></a><span data-ttu-id="18f21-109">Usando WsUtil para gerar cabeçalhos e auxiliares</span><span class="sxs-lookup"><span data-stu-id="18f21-109">Using WsUtil to Generate Headers and Helpers</span></span>

<span data-ttu-id="18f21-110">Para gerar os cabeçalhos e auxiliares, o WsUtil é aberto e lê os arquivos de metadados para o serviço de destino – arquivos WSDL e XSD — e os converte em cabeçalhos; Portanto, é necessário recuperar os arquivos de metadados para o serviço de destino com antecedência, por exemplo, usando SvcUtil, uma parte do Windows Communication Foundation.</span><span class="sxs-lookup"><span data-stu-id="18f21-110">To generate the headers and helpers, WsUtil opens and reads the metadata files for the target service — wsdl and xsd files— and converts them into headers; therefore, it is necessary to retrieve the metadata files for the target service in advance, for example by using SvcUtil, a part of the Windows Communication Foundation.</span></span> <span data-ttu-id="18f21-111">Por motivos de segurança, é imperativo que suas cópias desses arquivos sejam confiáveis.</span><span class="sxs-lookup"><span data-stu-id="18f21-111">For security reasons, it is imperative that your copies of these files are trustworthy.</span></span> <span data-ttu-id="18f21-112">(Para obter mais informações, consulte a seção "segurança" do tópico da [ferramenta do compilador WsUtil](wsutil-compiler-tool.md) .)</span><span class="sxs-lookup"><span data-stu-id="18f21-112">(For more information, see the "Security" section of the [WsUtil Compiler Tool](wsutil-compiler-tool.md) topic.)</span></span>

<span data-ttu-id="18f21-113">Para executar o WsUtil, use a seguinte sintaxe de linha de comando se os arquivos WSDL e XSD do serviço estiverem em seu próprio diretório: `WsUtil.exe *.wsdl *.xsd` .</span><span class="sxs-lookup"><span data-stu-id="18f21-113">To run WsUtil, use the following command-line syntax if the WSDL and XSD files for the service are in their own directory: `WsUtil.exe *.wsdl *.xsd`.</span></span> <span data-ttu-id="18f21-114">Como alternativa, você pode especificar os arquivos por nome completo.</span><span class="sxs-lookup"><span data-stu-id="18f21-114">Alternatively, you can specify the files by full name.</span></span>

<span data-ttu-id="18f21-115">O WsUtil geralmente gera dois arquivos para cada arquivo de metadados: um cabeçalho e um arquivo C.</span><span class="sxs-lookup"><span data-stu-id="18f21-115">WsUtil generally generates two files for each metadata file: a header and a C file.</span></span> <span data-ttu-id="18f21-116">Adicione esses arquivos ao seu projeto de codificação e use \# instruções include para incluí-los no código do seu cliente.</span><span class="sxs-lookup"><span data-stu-id="18f21-116">Add these files to your coding project, and use \#include statements to include them in the code for your client.</span></span> <span data-ttu-id="18f21-117">(Os arquivos XSD representam tipos e os arquivos WSDL representam operações.)</span><span class="sxs-lookup"><span data-stu-id="18f21-117">(The XSD files represent types, and the WSDL files represent operations.)</span></span>

## <a name="creating-the-service-proxy"></a><span data-ttu-id="18f21-118">Criando o proxy de serviço</span><span class="sxs-lookup"><span data-stu-id="18f21-118">Creating the Service Proxy</span></span>

<span data-ttu-id="18f21-119">O cabeçalho gerado por WsUtil contém uma rotina auxiliar para criar o proxy de serviço com a associação necessária.</span><span class="sxs-lookup"><span data-stu-id="18f21-119">The header generated by WsUtil contains a helper routine for creating the service proxy with the required binding.</span></span> <span data-ttu-id="18f21-120">Essa rotina está incluída na seção "rotinas auxiliares de política" do arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="18f21-120">This routine is included in the "Policy helper routines" section of the generated header file.</span></span> <span data-ttu-id="18f21-121">Por exemplo, o cabeçalho gerado para o serviço de calculadora ilustrado no exemplo [httpcalculatorclientexample](httpcalculatorclientexample.md) conterá o protótipo de função a seguir.</span><span class="sxs-lookup"><span data-stu-id="18f21-121">For example, the generated header for the calculator service illustrated in the [httpcalculatorclientexample](httpcalculatorclientexample.md) example will contain the following function prototype.</span></span>


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



<span data-ttu-id="18f21-122">Incorpore esse auxiliar em seu código e passe um identificador de [ \_ \_ proxy de serviço WS](ws-service-proxy.md) para receber o identificador para o proxy de serviço criado.</span><span class="sxs-lookup"><span data-stu-id="18f21-122">Incorporate this helper in your code and pass a [WS\_SERVICE\_PROXY](ws-service-proxy.md) handle to receive the handle to the created service proxy.</span></span> <span data-ttu-id="18f21-123">No cenário mais simples, no qual apenas um identificador de proxy de serviço e um objeto de erro são passados para a função, a chamada é semelhante ao seguinte.</span><span class="sxs-lookup"><span data-stu-id="18f21-123">In the simplest scenario, in which only a service proxy handle and an error object are passed to the function, the call looks like the following.</span></span>


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



<span data-ttu-id="18f21-124">Para criar a parte de endereço do proxy de serviço, chame [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) com um identificador para o proxy de serviço e um ponteiro para um [**\_ \_ endereço de ponto de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) contendo o endereço do ponto de extremidade de serviço ao qual você deseja se conectar.</span><span class="sxs-lookup"><span data-stu-id="18f21-124">To create the address portion of the service proxy, call [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) with a handle to the service proxy and a pointer to a [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) containing the service endpoint address to which you wish to connect.</span></span>

## <a name="implementing-the-client-with-function-prototypes"></a><span data-ttu-id="18f21-125">Implementando o cliente com protótipos de função</span><span class="sxs-lookup"><span data-stu-id="18f21-125">Implementing the Client with Function Prototypes</span></span>

<span data-ttu-id="18f21-126">Os cabeçalhos gerados nos arquivos WSDL de serviço também contêm protótipos de função C que representam os serviços disponíveis do serviço Web e específicos para a associação necessária.</span><span class="sxs-lookup"><span data-stu-id="18f21-126">The headers generated from the service WSDL files also contain C function prototypes representing the services available from the Web service and specific to the binding required.</span></span> <span data-ttu-id="18f21-127">Por exemplo, um cabeçalho gerado para o serviço de calculadora ilustrado em HttpCalculatorServiceExample conterá o protótipo a seguir para a operação de multiplicação desse serviço.</span><span class="sxs-lookup"><span data-stu-id="18f21-127">For example, a header generated for the calculator service illustrated in HttpCalculatorServiceExample will contain the following prototype for that service's multiplication operation.</span></span>

``` syntax
HRESULT BasicHttpBinding_ICalculator_Multiply(
    __in WS_SERVICE_PROXY* _serviceProxy,
    __in double n1,
    __in double n2,
    __out double* MultiplyResult,
    __in WS_HEAP* _heap,
    __in_ecount_opt(_callPropertyCount) const WS_CALL_PROPERTY* _callProperties,
    __in const ULONG _callPropertyCount,
    __in_opt const WS_ASYNC_CONTEXT* _asyncContext,
    __in_opt WS_ERROR* _error);
```

<span data-ttu-id="18f21-128">Você pode copiar os protótipos e usá-los como modelos para codificar as chamadas de função em seu cliente, em cada caso passando o identificador para o proxy de serviço.</span><span class="sxs-lookup"><span data-stu-id="18f21-128">You can copy the prototypes and use them as templates for coding the function calls in your client, in each case passing the handle to service proxy.</span></span> <span data-ttu-id="18f21-129">Quando terminar com o proxy de serviço, chame [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).</span><span class="sxs-lookup"><span data-stu-id="18f21-129">When you are finished with the service proxy, call [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).</span></span>

 

 




