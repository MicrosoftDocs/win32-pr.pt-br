---
description: O HTTP revolucionou o uso do computador permitindo que as pessoas usem um navegador da Web para facilitar o acesso a informações em um servidor remoto em uma rede.
ms.assetid: 44f3ff21-4978-4902-aa74-ddeef60881db
title: Visão geral do serviço SOAP COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93ce7d80753f306777d3ac0b77dc46dc4e08d22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753205"
---
# <a name="com-soap-service-overview"></a><span data-ttu-id="27c4a-103">Visão geral do serviço SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="27c4a-103">COM+ SOAP Service Overview</span></span>

<span data-ttu-id="27c4a-104">O HTTP revolucionou o uso do computador permitindo que as pessoas usem um navegador da Web para facilitar o acesso a informações em um servidor remoto em uma rede.</span><span class="sxs-lookup"><span data-stu-id="27c4a-104">HTTP revolutionized computer use by allowing people to use a Web browser for easy access to information on a remote server over a network.</span></span> <span data-ttu-id="27c4a-105">Os serviços Web XML agora revolucionaram o desenvolvimento de aplicativos, permitindo que aplicativos cliente chamem facilmente métodos remotos em uma rede.</span><span class="sxs-lookup"><span data-stu-id="27c4a-105">XML web services have now revolutionized application development by allowing client applications to easily call remote methods over a network.</span></span>

<span data-ttu-id="27c4a-106">Geralmente, é útil que um aplicativo cliente possa chamar um método implementado em um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="27c4a-106">It is often useful for a client application to be able to call a method implemented on a remote server.</span></span> <span data-ttu-id="27c4a-107">Às vezes, o método usa informações voláteis armazenadas no servidor remoto (por exemplo, um método que retorna o preço atual da bolsa correspondente a um determinado símbolo de marca).</span><span class="sxs-lookup"><span data-stu-id="27c4a-107">Sometimes the method makes use of volatile information stored on the remote server (for example, a method that returns the current price of the stock corresponding to a given ticker symbol).</span></span> <span data-ttu-id="27c4a-108">Em outras ocasiões, o desenvolvedor quer a capacidade de atualizar a implementação de métodos sem precisar reimplantar todos os aplicativos que o utilizam.</span><span class="sxs-lookup"><span data-stu-id="27c4a-108">At other times, the developer wants the ability to upgrade the methods implementation without having to redeploy all the applications that use it.</span></span>

<span data-ttu-id="27c4a-109">Assim como as páginas da Web, os serviços XML são acessados por meio de um servidor Web, como o IIS, usando HTTP.</span><span class="sxs-lookup"><span data-stu-id="27c4a-109">Like webpages, XML web services are accessed via a web server, such as IIS, using HTTP.</span></span> <span data-ttu-id="27c4a-110">No entanto, em vez de páginas da Web codificadas em HTML, esses pacotes HTTP contêm os parâmetros de entrada e saída de chamadas para um método implementado no servidor, codificado em SOAP.</span><span class="sxs-lookup"><span data-stu-id="27c4a-110">However, instead of webpages encoded in HTML, these HTTP packets contain the input and output parameters of calls to a method implemented on the server, encoded in SOAP.</span></span>

<span data-ttu-id="27c4a-111">Para usar um serviço Web XML, você precisa saber a URL onde o serviço é exposto e o nome do método que você deseja chamar, e deve fornecer os parâmetros de entrada para o método.</span><span class="sxs-lookup"><span data-stu-id="27c4a-111">To use an XML web service, you need to know the URL where the service is exposed and the name of the method you want to call, and you must provide the input parameters to the method.</span></span> <span data-ttu-id="27c4a-112">[O padrão SOAP 1,1](https://www.w3.org/TR/SOAP/) fornece o exemplo a seguir de um pacote http que contém uma chamada remota para um serviço Web XML em https://www.stockquoteserver.com/StockQuote , que retorna o preço atual da ação correspondente a um determinado símbolo de marca.</span><span class="sxs-lookup"><span data-stu-id="27c4a-112">[The SOAP 1.1 standard](https://www.w3.org/TR/SOAP/) provides the following example of an HTTP packet containing a remote call to an XML web service at https://www.stockquoteserver.com/StockQuote, which returns the current price of the stock corresponding to a given ticker symbol.</span></span>

``` syntax
POST /StockQuote HTTP/1.1
Host: www.stockquoteserver.com
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn
SOAPAction: "Some-URI"

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding/">
<SOAP-ENV:Body>
<m:GetLastTradePrice xmlns:m="Some-URI">
<symbol>DIS</symbol>
</m:GetLastTradePrice>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<span data-ttu-id="27c4a-113">Como o exemplo anterior ilustra, SOAP é uma instância XML que pode ser inserida em uma solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="27c4a-113">As the preceding example illustrates, SOAP is an XML instance that can be embedded in an HTTP request.</span></span> <span data-ttu-id="27c4a-114">Da mesma forma, o resultado é retornado como um pacote HTTP com uma carga SOAP, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="27c4a-114">Similarly, the result is returned as an HTTP packet with a SOAP payload, as shown in the following example.</span></span>

``` syntax
HTTP/1.1 200 OK
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding//">
<SOAP-ENV:Body>
<m:GetLastTradePriceResponse xmlns:m="Some-URI">
<Price>34.5</Price>
</m:GetLastTradePriceResponse>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<span data-ttu-id="27c4a-115">Embora seja útil ter alguma compreensão da infraestrutura que se baseia em serviços Web XML, o COM+ facilita a criação e o uso de Web Services XML que, com frequência, você não precisará mais se aprofundar nesse nível.</span><span class="sxs-lookup"><span data-stu-id="27c4a-115">While it is helpful to have some understanding of the infrastructure that underlies XML web services, COM+ makes it so easy to create and use XML web services that you won't often have to delve to this level.</span></span>

<span data-ttu-id="27c4a-116">Você pode expor os métodos nas interfaces padrão dos componentes COM configurados em qualquer aplicativo COM+ como um serviço Web XML.</span><span class="sxs-lookup"><span data-stu-id="27c4a-116">You can expose the methods in the default interfaces of the configured COM components in any COM+ application as an XML web service.</span></span> <span data-ttu-id="27c4a-117">Nenhuma consideração especial de programação é necessária ao gravar os componentes, exceto que os métodos que você deseja expor devem estar na interface padrão e o componente deve ser configurado (no catálogo COM+ do seu servidor).</span><span class="sxs-lookup"><span data-stu-id="27c4a-117">No special programming considerations are necessary when writing the components, except that the methods you want to expose must be in the default interface and the component must be configured (in your server's COM+ catalog).</span></span> <span data-ttu-id="27c4a-118">Você não precisa escrever código para se comunicar por meio de uma interface de rede ou para analisar SOAP.</span><span class="sxs-lookup"><span data-stu-id="27c4a-118">You need not write code to communicate via a network interface or to parse SOAP.</span></span> <span data-ttu-id="27c4a-119">Para obter instruções detalhadas sobre como usar o serviço SOAP COM+ para criar um serviço Web XML, consulte [criando XML Web Services](creating-xml-web-services.md).</span><span class="sxs-lookup"><span data-stu-id="27c4a-119">For detailed instructions about using the COM+ SOAP service to create an XML web service, see [Creating XML Web Services](creating-xml-web-services.md).</span></span>

<span data-ttu-id="27c4a-120">Quando você expõe um aplicativo COM+ como um serviço Web XML, informações detalhadas sobre a sintaxe de todos os métodos disponíveis de um serviço Web XML são publicadas automaticamente, usando o WSDL (Web Services Description Language).</span><span class="sxs-lookup"><span data-stu-id="27c4a-120">When you expose a COM+ application as an XML web service, detailed information about the syntax of all the methods available from an XML web service is published automatically, using the Web Services Description Language (WSDL).</span></span> <span data-ttu-id="27c4a-121">Essas informações são usadas por clientes que usam o serviço Web XML.</span><span class="sxs-lookup"><span data-stu-id="27c4a-121">This information is used by clients that use your XML web service.</span></span>

<span data-ttu-id="27c4a-122">O COM+ fornece duas maneiras de acessar e usar um serviço Web XML remoto, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="27c4a-122">COM+ provides two ways for you to access and use a remote XML web service, as follows:</span></span>

-   <span data-ttu-id="27c4a-123">O modo WKO ( *well-known Object* ) pode ser usado para acessar qualquer serviço Web XML que publica sua sintaxe usando WSDL, mesmo se esse serviço Web XML não tiver sido criado usando com+ ou mesmo Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="27c4a-123">The *well-known object* (WKO) mode can be used to access any XML web service that publishes its syntax using WSDL, even if that XML web service was not created using COM+ or even Microsoft Windows.</span></span>
-   <span data-ttu-id="27c4a-124">O modo Cao ( *objeto ativado pelo cliente* ) pode ser usado somente para acessar serviços Web XML criados pela exposição de aplicativos com+.</span><span class="sxs-lookup"><span data-stu-id="27c4a-124">The *client-activated object* (CAO) mode can be used only to access XML web services created by exposing COM+ applications.</span></span> <span data-ttu-id="27c4a-125">O modo CAO aumenta o desempenho usando conexões persistentes, um recurso sem suporte do padrão SOAP atual.</span><span class="sxs-lookup"><span data-stu-id="27c4a-125">CAO mode increases performance by using persistent connections, a feature not supported by the current SOAP standard.</span></span>

<span data-ttu-id="27c4a-126">Ambos os métodos permitem que aplicativos cliente chamem os métodos de serviços Web XML remotamente de maneira simples, sem precisar escrever código para se comunicar por meio de uma interface de rede ou analisar SOAP.</span><span class="sxs-lookup"><span data-stu-id="27c4a-126">Both methods allow client applications to call the methods of XML web services remotely in a straightforward fashion, without having to write code to communicate via a network interface or parse SOAP.</span></span> <span data-ttu-id="27c4a-127">Para obter detalhes sobre como acessar os serviços Web XML em ambos os modos, consulte [acessando serviços Web XML no modo Cao](accessing-xml-web-services-in-cao-mode.md) e [acessando Web Services XML no modo WKO](accessing-xml-web-services-in-wko-mode.md).</span><span class="sxs-lookup"><span data-stu-id="27c4a-127">For details about how to access XML web services in either mode, see [Accessing XML Web Services in CAO Mode](accessing-xml-web-services-in-cao-mode.md) and [Accessing XML Web Services in WKO Mode](accessing-xml-web-services-in-wko-mode.md).</span></span>

> [!Note]  
> <span data-ttu-id="27c4a-128">O COM+ dá suporte apenas à especificação SOAP-RPC, não à especificação de SOAP-Document.</span><span class="sxs-lookup"><span data-stu-id="27c4a-128">COM+ supports only the SOAP-RPC specification, not the SOAP-Document specification.</span></span>

 

<span data-ttu-id="27c4a-129">O COM+ torna o uso de serviços Web XML especialmente fácil, permitindo que você use aplicativos COM+ existentes como serviços Web XML no modo CAO de maneira totalmente transparente.</span><span class="sxs-lookup"><span data-stu-id="27c4a-129">COM+ makes using XML web services especially easy by allowing you to use existing COM+ applications as XML web services in CAO mode in a completely transparent fashion.</span></span> <span data-ttu-id="27c4a-130">Se você [Exportar](exporting-a-soap-enabled-application.md) um aplicativo com+ que foi exposto como um serviço Web XML do seu servidor, qualquer cliente que [importar](importing-a-soap-enabled-application.md) o aplicativo poderá usar de modo transparente o serviço Web XML do servidor sempre que o aplicativo importado for usado.</span><span class="sxs-lookup"><span data-stu-id="27c4a-130">If you [export](exporting-a-soap-enabled-application.md) a COM+ application that has been exposed as an XML web service from your server, any client that [imports](importing-a-soap-enabled-application.md) the application can transparently use the server's XML web service whenever the imported application is used.</span></span> <span data-ttu-id="27c4a-131">Esse recurso torna a conversão de aplicativos COM+ existentes em XML Web Services e a implantação desses serviços em uma rede muito fácil.</span><span class="sxs-lookup"><span data-stu-id="27c4a-131">This facility makes the conversion of existing COM+ applications to XML web services and the deployment of those services over a network very easy.</span></span>

<span data-ttu-id="27c4a-132">O uso de Web Services XML tem várias vantagens exclusivas sobre implementações alternativas de RPC (chamadas de procedimento remoto), incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="27c4a-132">Using XML web services has several unique advantages over alternative implementations of remote procedure calls (RPC), including the following:</span></span>

-   <span data-ttu-id="27c4a-133">SOAP é uma implementação de RPC de plataforma cruzada verdadeira, o que aumenta a interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="27c4a-133">SOAP is a true cross-platform RPC implementation, which increases interoperability.</span></span>
-   <span data-ttu-id="27c4a-134">Os serviços Web XML dão suporte a métodos com parâmetros de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="27c4a-134">XML web services support methods with both input and output parameters.</span></span>
-   <span data-ttu-id="27c4a-135">Os serviços Web XML são executados sobre HTTP, o que normalmente pode penetrar firewalls que podem bloquear outras implementações RPC.</span><span class="sxs-lookup"><span data-stu-id="27c4a-135">XML web services run over HTTP, which can usually penetrate firewalls that might block other RPC implementations.</span></span>
-   <span data-ttu-id="27c4a-136">Quando um serviço Web XML é implementado usando COM+, o desenvolvedor não precisa escrever nenhum código especializado; Essa é uma enorme vantagem em relação aos mecanismos alternativos de RPC.</span><span class="sxs-lookup"><span data-stu-id="27c4a-136">When an XML web service is implemented using COM+, the developer does not have to write any specialized code; this is a tremendous advantage over alternative RPC mechanisms.</span></span>

> [!Note]  
> <span data-ttu-id="27c4a-137">Os serviços Web XML não oferecem suporte a chamadas assíncronas ou transacionais de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="27c4a-137">XML web services do not support asynchronous or transparently transactional calls.</span></span> <span data-ttu-id="27c4a-138">Use o serviço de [componentes em fila com+](com--queued-components.md) quando você precisar dessa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="27c4a-138">Use the [COM+ Queued Components](com--queued-components.md) service when you require this functionality.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="27c4a-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27c4a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27c4a-140">Considerações de segurança do serviço SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="27c4a-140">COM+ SOAP Service Security Considerations</span></span>](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



