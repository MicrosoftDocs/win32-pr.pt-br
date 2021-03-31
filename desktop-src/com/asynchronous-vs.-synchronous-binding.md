---
title: Associação assíncrona e síncrona
description: Associação assíncrona e síncrona
ms.assetid: 9852df19-5ae4-4425-9ce0-cac160d68456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b022df239221f0a019b972067248225210e585
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641904"
---
# <a name="asynchronous-and-synchronous-binding"></a>Associação assíncrona e síncrona

O cliente pode verificar se o moniker é assíncrono chamando a função [**IsAsyncMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) . Se o cliente retornar o \_ sinalizador assíncrono BINDF, em vez de retornar um ponteiro de objeto ou um ponteiro de armazenamento das chamadas subsequentes para [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) ou [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject), o moniker retornará o \_ assíncrona do MK \_ no lugar do ponteiro do objeto e **nulo** no lugar do ponteiro de armazenamento. Em resposta, o cliente deve aguardar para receber o objeto ou armazenamento solicitado durante a implementação de [**IBindStatusCallback:: OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) e [**IBindStatusCallback:: OnObjectAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775063(v=vs.85)).

O objeto de retorno de chamada também recebe notificação de progresso por meio de [**IBindStatusCallback:: OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85)), notificação de disponibilidade de dados por meio de [**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))e várias outras notificações do moniker sobre o status da operação de associação.

Se o cliente não retornar o \_ sinalizador assíncrono BINDF da chamada do moniker para [**IBindStatusCallback:: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)), a operação de associação continuará de forma síncrona e o objeto ou armazenamento desejado será retornado das chamadas subsequentes para [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) ou [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage). Da mesma forma, se o cliente desejar uma operação síncrona e não quiser receber nenhuma notificação de progresso ou retornos de chamada, ele poderá solicitar que um moniker assíncrono se comporte de forma síncrona, não implementando [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)). Nesses casos, o moniker assíncrono se comportará como um moniker síncrono padrão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monikers assíncronos](asynchronous-monikers.md)
</dt> </dl>

 

 