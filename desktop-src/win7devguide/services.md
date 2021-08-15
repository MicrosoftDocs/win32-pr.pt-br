---
title: serviços (guia do desenvolvedor do Windows 7)
description: o Windows 7 fornece uma plataforma poderosa, altamente extensível e gerenciável para a criação e a integração dos serviços web e aplicativos do futuro. o Windows 7 oferece apis de código gerenciado e apis nativas para a criação e a execução de serviços web.
ms.assetid: 6a027e0c-28a0-41cf-b96f-ed988c64c92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42fe2a59a69efe7fb34bb4a09c58b2ee03f00ac8b8129c36b1ef5f0f61971c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118203859"
---
# <a name="services-windows-7-developer-guide"></a>serviços (guia do desenvolvedor do Windows 7)

o Windows 7 fornece uma plataforma poderosa, altamente extensível e gerenciável para a criação e a integração dos serviços web e aplicativos do futuro.

o Windows 7 oferece apis de código gerenciado e apis nativas para a criação e a execução de serviços web. Uma variedade de novos recursos se baseia em uma nova camada de extensibilidade que permite aos desenvolvedores estender todas as APIs, em código nativo ou no Microsoft .NET Framework.

o Windows 7 também permite que os desenvolvedores tirem proveito dos melhores recursos de cache e pesquisa. Com esses aprimoramentos, os desenvolvedores podem recuperar dados mais rapidamente e reduzir o uso da largura de banda da rede.

## <a name="windows-web-services"></a>Windows Serviços Web

com [Windows Web Services](/windows/desktop/wsw/portal), você pode criar aplicativos que se comunicam facilmente com um computador local ou com um serviço Web remoto. Windows Os serviços Web são uma implementação de código nativo do SOAP e fornecem comunicação de rede principal, dando suporte a um amplo conjunto de protocolos de família de serviços Web (*WS*). Windows os serviços web são um ponto a [Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) (*WCF*, serviços da web de código gerenciado) e fornece um subconjunto de alto desempenho da funcionalidade do *WCF* . Windows Os serviços Web oferecem os seguintes benefícios:

-   a capacidade de criar serviços da web de código nativo em C/C++ em Windows cliente e servidor.
-   ampla integração com serviços de [Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) .
-   A capacidade de criar serviços Web com tempo de inicialização mínimo.
-   A capacidade de criar serviços com base na família básica *WS* de protocolos e padrões *W3C* .
-   A capacidade de usar serviços Web em ambientes com restrição de recursos.

para obter mais informações, consulte [Windows api de serviços web](../wsw/portal.md) e [implementar serviços web com a API de serviços web do Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/web/WWSAPI).

## <a name="distributed-routing-table"></a>Tabela de roteamento distribuído

o Windows 7 facilita a compilação de aplicativos ponto a ponto sofisticados, como sistemas de arquivos distribuídos e redes de distribuição de conteúdo com a [tabela de roteamento distribuído](/windows/desktop/P2PSdk/distributed-routing-table-api-reference). A tabela de roteamento distribuído fornece um mecanismo seguro e escalonável para publicar e procurar chaves em um sistema ponto a ponto. Ele pode ser usado para criar tabelas de hash distribuídas e construir topologias para sobreposição de redes. (Consulte [API de tabela de roteamento distribuído](../p2psdk/distributed-routing-table-api.md).)

## <a name="windows-branchcache"></a>**Windows BranchCache**

o Windows 7 melhora a capacidade de resposta do aplicativo entre servidores centrais e computadores do escritório da filial. Nas redes atuais, a comunicação entre servidores centrais e filiais geralmente está congestionada, o que leva a um desempenho mais lento para aplicativos na filial. com o Windows BranchCache, os clientes podem recuperar dados de outros clientes em seu próprio branch que já baixaram os dados, em vez de precisar recuperar os dados em servidores remotos. Como resultado, o tráfego de link de WAN (rede de longa distância) diminui e a capacidade de resposta do aplicativo melhora. O cache mantém uma cópia de todo o conteúdo que os clientes na ramificação solicitaram e garante que somente os clientes autorizados pelo servidor de conteúdo possam acessar os dados solicitados, preservando a criptografia de ponta a ponta dos dados.

Windows O BranchCache já está integrado com HTTP e SMB (bloco de mensagens de servidor). se um aplicativo usar o WindowsAPIs para qualquer um desses protocolos, Windows BranchCache poderá ajudar a aumentar o desempenho desse aplicativo no Windows 7 sem fazer nenhuma alteração nele.

se seu aplicativo recupera os mesmos dados várias vezes de um servidor em um link de WAN e não é otimizado automaticamente usando o Windows 7, é fácil usar o Windows BranchCacheAPIs para otimizar seu aplicativo para trabalhar mais rapidamente no Windows 7 e atender aos usuários da sua filial.

Esses novos recursos ajudam a reduzir o tráfego e a latência da WAN, garantindo a conformidade com as obrigações de segurança. (Consulte [distribuição de pares](../p2psdk/peer-distribution.md).)

 

 
