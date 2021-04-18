---
title: Serviços (guia do desenvolvedor do Windows 7)
description: O Windows 7 fornece uma plataforma poderosa, altamente extensível e gerenciável para a criação e a integração dos serviços Web e aplicativos do futuro. O Windows 7 oferece APIs de código gerenciado e APIs nativas para a criação e a execução de serviços Web.
ms.assetid: 6a027e0c-28a0-41cf-b96f-ed988c64c92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aab84cbb522f21b9a09a85d80ef25bf1c858baf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105796397"
---
# <a name="services-windows-7-developer-guide"></a>Serviços (guia do desenvolvedor do Windows 7)

O Windows 7 fornece uma plataforma poderosa, altamente extensível e gerenciável para a criação e a integração dos serviços Web e aplicativos do futuro.

O Windows 7 oferece APIs de código gerenciado e APIs nativas para a criação e a execução de serviços Web. Uma variedade de novos recursos se baseia em uma nova camada de extensibilidade que permite aos desenvolvedores estender todas as APIs, em código nativo ou dentro da estrutura de Microsoft .NET.

O Windows 7 também permite que os desenvolvedores tirem proveito dos melhores recursos de cache e pesquisa. Com esses aprimoramentos, os desenvolvedores podem recuperar dados mais rapidamente e reduzir o uso da largura de banda da rede.

## <a name="windows-web-services"></a>Serviços Web do Windows

Com os [Serviços Web do Windows](/windows/desktop/wsw/portal), você pode criar aplicativos que se comunicam facilmente com um computador local ou com um serviço Web remoto. O Windows Web Services é uma implementação de código nativo do SOAP e fornece comunicação de rede principal, dando suporte a um amplo conjunto de protocolos de família de serviços Web (*WS*). Os serviços Web do Windows são um ponto a [Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) (*WCF*, serviços da Web de código gerenciado) e fornece um subconjunto de alto desempenho da funcionalidade do *WCF* . Os serviços Web do Windows oferecem os seguintes benefícios:

-   A capacidade de criar serviços da Web de código nativo em C/C++ no cliente e servidor Windows.
-   Ampla integração com serviços de [Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) .
-   A capacidade de criar serviços Web com tempo de inicialização mínimo.
-   A capacidade de criar serviços com base na família básica *WS* de protocolos e padrões *W3C* .
-   A capacidade de usar serviços Web em ambientes com restrição de recursos.

Para obter mais informações, consulte [API de serviços Web do Windows](../wsw/portal.md) e [implementar serviços Web com a API de serviços Web do Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/web/WWSAPI).

## <a name="distributed-routing-table"></a>Tabela de roteamento distribuído

O Windows 7 facilita a compilação de aplicativos ponto a ponto sofisticados, como sistemas de arquivos distribuídos e redes de distribuição de conteúdo com a [tabela de roteamento distribuído](/windows/desktop/P2PSdk/distributed-routing-table-api-reference). A tabela de roteamento distribuído fornece um mecanismo seguro e escalonável para publicar e procurar chaves em um sistema ponto a ponto. Ele pode ser usado para criar tabelas de hash distribuídas e construir topologias para sobreposição de redes. (Consulte [API de tabela de roteamento distribuído](../p2psdk/distributed-routing-table-api.md).)

## <a name="windows-branchcache"></a>**Windows BranchCache**

O Windows 7 melhora a capacidade de resposta do aplicativo entre servidores centrais e computadores do escritório de filial. Nas redes atuais, a comunicação entre servidores centrais e filiais geralmente está congestionada, o que leva a um desempenho mais lento para aplicativos na filial. Com o Windows BranchCache, os clientes podem recuperar dados de outros clientes em seu próprio Branch que já baixaram os dados, em vez de precisar recuperar os dados em servidores remotos. Como resultado, o tráfego de link de WAN (rede de longa distância) diminui e a capacidade de resposta do aplicativo melhora. O cache mantém uma cópia de todo o conteúdo que os clientes na ramificação solicitaram e garante que somente os clientes autorizados pelo servidor de conteúdo possam acessar os dados solicitados, preservando a criptografia de ponta a ponta dos dados.

O Windows BranchCache já está integrado com HTTP e SMB (bloco de mensagens de servidor). Se um aplicativo usar o WindowsAPIs para qualquer um desses protocolos, o Windows BranchCache poderá ajudar a aumentar o desempenho desse aplicativo no Windows 7 sem fazer nenhuma alteração nele.

Se seu aplicativo recupera os mesmos dados várias vezes de um servidor em um link WAN e não é otimizado automaticamente usando o Windows 7, é fácil usar o BranchCacheAPIs do Windows para otimizar seu aplicativo para trabalhar mais rapidamente no Windows 7 e atender aos usuários da sua filial.

Esses novos recursos ajudam a reduzir o tráfego e a latência da WAN, garantindo a conformidade com as obrigações de segurança. (Consulte [distribuição de pares](../p2psdk/peer-distribution.md).)

 

 
