---
title: Armazenamento síncronos e assíncronos
description: Armazenamento síncronos e assíncronos
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5662f5d9291de19fb39f044731ed72fd1db2cb04fe29d76eb785981ddeb8a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071086"
---
# <a name="asynchronous-and-synchronous-storage"></a>Armazenamento síncronos e assíncronos

os monikers assíncronos também podem retornar um objeto [Armazenamento assíncrono](/windows/desktop/Stg/asynchronous-storage) na notificação [**IBindStatusCallback:: OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) . Esse objeto de armazenamento pode permitir o acesso a alguns dos dados persistentes do objeto enquanto a associação ainda está em andamento. Um cliente pode escolher entre dois modos para o armazenamento: bloqueio e não bloqueio.

No modo de bloqueio, que é compatível com as implementações atuais de objetos de armazenamento, se os dados estiverem indisponíveis, a chamada será bloqueada até que os dados cheguem. No modo de não bloqueio, em vez de bloquear a chamada, o objeto de armazenamento retorna um novo erro E \_ pendente quando os dados não estão disponíveis. Um cliente que reconhece a associação assíncrona e o armazenamento observa esse erro e aguarda outras notificações ([**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) para repetir a operação. Um cliente pode escolher entre um armazenamento síncrono (bloqueio) e assíncrono (não bloqueado) escolhendo se deseja definir o \_ sinalizador BINDF ASYNCSTORAGE no valor *grfBINDF* retornado para [**IBindStatusCallback:: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monikers assíncronos](asynchronous-monikers.md)
</dt> </dl>

 

 