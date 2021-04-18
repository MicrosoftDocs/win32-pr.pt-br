---
description: Os endereços IPv6 de link local e local são chamados de endereços no escopo.
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: Link IPv6-local e endereços locais do site
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80b8e201adf382b10dd31fe5607de903d6c588
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814014"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a>Link IPv6-local e endereços locais do site

Os endereços IPv6 de link local e local são chamados de endereços no escopo. A API do Windows Sockets (Winsock) dá suporte ao membro da **\_ \_ ID de escopo sin6** na estrutura [**SOCKADDR \_ In6**](sockaddr-2.md) para uso com endereços com escopo. Para endereços de link local IPv6 (FE80::/10 prefix), o membro de **\_ \_ ID de escopo sin6** na estrutura **SOCKADDR \_ In6** é o número da interface. Para endereços locais de site IPv6 (FEC0::/10 prefix), o membro de **\_ \_ ID de escopo sin6** na estrutura **SOCKADDR \_ In6** é um identificador de site.

Um exemplo de um endereço IPv6 de link local na interface \# 5 é o seguinte:

``` syntax
fe80::208:74ff:feda:625c%5
```

O comando a seguir está disponível no Windows XP com Service Pack 1 (SP1) e posterior para consultar e configurar o IPv6 em um computador local:

-   [Netsh.exe](netsh-exe.md)

As alterações de configuração feitas usando os comandos Netsh.exe são permanentes e não são perdidas quando o computador ou o protocolo IPv6 é reiniciado.

Antes do Windows XP com Service Pack 1 (SP1), a configuração e o gerenciamento de IPv6 usavam várias ferramentas de linha de comando mais antigas (Net.exe, Ipv6.exe e Ipsec6.exe) para configurar e gerenciar o IPv6. Usando essas ferramentas mais antigas, as alterações de IPv6 não são permanentes e são perdidas quando o computador ou o protocolo IPv6 foi reiniciado. Essas ferramentas de linha de comando mais antigas só têm suporte no Windows XP.

No Windows XP com SP1, o comando a seguir exibirá a lista de interfaces IPv6 em um computador local, incluindo o índice da interface, o nome da interface e várias outras propriedades da interface.

**netsh interface ipv6 show interface**

No Windows XP com SP1, o comando a seguir alterará o identificador de site associado a um índice de interface.

**netsh interface ipv6 set interface <InterfaceIndex or Name> SiteId = valor**

No Windows XP, o comando mais antigo a seguir também alterará o identificador de site associado a um endereço de site local para 3.

**IPv6 RTU FEC0::/10 3**

Se você estiver enviando ou se conectando a um endereço com escopo, o membro de **\_ \_ ID de escopo sin6** na estrutura [**\_ In6 SOCKADDR**](sockaddr-2.md) pode ser deixado não especificado (zero), o que representa um endereço de escopo ambíguo. Por exemplo, o endereço de link local a seguir é ambíguo:

``` syntax
fe80::10
```

Se você estiver ligando a um endereço de escopo, o membro **de \_ \_ ID de escopo sin6** na [**estrutura \_ In6 SOCKADDR**](sockaddr-2.md) deverá conter um valor diferente de zero que especifica um número de interface válido para um endereço de vínculo local ou um identificador de site para um endereço de site local.

## <a name="ambiguous-scoped-addresses"></a>Endereços com escopo ambíguo

Se você estiver enviando ou se conectando a um endereço com escopo e não tiver especificado o membro de **\_ \_ ID de escopo sin6** na estrutura [**\_ In6 SOCKADDR**](sockaddr-2.md) , o endereço com escopo será ambíguo. Para resolver isso, o protocolo IPv6 primeiro determina se você asboundu o soquete a um endereço de origem. Nesse caso, o endereço de origem associado resolve a ambiguidade fornecendo um número de interface ou identificador de site.

Se você estiver enviando ou se conectando a um endereço com escopo e não tiver especificado o membro de **\_ \_ ID de escopo sin6** nem associado a um endereço de origem, o protocolo IPv6 verificará a tabela de roteamento. Por exemplo, o comando a seguir exibirá a tabela de roteamento IPv6 em um computador local:

**netsh interface ipv6 show route**

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

Isso indica que os endereços de link local são tratados como on-link para a interface \# 13 e \# 14 por padrão.

A ambiguidade surge quando um computador local tem vários adaptadores de rede. Por exemplo, o comando **netsh** acima indica que há duas interfaces de rede (conexão de área local e conexão de rede sem fio). Quando um aplicativo especifica um endereço de destino local (FE80:: 10, por exemplo) sem uma ID de escopo, não fica claro qual adaptador usar para enviar o pacote. Somente um link-local unicast (FE80::/64) ou um endereço de destino de multicast de escopo de link (FF00::/8) pode ser prejudicado de não ter uma ID de escopo ao enviar um pacote.

## <a name="neighbor-discovery"></a>Descoberta de vizinhos

Se você não tiver especificado o membro de **\_ \_ ID de escopo sin6** na estrutura [**\_ In6 SOCKADDR**](sockaddr-2.md) , não tiver associado um endereço de origem e não tiver especificado uma rota para endereços de vínculo local, o protocolo IPv6 tentará a descoberta de vizinho para resolver o endereço de destino-local. Para um determinado pacote que está sendo enviado, uma interface é tentada. Essa primeira interface que é tentada é considerada a interface mais preferencial. Se a descoberta de vizinho não resolver o endereço de vínculo local em uma interface, o pacote a ser enviado será descartado e o sistema se lembrará de que o endereço de link local de destino não estará acessível nessa interface. No próximo pacote a ser enviado em todas as mesmas condições, uma interface diferente é tentada para a descoberta de vizinho. Esse processo continua em cada uma das interfaces em um computador local para cada novo pacote até que a descoberta de vizinho responda ao endereço local de destino ou todas as interfaces possíveis tenham sido tentadas e falharam. Cada vez que uma tentativa de resolver o vizinho falha, uma interface é eliminada para esse vizinho.

Se o endereço de link local de destino for resolvido, essa interface será usada para enviar o pacote atual. Essa interface também é usada para todos os pacotes de escopo ambíguos subseqüentes que são enviados para o mesmo endereço de destino de link local.

Se a descoberta de vizinhos falhar ao resolver o endereço de destino-local em todas as interfaces, o sistema tentará enviar o pacote na interface mais preferencial (a primeira interface tentada). A pilha de rede continua tentando resolver o endereço do link-local de destino na interface mais preferencial. Após um período de tempo após a falha da descoberta de vizinho em todas as interfaces, a pilha de rede reiniciará o processo novamente e tentará resolver o endereço do link-local de destino em todas as interfaces. Atualmente, esse intervalo de tempo quando a descoberta de vizinho é tentada novamente em todas as interfaces é de 60 segundos. No entanto, esse intervalo de tempo pode ser alterado em versões do Windows e não deve ser considerado por um aplicativo.

> [!Note]  
> Se um aplicativo associar o mesmo endereço de vínculo local a uma interface diferente depois que a descoberta de vizinho tiver resolvido o endereço de vínculo local, isso não substituirá a interface pelo endereço de destino de link local retornado pela descoberta de vizinho.

 

Para obter mais informações sobre a descoberta de vizinho para IP versão 6, consulte [RFC4861](https://tools.ietf.org/html/rfc4861) publicado pela IETF.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Prefixos de site IPv6](site-prefixes-2.md)
</dt> <dt>

[Ipv6.exe](ipv6-exe-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> <dt>

[Usando IPv6](using-ipv6-2.md)
</dt> </dl>

 

 



