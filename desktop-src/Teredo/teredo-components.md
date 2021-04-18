---
title: Componentes do Teredo
ms.assetid: 95d83030-b1de-4f09-b9d0-f443d9672ca1
description: 'Saiba mais sobre: componentes do Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b4de66f38d5eb64b8321b6bb89e78fbb763e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789835"
---
# <a name="teredo-components"></a>Componentes do Teredo

A infraestrutura de [Teredo](about-teredo.md) consiste nos seguintes componentes:

## <a name="teredo-clients"></a>Clientes Teredo

Um cliente Teredo é um nó IPv6/IPv4 que dá suporte a uma interface de túnel Teredo por meio da qual os pacotes são encapsulados em outros clientes ou nós Teredo na Internet IPv6 (por meio de uma retransmissão Teredo). Um cliente Teredo se comunica com um servidor Teredo para obter um prefixo de endereço do qual um endereço IPv6 baseado em Teredo está configurado ou usado para facilitar a comunicação com outros clientes ou hosts Teredo na Internet IPv6.

O Windows XP com Service Pack 1 (SP1) com o Advanced Networking Pack, o Windows XP com Service Pack 2 (SP2), o Windows Server 2003 com Service Pack 1 (SP1), o Windows Server 2003 com Service Pack 2 (SP2), o Windows Vista e o Windows Server 2008 incluem o cliente Teredo.

## <a name="teredo-servers"></a>Servidores Teredo

Um servidor Teredo é um nó IPv6/IPv4 que está conectado à Internet IPv4 e à Internet IPv6 e dá suporte a uma interface de túnel Teredo sobre a qual os pacotes são recebidos. A função geral do servidor Teredo é auxiliar na configuração de endereço de clientes Teredo e facilitar a comunicação inicial entre clientes Teredo e outros clientes Teredo ou entre clientes Teredo e hosts somente IPv6. O servidor Teredo escuta a porta UDP 3544 para o tráfego Teredo.

Ao contrário do cliente, o servidor Teredo não está incluído nas plataformas operacionais da Microsoft. Para facilitar a comunicação entre computadores cliente do Teredo baseados no Windows, a Microsoft implantou servidores Teredo na Internet IPv4.

## <a name="teredo-relays"></a>Retransmissões Teredo

Uma retransmissão Teredo é um roteador IPv6/IPv4 que pode encaminhar pacotes entre clientes Teredo na Internet IPv4 (usando uma interface de túnel Teredo) e hosts somente IPv6. Em alguns casos, a retransmissão Teredo interage com um servidor Teredo para facilitar a comunicação inicial entre clientes Teredo e hosts somente IPv6. A retransmissão Teredo escuta na porta UDP 3544 para o tráfego Teredo.

Como o servidor Teredo, as plataformas operacionais da Microsoft não incluem a funcionalidade de retransmissão Teredo. Atualmente, a Microsoft não planeja implantar retransmissões Teredo na Internet IPv4. As retransmissões Teredo não são necessárias para se comunicar com retransmissões específicas do host Teredo.

## <a name="teredo-host-specific-relays"></a>Retransmissões de Host-Specific Teredo

A comunicação entre clientes Teredo e hosts IPv6 configurados com um endereço global deve passar por uma retransmissão Teredo. Isso é necessário para hosts somente IPv6 conectados à Internet IPv6. No entanto, quando o host IPv6 é compatível com IPv6 e IPv4 e está conectado à Internet IPv4 e à Internet IPv6, a comunicação deve ocorrer entre o cliente Teredo e o host IPv6 pela Internet IPv4, em vez de ter que atravessar a Internet IPv6 e passar por uma retransmissão Teredo.

Uma retransmissão específica do host Teredo é um nó IPv6/IPv4 que tem uma interface e conectividade com a Internet IPv4 e a Internet IPv6 e pode se comunicar diretamente com clientes Teredo pela Internet IPv4, sem a necessidade de uma retransmissão Teredo intermediária. A conectividade com a Internet IPv4 pode ser por meio de um endereço IPv4 público ou por meio de um endereço IPv4 privado e de um NAT vizinho. A conectividade com a Internet IPv6 pode ser por meio de uma conexão direta com a Internet IPv6 ou por meio de uma tecnologia de transição IPv6, como o 6to4, em que os pacotes IPv6 são encapsulados na Internet IPv4. A retransmissão específica do host Teredo escuta na porta UDP 3544 para o tráfego Teredo.

O Windows XP com SP1 com o Advanced Networking Pack, o Windows XP com SP2, o Windows Server 2003 com SP1, o Windows Server 2003 com SP2, o Windows Vista e o Windows Server 2008 incluem a funcionalidade de retransmissão específica do host Teredo, que será habilitada automaticamente se o computador tiver um endereço global atribuído. Um endereço global é atribuído em uma mensagem de anúncio de roteador recebida de um roteador IPv6 nativo, um roteador ISATAP ou um roteador 6to4. Se o computador não tiver um endereço global, a funcionalidade do cliente Teredo estará habilitada.

A retransmissão específica do host Teredo permite que os clientes Teredo se comuniquem com eficiência com hosts 6to4, hosts IPv6 com um prefixo global não 6to4 ou hosts ISATAP ou 6over4 em organizações que usam um prefixo global para seus endereços, desde que ambos os hosts estejam usando uma versão do Windows que ofereça suporte a Teredo.

 

 




