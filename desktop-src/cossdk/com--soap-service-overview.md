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
# <a name="com-soap-service-overview"></a>Visão geral do serviço SOAP COM+

O HTTP revolucionou o uso do computador permitindo que as pessoas usem um navegador da Web para facilitar o acesso a informações em um servidor remoto em uma rede. Os serviços Web XML agora revolucionaram o desenvolvimento de aplicativos, permitindo que aplicativos cliente chamem facilmente métodos remotos em uma rede.

Geralmente, é útil que um aplicativo cliente possa chamar um método implementado em um servidor remoto. Às vezes, o método usa informações voláteis armazenadas no servidor remoto (por exemplo, um método que retorna o preço atual da bolsa correspondente a um determinado símbolo de marca). Em outras ocasiões, o desenvolvedor quer a capacidade de atualizar a implementação de métodos sem precisar reimplantar todos os aplicativos que o utilizam.

Assim como as páginas da Web, os serviços XML são acessados por meio de um servidor Web, como o IIS, usando HTTP. No entanto, em vez de páginas da Web codificadas em HTML, esses pacotes HTTP contêm os parâmetros de entrada e saída de chamadas para um método implementado no servidor, codificado em SOAP.

Para usar um serviço Web XML, você precisa saber a URL onde o serviço é exposto e o nome do método que você deseja chamar, e deve fornecer os parâmetros de entrada para o método. [O padrão SOAP 1,1](https://www.w3.org/TR/SOAP/) fornece o exemplo a seguir de um pacote http que contém uma chamada remota para um serviço Web XML em https://www.stockquoteserver.com/StockQuote , que retorna o preço atual da ação correspondente a um determinado símbolo de marca.

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

Como o exemplo anterior ilustra, SOAP é uma instância XML que pode ser inserida em uma solicitação HTTP. Da mesma forma, o resultado é retornado como um pacote HTTP com uma carga SOAP, conforme mostrado no exemplo a seguir.

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

Embora seja útil ter alguma compreensão da infraestrutura que se baseia em serviços Web XML, o COM+ facilita a criação e o uso de Web Services XML que, com frequência, você não precisará mais se aprofundar nesse nível.

Você pode expor os métodos nas interfaces padrão dos componentes COM configurados em qualquer aplicativo COM+ como um serviço Web XML. Nenhuma consideração especial de programação é necessária ao gravar os componentes, exceto que os métodos que você deseja expor devem estar na interface padrão e o componente deve ser configurado (no catálogo COM+ do seu servidor). Você não precisa escrever código para se comunicar por meio de uma interface de rede ou para analisar SOAP. Para obter instruções detalhadas sobre como usar o serviço SOAP COM+ para criar um serviço Web XML, consulte [criando XML Web Services](creating-xml-web-services.md).

Quando você expõe um aplicativo COM+ como um serviço Web XML, informações detalhadas sobre a sintaxe de todos os métodos disponíveis de um serviço Web XML são publicadas automaticamente, usando o WSDL (Web Services Description Language). Essas informações são usadas por clientes que usam o serviço Web XML.

O COM+ fornece duas maneiras de acessar e usar um serviço Web XML remoto, da seguinte maneira:

-   O modo WKO ( *well-known Object* ) pode ser usado para acessar qualquer serviço Web XML que publica sua sintaxe usando WSDL, mesmo se esse serviço Web XML não tiver sido criado usando com+ ou mesmo Microsoft Windows.
-   O modo Cao ( *objeto ativado pelo cliente* ) pode ser usado somente para acessar serviços Web XML criados pela exposição de aplicativos com+. O modo CAO aumenta o desempenho usando conexões persistentes, um recurso sem suporte do padrão SOAP atual.

Ambos os métodos permitem que aplicativos cliente chamem os métodos de serviços Web XML remotamente de maneira simples, sem precisar escrever código para se comunicar por meio de uma interface de rede ou analisar SOAP. Para obter detalhes sobre como acessar os serviços Web XML em ambos os modos, consulte [acessando serviços Web XML no modo Cao](accessing-xml-web-services-in-cao-mode.md) e [acessando Web Services XML no modo WKO](accessing-xml-web-services-in-wko-mode.md).

> [!Note]  
> O COM+ dá suporte apenas à especificação SOAP-RPC, não à especificação de SOAP-Document.

 

O COM+ torna o uso de serviços Web XML especialmente fácil, permitindo que você use aplicativos COM+ existentes como serviços Web XML no modo CAO de maneira totalmente transparente. Se você [Exportar](exporting-a-soap-enabled-application.md) um aplicativo com+ que foi exposto como um serviço Web XML do seu servidor, qualquer cliente que [importar](importing-a-soap-enabled-application.md) o aplicativo poderá usar de modo transparente o serviço Web XML do servidor sempre que o aplicativo importado for usado. Esse recurso torna a conversão de aplicativos COM+ existentes em XML Web Services e a implantação desses serviços em uma rede muito fácil.

O uso de Web Services XML tem várias vantagens exclusivas sobre implementações alternativas de RPC (chamadas de procedimento remoto), incluindo o seguinte:

-   SOAP é uma implementação de RPC de plataforma cruzada verdadeira, o que aumenta a interoperabilidade.
-   Os serviços Web XML dão suporte a métodos com parâmetros de entrada e saída.
-   Os serviços Web XML são executados sobre HTTP, o que normalmente pode penetrar firewalls que podem bloquear outras implementações RPC.
-   Quando um serviço Web XML é implementado usando COM+, o desenvolvedor não precisa escrever nenhum código especializado; Essa é uma enorme vantagem em relação aos mecanismos alternativos de RPC.

> [!Note]  
> Os serviços Web XML não oferecem suporte a chamadas assíncronas ou transacionais de forma transparente. Use o serviço de [componentes em fila com+](com--queued-components.md) quando você precisar dessa funcionalidade.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Considerações de segurança do serviço SOAP COM+](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



