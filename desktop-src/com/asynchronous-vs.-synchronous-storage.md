---
title: Armazenamento assíncrono e síncrono
description: Armazenamento assíncrono e síncrono
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884b8613bebf8ef401f76e4761f48fa0ddd831c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104499168"
---
# <a name="asynchronous-and-synchronous-storage"></a>Armazenamento assíncrono e síncrono

Os monikers assíncronos também podem retornar um objeto de [armazenamento assíncrono](/windows/desktop/Stg/asynchronous-storage) na notificação [**IBindStatusCallback:: OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) . Esse objeto de armazenamento pode permitir o acesso a alguns dos dados persistentes do objeto enquanto a associação ainda está em andamento. Um cliente pode escolher entre dois modos para o armazenamento: bloqueio e não bloqueio.

No modo de bloqueio, que é compatível com as implementações atuais de objetos de armazenamento, se os dados estiverem indisponíveis, a chamada será bloqueada até que os dados cheguem. No modo de não bloqueio, em vez de bloquear a chamada, o objeto de armazenamento retorna um novo erro E \_ pendente quando os dados não estão disponíveis. Um cliente que reconhece a associação assíncrona e o armazenamento observa esse erro e aguarda outras notificações ([**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) para repetir a operação. Um cliente pode escolher entre um armazenamento síncrono (bloqueio) e assíncrono (não bloqueado) escolhendo se deseja definir o \_ sinalizador BINDF ASYNCSTORAGE no valor *grfBINDF* retornado para [**IBindStatusCallback:: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monikers assíncronos](asynchronous-monikers.md)
</dt> </dl>

 

 