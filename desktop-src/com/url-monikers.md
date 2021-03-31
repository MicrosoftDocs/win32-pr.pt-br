---
title: Identificadores de URL
description: A arquitetura de moniker do OLE fornece um modelo de programação conveniente para trabalhar com URLs.
ms.assetid: 8e0e2bad-9275-4b96-a96b-35d9c933ae31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2a63f63d14dfe51c0b8c5c3727637e12a51356
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104172387"
---
# <a name="url-monikers"></a>Identificadores de URL

A arquitetura de moniker do OLE fornece um modelo de programação conveniente para trabalhar com URLs. A arquitetura do moniker dá suporte à análise de nome extensível e completo por meio da função [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname) e das interfaces [**IParseDisplayName**](/windows/desktop/api/OleIdl/nn-oleidl-iparsedisplayname) e [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) , bem como nomes imprimíveis por meio do método [**IMoniker:: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) . A interface **IMoniker** é a maneira como você realmente usa URLs que você encontra e a criação de componentes que se enquadram na arquitetura do moniker é a maneira de realmente estender os namespaces de URL na prática.

Uma classe de moniker fornecida pelo sistema, o moniker da URL, fornece uma estrutura para a criação e o uso de determinadas URLs. Como as URLs frequentemente veem recursos em redes de alta latência, o moniker de URL dá suporte à associação assíncrona e síncrona. O moniker da URL atualmente não dá suporte ao [armazenamento assíncrono](/windows/desktop/Stg/asynchronous-storage).

O diagrama a seguir mostra os componentes envolvidos no uso de identificadores de URL. Todos esses componentes devem ser familiares. (Consulte [monikers assíncronos](asynchronous-monikers.md).)

![Diagrama que mostra os componentes envolvidos no uso de monikers do U R L.](images/bb10975a-9cb5-418e-872e-1e1add0b58ed.png)

Como todos os clientes de moniker, um usuário de moniker de identificadores de URL normalmente cria e mantém uma referência ao moniker, bem como ao contexto de associação a ser usado durante a associação ([**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) ou [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)). Para dar suporte à vinculação assíncrona, o cliente pode implementar um objeto BIND-status-retorno de chamada, que implementa a interface [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) e registrá-lo com o contexto de associação usando a função [**RegisterBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) . Esse objeto receberá a interface [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) do transporte durante chamadas para [**IBindStatusCallback:: OnStart**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)).

O moniker da URL identifica o protocolo que está sendo usado pela análise do prefixo da URL e, em seguida, recupera a interface [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) da camada de transporte. O cliente usa **IBinding** para dar suporte à pausa, cancelamento e priorização da operação de associação. O objeto de retorno de chamada também recebe notificação de progresso por meio de [**IBindStatusCallback:: OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85)), notificação de disponibilidade de dados por meio de [**IBindStatusCallback:: OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))e várias outras notificações de camada de transporte sobre o status da associação. O moniker de URL ou as camadas de transporte específicas também podem solicitar informações estendidas do cliente por meio de **IBindStatusCallback:: QueryInterface**, permitindo que o cliente forneça informações específicas de protocolo que afetarão a operação de associação.

Para mais informações, consulte os seguintes tópicos:

-   [Sincronização de retorno de chamada](callback-synchronization.md)
-   [Negociação de tipo de mídia](media-type-negotiation.md)
-   [Funções de moniker de URL](url-moniker-api-functions.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monikers assíncronos](asynchronous-monikers.md)
</dt> <dt>

[Sobre monikers de URL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775149(v=vs.85))
</dt> </dl>

 

 