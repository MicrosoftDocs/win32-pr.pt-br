---
title: Representação e chamadas assíncronas
description: Representação e chamadas assíncronas
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84f7fcbdc820b50ef4eaaedd81ac579fcce64f1371bc57219348f6dcbedc0f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070876"
---
# <a name="impersonation-and-asynchronous-calls"></a>Representação e chamadas assíncronas

O servidor não pode representar o cliente após a conclusão da chamada do servidor para [**ISynchronize::Signal,**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) mesmo que o método Begin \_ ainda não tenha sido concluído. Por exemplo, suponha que um cliente chame o método Begin, o servidor processe a chamada imediatamente e o servidor chame Signal para indicar \_ que o processamento foi concluído.  Mesmo que o trabalho permaneça a ser feito no método Begin, o servidor não poderá representar o cliente após a conclusão da chamada \_ **para Signal.**

Se o servidor representar o cliente antes de chamar [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), o token de representação não será removido do thread até que o servidor chame [**IServerSecurity::RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) ou até que a chamada do servidor para Begin retorne, o que ocorrer \_ primeiro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Delegação e representação](delegation-and-impersonation.md)
</dt> <dt>

[Fazendo uma chamada assíncrona](making-an-asynchronous-call.md)
</dt> </dl>

 

 