---
title: Exemplos (RPC)
description: Exemplos que demonstram conceitos de RPC (chamada de procedimento remoto).
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- RPC de chamada de procedimento remoto, exemplos
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

O SDK (Software Development Kit) da plataforma inclui exemplos que demonstram uma variedade de conceitos de RPC (chamada de procedimento remoto), da seguinte maneira:

-   ASYNCRPC ilustra a estrutura de um aplicativo RPC que usa chamadas de procedimento remoto assíncronas. Ele também demonstra vários métodos de notificação da conclusão da chamada.
-   CLUUID demonstra o uso do UUID de objeto de cliente para permitir que um cliente selecione várias implementações de um procedimento remoto.
-   O diretório de dados contém quatro programas: DUNION ilustra uniões discriminadas (não encapsuladas); O Inout demonstra os parâmetros [ \[ de \] ](../midl/in.md) [ \[ saída \] ](../midl/out-idl.md) ; REPAS demonstra a [representação \_ como](/windows/desktop/Midl/represent-as) atributo; TRANSMISSÃO demonstra o atributo [transmitir \_ como](/windows/desktop/Midl/transmit-as) .
-   DYNEPT demonstra um aplicativo cliente Gerenciando sua conexão com o servidor por meio de pontos de extremidade dinâmicos.
-   O diretório FILEREP contém quatro exemplos que ilustram como os desenvolvedores podem escrever um serviço de replicação de arquivo simples, um serviço de replicação de arquivo multiusuário, um serviço que dá suporte a recursos de segurança e um serviço usando pipes assíncronos RPC.
-   O diretório HANDLES contém três programas, AUTO, CXHNDL, USRDEF, que demonstram [ \_ identificadores automáticos](/windows/desktop/Midl/auto-handle), \[ \_ identificadores de contexto \] e identificadores genéricos (definidos pelo usuário), respectivamente.
-   Olá é uma implementação de cliente/servidor de "Olá, mundo".
-   O diretório PICKLE contém dois programas: PICKLP demonstra a serialização de procedimento de dados; PICKLT demonstra a serialização de tipo de dados; ambos os programas usam os atributos de [ \[ codificação \] ](../midl/encode.md) e [ \[ decodificação \] ](../midl/decode.md) .
-   Pipes demonstra o uso do construtor de tipo de pipe.
-   RPCSVC demonstra a implementação de um serviço com RPC.
-   STROUT demonstra como alocar memória em um servidor para um objeto bidimensional (uma matriz de ponteiros) e passá-lo de volta para o cliente como um \[ \] parâmetro somente out. Em seguida, o cliente libera a memória. Essa técnica permite que o stub chame o servidor sem saber com antecedência a quantidade de dados que será retornada.

    Esse programa também permite que o usuário compile para UNICODE ou ANSI.

Todos os arquivos de origem e os makefiles para esses programas estão localizados no SDK da plataforma.

Para o desenvolvimento de aplicativos RPC básico e exemplos mais simples, consulte os tópicos do [tutorial](tutorial.md) .

 

 
