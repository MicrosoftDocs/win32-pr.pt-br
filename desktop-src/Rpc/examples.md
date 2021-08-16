---
title: Exemplos (RPC)
description: Exemplos que demonstram conceitos de RPC (Chamada de Procedimento Remoto).
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- RPC de Chamada de Procedimento Remoto , exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e75dca3866e325a4f10eb446d209b834b62ff0407e7edd19f92ec70ac700df85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930045"
---
# <a name="examples-rpc"></a>Exemplos (RPC)

O SDK (Kit de Desenvolvimento de Software) da Plataforma inclui exemplos que demonstram uma variedade de conceitos de RPC (Chamada de Procedimento Remoto), da seguinte forma:

-   ASYNCRPC ilustra a estrutura de um aplicativo RPC que usa chamadas de procedimento remoto assíncrono. Ele também demonstra vários métodos de notificação da conclusão da chamada.
-   O CLUUID demonstra o uso do UUID client-object para permitir que um cliente selecione entre várias implementações de um procedimento remoto.
-   O diretório DATA contém quatro programas: o DUNION ilustra uniões discriminadas (não truncadas); INOUT demonstra [ \[ os parâmetros \] ](../midl/in.md)em , [ \[ \] ](../midl/out-idl.md) out; REPAS demonstra a [representação \_ como](/windows/desktop/Midl/represent-as) atributo; XMIT demonstra a [transmissão \_ como](/windows/desktop/Midl/transmit-as) atributo.
-   D LTDAPT demonstra um aplicativo cliente gerenciando sua conexão com o servidor por meio de pontos de extremidade dinâmicos.
-   O diretório FILEREP contém quatro exemplos que ilustram como os desenvolvedores podem escrever um serviço de replicação de arquivo simples, um serviço de replicação de arquivos de vários usuários, um serviço que dá suporte a recursos de segurança e um serviço usando pipes assíncronos RPC.
-   O diretório HANDLES contém três programas, AUTO, CXHNDL, USNIXF, que demonstram o manipular automaticamente [, \_ ](/windows/desktop/Midl/auto-handle)o alça de contexto e os \[ \_ \] handles genéricos (definidos pelo usuário), respectivamente.
-   HELLO é uma implementação de cliente/servidor de "Olá, mundo".
-   O diretório PICKLE contém dois programas: PICKLP demonstra a serialização do procedimento de dados; PICKLT demonstra a serialização de tipo de dados; ambos os programas usam os [ \[ atributos de \] codificação](../midl/encode.md) [ \[ e decodificar. \] ](../midl/decode.md)
-   PIPES demonstra o uso do construtor de tipo pipe.
-   RPCSVC demonstra a implementação de um serviço com RPC.
-   O STROUT demonstra como alocar memória em um servidor para um objeto bidimensional (uma matriz de ponteiros) e passá-la de volta para o cliente como um parâmetro \[ \] somente saída. Em seguida, o cliente libera a memória. Essa técnica permite que o stub chame o servidor sem saber com antecedência quantos dados serão retornados.

    Esse programa também permite que o usuário compile para UNICODE ou ANSI.

Todos os arquivos de origem e makefiles para esses programas estão localizados no SDK da Plataforma.

Para desenvolvimento de aplicativos RPC básicos e exemplos mais simples, consulte os [tópicos](tutorial.md) do Tutorial.

 

 
