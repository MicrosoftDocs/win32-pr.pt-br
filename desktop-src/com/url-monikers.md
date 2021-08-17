---
title: URL Monikers
description: A arquitetura de moniker OLE fornece um modelo de programação conveniente para trabalhar com URLs.
ms.assetid: 8e0e2bad-9275-4b96-a96b-35d9c933ae31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92e952e2d9bdd8ae70108e34845a3e920228b1b68f1db061977dff36e942254
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129478"
---
# <a name="url-monikers"></a>URL Monikers

A arquitetura de moniker OLE fornece um modelo de programação conveniente para trabalhar com URLs. A arquitetura de moniker dá suporte à análise de nome extensível e completa por meio da função [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname) e das interfaces [**IParseDisplayName**](/windows/desktop/api/OleIdl/nn-oleidl-iparsedisplayname) e [**IMoniker,**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) bem como nomes imprimíveis por meio do método [**IMoniker::GetDisplayName.**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) A interface **IMoniker** é a maneira como você realmente usa URLs encontradas e a criação de componentes que se ajustam à arquitetura de moniker é a maneira de realmente estender namespaces de URL na prática.

Uma classe de moniker fornecida pelo sistema, o moniker de URL, fornece uma estrutura para criar e usar determinadas URLs. Como as URLs frequentemente veem recursos em redes de alta latência, o moniker de URL dá suporte a associação assíncrona e síncrona. Atualmente, o moniker de URL não dá suporte ao [armazenamento assíncrono](/windows/desktop/Stg/asynchronous-storage).

O diagrama a seguir mostra os componentes envolvidos no uso de monikers de URL. Todos esses componentes devem ser familiares. (Consulte [Monikers assíncronos](asynchronous-monikers.md).)

![Diagrama que mostra os componentes envolvidos no uso de monikers U R L.](images/bb10975a-9cb5-418e-872e-1e1add0b58ed.png)

Como todos os clientes moniker, um usuário de Monikers de URL normalmente cria e mantém uma referência ao moniker, bem como ao contexto de associação a ser usado durante a associação ([**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) ou [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)). Para dar suporte à associação assíncrona, o cliente pode implementar um objeto bind-status-callback, que implementa a interface [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) e registrá-lo com o contexto de associação usando a [**função RegisterBindStatusCallback.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) Esse objeto receberá a interface [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) do transporte durante chamadas para [**IBindStatusCallback::OnStartBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)).

O Moniker de URL identifica o protocolo que está sendo usado pela análise do prefixo de URL e recupera a interface [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) da camada de transporte. O cliente usa **IBinding para dar** suporte à pausa, cancelamento e priorização da operação de associação. O objeto de retorno de chamada também recebe notificação de progresso por [**meio de IBindStatusCallback::OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85)), notificação de disponibilidade de dados por meio [**de IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))e várias outras notificações de camada de transporte sobre o status da associação. O moniker de URL ou camadas de transporte específicas também pode solicitar informações estendidas do cliente por meio de **IBindStatusCallback::QueryInterface**, permitindo que o cliente forneça informações específicas do protocolo que afetarão a operação de vinculação.

Para obter mais informações, consulte estes tópicos:

-   [Sincronização de retorno de chamada](callback-synchronization.md)
-   [Negociação de tipo de mídia](media-type-negotiation.md)
-   [Funções de Moniker de URL](url-moniker-api-functions.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monikers assíncronos](asynchronous-monikers.md)
</dt> <dt>

[Sobre monikers de URL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775149(v=vs.85))
</dt> </dl>

 

 