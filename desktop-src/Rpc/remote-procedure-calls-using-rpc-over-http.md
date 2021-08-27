---
title: Chamadas de procedimentos remotos usando RPC sobre HTTP
description: Programas de navegador da Internet normalmente empregam o PROTOCOLO HTTP como o principal meio de navegação no World Wide Web.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- RPC de Chamada de Procedimento Remoto , tarefas, usando RPC/http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fedeb1700d798a616d3441b356f6f31867eed0399f412ed1f82923bcc4ac5f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101656"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a>Chamadas de procedimentos remotos usando RPC sobre HTTP

Programas de navegador da Internet normalmente empregam o PROTOCOLO HTTP como o principal meio de navegação no World Wide Web. O HTTP, portanto, vê uso extensivo na maioria dos computadores atualmente. A Microsoft estendeu os recursos do IIS (Servidor de Informações da Internet) para fornecer serviços de chamada de procedimento remoto usando HTTP.

A implementação RPC sobre HTTP da Microsoft (RPC sobre HTTP) permite que os clientes RPC se conectem com segurança e eficiência pela Internet a programas de servidor RPC e executem chamadas de procedimento remoto. Isso é feito com a ajuda de um intermediário conhecido como Proxy RPC sobre HTTP ou simplesmente o Proxy RPC.

O Proxy RPC é executado em um computador IIS. Ele aceita solicitações RPC provenientes da Internet, executa verificações de autenticação, validação e acesso nessas solicitações e, se a solicitação passar em todos os testes, o Proxy RPC encaminhará a solicitação para o servidor RPC que executa o processamento real. Com o RPC por HTTP, o cliente e o servidor RPC não se comunicam diretamente; em vez disso, eles usam o Proxy RPC como intermediário. Esse modelo foi escolhido por vários motivos. Para obter mais informações, consulte [RPC sobre Segurança HTTP.](rpc-over-http-security.md)

Esta seção fornece uma visão geral do RPC sobre HTTP nos seguintes tópicos:

-   [Usando HTTP como um transporte RPC](using-http-as-an-rpc-transport.md)
-   [RPC sobre Segurança HTTP](rpc-over-http-security.md)
-   [Requisitos do sistema e interoperabilidade para RPC por HTTP](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [Configurando computadores para RPC por HTTP](configuring-computers-for-rpc-over-http.md)
-   [RPC sobre implantação HTTP Recomendações](rpc-over-http-deployment-recommendations.md)

Para obter informações sobre cenários de RPC de alto volume sobre HTTP, consulte [Microsoft RPC Load Balancing](rpc-load-balancing.md).

 

 




