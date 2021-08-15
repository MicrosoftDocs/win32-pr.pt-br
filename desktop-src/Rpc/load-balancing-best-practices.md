---
title: Práticas recomendadas de balanceamento de carga
description: Práticas recomendadas de balanceamento de carga
ms.assetid: 260cf8dd-13b8-4b46-93a6-5333e794c0d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fe4af9dffe758c89d1a494d4cc2597e057c563ca8c85db87d789ae91b89698
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928591"
---
# <a name="load-balancing-best-practices"></a>Práticas recomendadas de balanceamento de carga

Várias práticas recomendadas devem ser seguidas ao configurar e configurar o balanceamento de carga RPC.

Primeiro, a segurança deve ser definida em chamadas de LBS de entrada e saída. Isso significa que as duas chaves opcionais do registro [NoSecurity](configuring-load-balancing.md) não devem estar presentes ou devem ser definidas como zero.

Segundo, a atenção deve ser paga à solução de balanceamento de carga de front-end usada em conjunto com a solução de balanceamento de carga RPC. Por exemplo, se o balanceador de carga de front-end usar o balanceamento de carga de round robin simples, um número ímpar de servidores deverá existir no farm de servidores. Isso é para atenuar a possibilidade de todas as conexões serem encaminhadas e, portanto, atendidas pelo mesmo servidor ou servidores.

Por segurança, normalmente é desejável ter um controle de firewall de acesso a servidores proxy RPC. Se uma solução de firewall baseada em porta for empregada, os pontos de extremidade RPC deverão ser estáticos para limitar o número de portas abertas no firewall. no Windows Server 2008 e versões posteriores do Windows, o RPC fornece um mecanismo para atribuir uma porta estática a pontos de extremidade dinâmicos. Isso é obtido por meio dos comandos RPC netsh firewall. Um conjunto de comandos de exemplo para definir a interface lb para a porta estática de 3010 é:

``` syntax
netsh rpc filter add rule layer=ep_add actiontype=permit

netsh rpc filter add condition field=process_with_if_uuid matchtype=equal data=
3357951c-a1d1-47db-a278-ab945d063d03

netsh rpc filter add condition field=protocol matchtype=equal data=ncacn_ip_tcp

netsh rpc filter add condition field=ep_value matchtype=equal data=w3010

netsh rpc filter add filter
```

O comando RPC netsh pode ser usado para definir um ponto de extremidade estático para qualquer interface dinâmica ou estática. Isso é útil ao restringir o acesso a um computador que executa uma solução de firewall baseada em porta. se a solução de firewall Windows for usada, a interface RPC poderá ser bloqueada ou habilitada sem a necessidade de atribuí-la a uma porta específica. Para obter mais informações, consulte a [referência de comando RPC netsh firewall](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).

 

 