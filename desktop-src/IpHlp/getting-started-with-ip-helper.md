---
description: Veja a seguir um guia passo a passo para a programação de introdução usando a API (interface de programação de aplicativo) auxiliar de IP. Ele foi projetado para fornecer uma compreensão das funções auxiliares de IP e estruturas de dados básicas e como elas funcionam juntas.
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: Introdução com auxiliar de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134ca2df12a7d2d2cbd2d0a64f1da07c8aeecd4980fea791bfc19ca018cd87be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014154"
---
# <a name="getting-started-with-ip-helper"></a>Introdução com auxiliar de IP

Veja a seguir um guia passo a passo para a programação de introdução usando a API (interface de programação de aplicativo) auxiliar de IP. Ele foi projetado para fornecer uma compreensão das funções auxiliares de IP e estruturas de dados básicas e como elas funcionam juntas.

O aplicativo usado para ilustração é um aplicativo auxiliar de IP muito básico. exemplos de código mais avançados estão incluídos nos exemplos incluídos no Microsoft Windows Software Development Kit (SDK).

A primeira etapa é a mesma para a maioria dos aplicativos auxiliares de IP.

-   [Criando um aplicativo auxiliar de IP básico](creating-a-basic-ip-helper-application.md)

As seções a seguir descrevem as etapas restantes para criar esse aplicativo auxiliar de IP básico.

-   [Recuperando informações usando GetNetworkParams](retrieving-information-using-getnetworkparams.md)
-   [Gerenciando adaptadores de rede usando o GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)
-   [Gerenciando interfaces usando o GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)
-   [Gerenciando endereços IP usando GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)
-   [Gerenciando concessões DHCP usando IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [Gerenciando endereços IP usando AddIPAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [Recuperando informações usando GetIpStatistics](retrieving-information-using-getipstatistics.md)
-   [Recuperando informações usando GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

O código-fonte completo para este exemplo de auxiliar de IP básico.

-   [Código-fonte completo do aplicativo auxiliar de IP](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a>Exemplos do auxiliar de IP avançado

vários exemplos mais avançados de auxiliares de IP estão incluídos no Microsoft Windows Software Development Kit (SDK). por padrão, o código-fonte de exemplo do auxiliar de IP é instalado pelo SDK do Windows liberado para o Windows 7 no seguinte diretório:

*C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ NetDs \\ IPHelp*

Os exemplos mais avançados listados abaixo são encontrados nos seguintes diretórios:

-   EnableRouter

    Esse diretório contém um exemplo que demonstra como usar as funções auxiliares de IP [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) e [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) para habilitar e desabilitar o encaminhamento de IPv4 no computador local.

-   iparp

    Esse diretório contém um programa de exemplo que demonstra como usar as funções auxiliares de IP para exibir e manipular entradas na tabela ARP IPv4 no computador local.

-   ipchange

    Esse diretório contém um programa de exemplo que demonstra como usar as funções auxiliares de IP para alterar programaticamente um endereço IP para um adaptador de rede específico em seu computador. Este programa também demonstra como recuperar informações de configuração de IP do adaptador de rede existentes.

-   IPConfig

    Esse diretório contém um programa de exemplo que demonstra como recuperar programaticamente as informações de configuração de IPv4 semelhantes ao utilitário IPCONFIG.EXE. Ele demonstra como usar as funções [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) e [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) . Observe que a função **GetAdaptersInfo** recupera apenas informações de IPv4.

-   IPRenew

    Esse diretório contém um programa de exemplo que demonstra como lançar e renovar programaticamente os endereços IPv4 obtidos por meio do DHCP. Este programa também demonstra como recuperar informações de configuração de adaptador de rede existentes.

-   IPRoute

    Esse diretório contém um programa de exemplo que demonstra como usar as funções auxiliares de IP para manipular a tabela de roteamento IPv4.

-   ipstat

    Esse diretório contém um programa de exemplo que demonstra como usar as funções auxiliares de IP para mostrar conexões IPv4 para um protocolo. Por padrão, as estatísticas são mostradas para IP, ICMP, TCP e UDP.

-   NetInfo

    esse diretório contém um programa de exemplo que demonstra como usar as novas APIs auxiliares de IP introduzidas no Windows Vista e versões posteriores para exibir/alterar informações de endereço e de interface para IPv4 e IPv6.

 

 



