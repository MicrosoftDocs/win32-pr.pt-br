---
title: Sobre os serviços Web do Windows
description: A API de serviços Web do Windows é uma API em camadas e pode ser a imagem a seguir.
ms.assetid: 6e8c23d1-c86b-432d-8e0c-e16982849239
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7546aaa72d58e43d7faefccf394a3e27756f4a96
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104567295"
---
# <a name="about-windows-web-services"></a><span data-ttu-id="213fd-103">Sobre os serviços Web do Windows</span><span class="sxs-lookup"><span data-stu-id="213fd-103">About Windows Web Services</span></span>

<span data-ttu-id="213fd-104">A API de serviços Web do Windows é uma API em camadas e pode ser apresentada da seguinte maneira</span><span class="sxs-lookup"><span data-stu-id="213fd-104">The Windows Web Services API is a layered API and it may be pictured as follows</span></span>

![Diagrama mostrando as camadas e áreas de camada cruzada da API dos serviços Web do Windows.](images/apistack.png)

<span data-ttu-id="213fd-106">O WWSAPI é uma API em camadas.</span><span class="sxs-lookup"><span data-stu-id="213fd-106">The WWSAPI is a layered API.</span></span> <span data-ttu-id="213fd-107">Esperamos que a maioria dos desenvolvedores direcione o modelo de serviço, que é um modelo de programação baseado em método.</span><span class="sxs-lookup"><span data-stu-id="213fd-107">We expect most developers to target the Service Model, which is a method-based programming model.</span></span> <span data-ttu-id="213fd-108">No modelo de serviço, o host de serviço fornece o modelo de programação do lado do servidor, enquanto o proxy de serviço fornece o modelo de programação do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="213fd-108">In the Service Model, the Service Host provides the server side programming model, while Service Proxy provides the client side programming model.</span></span>

<span data-ttu-id="213fd-109">Cada camada expõe um conjunto de APIs e tipos que podem ser usados com APIs dessa camada.</span><span class="sxs-lookup"><span data-stu-id="213fd-109">Every layer exposes a set of APIs and types that can be used with APIs of that layer.</span></span>

## <a name="service-model"></a><span data-ttu-id="213fd-110">Modelo de serviço</span><span class="sxs-lookup"><span data-stu-id="213fd-110">Service Model</span></span>

<span data-ttu-id="213fd-111">A camada de nível superior chamada [modelo de serviço](service-model-layer-overview.md) fornece um modelo de programação baseado em método e é o modelo mais fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="213fd-111">The top level layer called the [Service Model](service-model-layer-overview.md) provides a method-based programming model and it is the easiest model to use.</span></span> <span data-ttu-id="213fd-112">No modelo de serviço, o [host de serviço](service-host.md) fornece o modelo de programação do lado do servidor, enquanto o [proxy de serviço](service-proxy.md) fornece o modelo de programação do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="213fd-112">In the Service Model, the [Service Host](service-host.md) provides the server side programming model, while the [Service Proxy](service-proxy.md) provides the client side programming model.</span></span> <span data-ttu-id="213fd-113">O [contexto](context.md) é usado dentro do modelo de serviço para passar um estado relevante disponível para a operação de serviço e/ou o retorno de chamada quando ele é invocado.</span><span class="sxs-lookup"><span data-stu-id="213fd-113">[Context](context.md) is used within the Service Model to pass in a relevant state available to the service operation and/or the callback when it is invoked.</span></span> <span data-ttu-id="213fd-114">E o [contrato de serviço](contract.md) é usado para especificar um contrato de serviço em um ponto de extremidade exposto no serviço.</span><span class="sxs-lookup"><span data-stu-id="213fd-114">And [Service Contract](contract.md) is used to specify a service contract on an endpoint exposed on the service.</span></span> <span data-ttu-id="213fd-115">Os seguintes componentes e operações fazem parte da camada de serviço:</span><span class="sxs-lookup"><span data-stu-id="213fd-115">The following components and operations are part of the Service Layer:</span></span>

-   [<span data-ttu-id="213fd-116">Host de serviço</span><span class="sxs-lookup"><span data-stu-id="213fd-116">Service Host</span></span>](service-host.md)
-   [<span data-ttu-id="213fd-117">Proxy de serviço</span><span class="sxs-lookup"><span data-stu-id="213fd-117">Service Proxy</span></span>](service-proxy.md)
-   [<span data-ttu-id="213fd-118">Contexto</span><span class="sxs-lookup"><span data-stu-id="213fd-118">Context</span></span>](context.md)
-   [<span data-ttu-id="213fd-119">Contrato</span><span class="sxs-lookup"><span data-stu-id="213fd-119">Contract</span></span>](contract.md)
-   [<span data-ttu-id="213fd-120">Metadados de serviço</span><span class="sxs-lookup"><span data-stu-id="213fd-120">Service Metadata</span></span>](service-metadata.md)

## <a name="channel-layer"></a><span data-ttu-id="213fd-121">Camada de canal</span><span class="sxs-lookup"><span data-stu-id="213fd-121">Channel Layer</span></span>

<span data-ttu-id="213fd-122">O modelo de serviço é criado com base em uma camada de canal, que fornece flexibilidade total, mas é mais difícil de usar.</span><span class="sxs-lookup"><span data-stu-id="213fd-122">The Service Model is built upon a Channel Layer, which provides full flexibility but is more difficult to use.</span></span> <span data-ttu-id="213fd-123">Os seguintes componentes e operações fazem parte da camada de canal:</span><span class="sxs-lookup"><span data-stu-id="213fd-123">The following components and operations are part of the Channel Layer:</span></span>

-   [<span data-ttu-id="213fd-124">Message</span><span class="sxs-lookup"><span data-stu-id="213fd-124">Message</span></span>](message.md)
-   [<span data-ttu-id="213fd-125">Channel</span><span class="sxs-lookup"><span data-stu-id="213fd-125">Channel</span></span>](channel.md)
-   [<span data-ttu-id="213fd-126">Ouvinte</span><span class="sxs-lookup"><span data-stu-id="213fd-126">Listener</span></span>](listener.md)
-   [<span data-ttu-id="213fd-127">Falhas</span><span class="sxs-lookup"><span data-stu-id="213fd-127">Faults</span></span>](faults.md)
-   [<span data-ttu-id="213fd-128">URL</span><span class="sxs-lookup"><span data-stu-id="213fd-128">Url</span></span>](url.md)
-   [<span data-ttu-id="213fd-129">Segurança</span><span class="sxs-lookup"><span data-stu-id="213fd-129">Security</span></span>](security-overview.md)
-   [<span data-ttu-id="213fd-130">Importação de metadados</span><span class="sxs-lookup"><span data-stu-id="213fd-130">Metadata Import</span></span>](metadata-import.md)

## <a name="xml-layer"></a><span data-ttu-id="213fd-131">Camada XML</span><span class="sxs-lookup"><span data-stu-id="213fd-131">XML Layer</span></span>

<span data-ttu-id="213fd-132">A camada de canal, por sua vez, é criada com base em uma estrutura XML leve, que inclui a desserialização de tipos de dados C.</span><span class="sxs-lookup"><span data-stu-id="213fd-132">The Channel Layer is in turn built upon a lightweight XML framework, which includes deserialization of C data types.</span></span> <span data-ttu-id="213fd-133">Os seguintes componentes e operações fazem parte da camada XML:</span><span class="sxs-lookup"><span data-stu-id="213fd-133">The following components and operations are part of the XML Layer:</span></span>

-   [<span data-ttu-id="213fd-134">Gravador de XML</span><span class="sxs-lookup"><span data-stu-id="213fd-134">XML Writer</span></span>](xml-writer.md)
-   [<span data-ttu-id="213fd-135">Leitor de XML</span><span class="sxs-lookup"><span data-stu-id="213fd-135">XML Reader</span></span>](xml-reader.md)
-   [<span data-ttu-id="213fd-136">Buffer XML</span><span class="sxs-lookup"><span data-stu-id="213fd-136">XML Buffer</span></span>](xml-buffer.md)
-   [<span data-ttu-id="213fd-137">Série</span><span class="sxs-lookup"><span data-stu-id="213fd-137">Serialization</span></span>](serialization.md)
-   [<span data-ttu-id="213fd-138">Suporte à linguagem XML</span><span class="sxs-lookup"><span data-stu-id="213fd-138">XML Language Support</span></span>](xml-language-support.md)

## <a name="common-to-all-layers"></a><span data-ttu-id="213fd-139">Comum a todas as camadas</span><span class="sxs-lookup"><span data-stu-id="213fd-139">Common to all layers</span></span>

<span data-ttu-id="213fd-140">Veja a seguir os tópicos que se aplicam a qualquer uma das três camadas:</span><span class="sxs-lookup"><span data-stu-id="213fd-140">The following are topics that apply to any of the three layers:</span></span>

-   [<span data-ttu-id="213fd-141">Erros</span><span class="sxs-lookup"><span data-stu-id="213fd-141">Errors</span></span>](errors.md)
-   [<span data-ttu-id="213fd-142">Modelo assíncrono</span><span class="sxs-lookup"><span data-stu-id="213fd-142">Asynchronous Model</span></span>](asynchronous-model.md)
-   [<span data-ttu-id="213fd-143">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="213fd-143">Thread Safety</span></span>](thread-safety.md)
-   [<span data-ttu-id="213fd-144">Rastreamento</span><span class="sxs-lookup"><span data-stu-id="213fd-144">Tracing</span></span>](tracing.md)
-   [<span data-ttu-id="213fd-145">Cancelamento</span><span class="sxs-lookup"><span data-stu-id="213fd-145">Cancellation</span></span>](cancellation.md)
-   [<span data-ttu-id="213fd-146">Utilitários</span><span class="sxs-lookup"><span data-stu-id="213fd-146">Utilities</span></span>](utilities.md)
-   [<span data-ttu-id="213fd-147">Depuração</span><span class="sxs-lookup"><span data-stu-id="213fd-147">Debugging</span></span>](debugging.md)
-   [<span data-ttu-id="213fd-148">Ferramenta de compilador do Wsutil</span><span class="sxs-lookup"><span data-stu-id="213fd-148">Wsutil Compiler tool</span></span>](wsutil-compiler-tool.md)
-   [<span data-ttu-id="213fd-149">Áreas</span><span class="sxs-lookup"><span data-stu-id="213fd-149">Heap</span></span>](heap.md)

## <a name="examples"></a><span data-ttu-id="213fd-150">Exemplos</span><span class="sxs-lookup"><span data-stu-id="213fd-150">Examples</span></span>

<span data-ttu-id="213fd-151">Para obter mais informações sobre elementos de API, consulte [referência de serviços Web do Windows](windows-web-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="213fd-151">For more information about API elements, see [Windows Web Services Reference](windows-web-services-reference.md).</span></span> <span data-ttu-id="213fd-152">Para obter exemplos de como usar a API, consulte [usando os serviços Web do Windows](using-windows-web-services.md).</span><span class="sxs-lookup"><span data-stu-id="213fd-152">For examples of using the API, see [Using Windows Web Services](using-windows-web-services.md).</span></span>

 

 




