---
description: Http revolutionized computer use, permitindo que as pessoas usem um navegador da Web para facilitar o acesso a informações em um servidor remoto em uma rede.
ms.assetid: 44f3ff21-4978-4902-aa74-ddeef60881db
title: Visão geral do serviço COM+ SOAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68501d80596d8547715cb1694fe77a17a3ab4b6955ad1e1acd596f249be5f231
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096866"
---
# <a name="com-soap-service-overview"></a>Visão geral do serviço COM+ SOAP

Http revolutionized computer use, permitindo que as pessoas usem um navegador da Web para facilitar o acesso a informações em um servidor remoto em uma rede. Os serviços Web XML agora revolucionaram o desenvolvimento de aplicativos, permitindo que os aplicativos cliente chame facilmente métodos remotos em uma rede.

Geralmente, é útil para um aplicativo cliente chamar um método implementado em um servidor remoto. Às vezes, o método usa informações voláteis armazenadas no servidor remoto (por exemplo, um método que retorna o preço atual da ação correspondente a um determinado símbolo de tique). Em outros momentos, o desenvolvedor deseja a capacidade de atualizar a implementação de métodos sem precisar reimplantar todos os aplicativos que a usam.

Assim como as páginas da Web, os serviços Web XML são acessados por meio de um servidor Web, como o IIS, usando HTTP. No entanto, em vez de páginas da Web codificadas em HTML, esses pacotes HTTP contêm os parâmetros de entrada e saída de chamadas para um método implementado no servidor, codificado em SOAP.

Para usar um serviço Web XML, você precisa saber a URL em que o serviço é exposto e o nome do método que você deseja chamar e fornecer os parâmetros de entrada para o método . O padrão [SOAP 1.1](https://www.w3.org/TR/SOAP/) fornece o exemplo a seguir de um pacote HTTP que contém uma chamada remota para um serviço Web XML em , que retorna o preço atual da ação correspondente a um determinado símbolo de tique. https://www.stockquoteserver.com/StockQuote

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

Como ilustra o exemplo anterior, SOAP é uma instância XML que pode ser inserida em uma solicitação HTTP. Da mesma forma, o resultado é retornado como um pacote HTTP com uma carga SOAP, conforme mostrado no exemplo a seguir.

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

Embora seja útil ter alguma compreensão da infraestrutura que se baseia em serviços Web XML, o COM+ facilita a criação e o uso de serviços Web XML que, muitas vezes, você não precisa se aprofundar nesse nível.

Você pode expor os métodos nas interfaces padrão dos componentes COM configurados em qualquer aplicativo COM+ como um serviço Web XML. Nenhuma consideração especial de programação é necessária ao escrever os componentes, exceto que os métodos que você deseja expor devem estar na interface padrão e o componente deve ser configurado (no catálogo COM+ do servidor). Você não precisa escrever código para se comunicar por meio de um interface de rede ou para analisar SOAP. Para obter instruções detalhadas sobre como usar o serviço SOAP COM+ para criar um serviço Web XML, consulte [Criando serviços Web XML.](creating-xml-web-services.md)

Quando você expõe um aplicativo COM+ como um serviço Web XML, informações detalhadas sobre a sintaxe de todos os métodos disponíveis de um serviço Web XML são publicadas automaticamente, usando a linguagem WSDL. Essas informações são usadas por clientes que usam seu serviço Web XML.

O COM+ fornece duas maneiras de acessar e usar um serviço Web XML remoto, da seguinte maneira:

-   O modo WKO *(objeto* conhecido) pode ser usado para acessar qualquer serviço Web XML que publique sua sintaxe usando WSDL, mesmo que esse serviço Web XML não tenha sido criado usando COM+ ou até mesmo o Microsoft Windows.
-   O *modo DED* (objeto ativado pelo cliente) só pode ser usado para acessar serviços Web XML criados expondo aplicativos COM+. O modo UNIFORM aumenta o desempenho usando conexões persistentes, um recurso sem suporte do padrão SOAP atual.

Ambos os métodos permitem que os aplicativos cliente chamem os métodos de serviços Web XML remotamente de maneira simples, sem precisar escrever código para se comunicar por meio de um interface de rede ou analisar SOAP. Para obter detalhes sobre como acessar serviços Web XML em qualquer modo, consulte Acessando serviços [Web XML](accessing-xml-web-services-in-cao-mode.md) no modo XML e Acessando serviços Web XML no modo [WKO](accessing-xml-web-services-in-wko-mode.md).

> [!Note]  
> O COM+ dá suporte apenas à especificação SOAP-RPC, não à SOAP-Document especificação.

 

O COM+ torna o uso de serviços Web XML especialmente fácil, permitindo que você use aplicativos COM+ existentes como serviços Web XML no modo XML de maneira completamente transparente. Se [](exporting-a-soap-enabled-application.md) você exportar um aplicativo COM+ que foi exposto como um [](importing-a-soap-enabled-application.md) serviço Web XML do seu servidor, qualquer cliente que importar o aplicativo poderá usar de forma transparente o serviço Web XML do servidor sempre que o aplicativo importado for usado. Essa instalação facilita muito a conversão de aplicativos COM+ existentes em serviços Web XML e a implantação desses serviços em uma rede.

O uso de serviços Web XML tem várias vantagens exclusivas em relação a implementações alternativas de RPC (chamadas de procedimento remoto), incluindo o seguinte:

-   SOAP é uma verdadeira implementação de RPC de plataforma cruzada, o que aumenta a interoperabilidade.
-   Os serviços Web XML suportam métodos com parâmetros de entrada e saída.
-   Os serviços Web XML são executados por HTTP, o que geralmente pode impedir firewalls que podem bloquear outras implementações de RPC.
-   Quando um serviço Web XML é implementado usando COM+, o desenvolvedor não precisa escrever nenhum código especializado; essa é uma enorme vantagem sobre mecanismos RPC alternativos.

> [!Note]  
> Os serviços Web XML não são suportados por chamadas assíncronas ou transacionais de forma transparente. Use o [serviço Componentes Em Fila COM+](com--queued-components.md) quando precisar dessa funcionalidade.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Considerações sobre segurança do serviço SOAP COM+](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



