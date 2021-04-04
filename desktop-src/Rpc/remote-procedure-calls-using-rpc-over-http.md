---
title: Chamadas de procedimentos remotos usando RPC sobre HTTP
description: Os programas de navegador da Internet normalmente empregam o protocolo HTTP como o principal meio de procurar o World Wide Web.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- RPC de chamada de procedimento remoto, tarefas, usando RPC/http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c84551500af712b1126d8f9a65cb3d02eba8c9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915867"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a>Chamadas de procedimentos remotos usando RPC sobre HTTP

Os programas de navegador da Internet normalmente empregam o protocolo HTTP como o principal meio de procurar o World Wide Web. O HTTP, portanto, vê uso extensivo na maioria dos computadores atualmente. A Microsoft ampliou os recursos de seu IIS (servidor de informações da Internet) para fornecer serviços de chamada de procedimento remoto usando HTTP.

A implementação RPC via http da Microsoft (RPC sobre HTTP) permite que clientes RPC se conectem com segurança e eficiência pela Internet a programas de servidor RPC e executem chamadas de procedimento remoto. Isso é feito com a ajuda de um intermediário conhecido como proxy RPC sobre HTTP ou simplesmente o proxy RPC.

O proxy RPC é executado em um computador IIS. Ele aceita solicitações RPC provenientes da Internet, realiza autenticação, validação e verificações de acesso nessas solicitações e, se a solicitação passar em todos os testes, o proxy RPC encaminha a solicitação para o servidor RPC que executa o processamento real. Com RPC sobre HTTP, o cliente RPC e o servidor não se comunicam diretamente; em vez disso, eles usam o proxy RPC como intermediário. Esse modelo foi escolhido por muitos motivos. Para obter mais informações, consulte [RPC sobre segurança http](rpc-over-http-security.md).

Esta seção fornece uma visão geral do RPC sobre HTTP nos seguintes tópicos:

-   [Usando HTTP como um transporte RPC](using-http-as-an-rpc-transport.md)
-   [Segurança de RPC sobre HTTP](rpc-over-http-security.md)
-   [Requisitos do sistema e interoperabilidade para RPC sobre HTTP](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [Configurando computadores para RPC sobre HTTP](configuring-computers-for-rpc-over-http.md)
-   [Recomendações de implantação de RPC sobre HTTP](rpc-over-http-deployment-recommendations.md)

Para obter informações sobre cenários de RPC sobre HTTP em grande volume, consulte [balanceamento de carga do Microsoft RPC](rpc-load-balancing.md).

 

 




