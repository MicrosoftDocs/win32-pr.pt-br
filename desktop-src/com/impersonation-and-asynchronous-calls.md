---
title: Representação e chamadas assíncronas
description: Representação e chamadas assíncronas
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0854946b619f7580173ffcbc97c9af3f2540361b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641944"
---
# <a name="impersonation-and-asynchronous-calls"></a>Representação e chamadas assíncronas

O servidor não pode representar o cliente depois que a chamada do servidor para [**ISynchronize:: Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) for concluída, mesmo que o \_ método Begin ainda não tenha sido concluído. Por exemplo, suponha que um cliente chame o \_ método Begin, o servidor processa a chamada imediatamente e o servidor chama o **sinal** para indicar que ele concluiu o processamento. Mesmo se o trabalho continuar a ser feito no \_ método Begin, o servidor não poderá representar o cliente depois que a chamada para **Signal** for concluída.

Se o servidor representar o cliente antes de chamar [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), o token de representação não será removido do thread até que o servidor chame [**IServerSecurity:: RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) ou até que a chamada do servidor para Begin \_ Returns, o que ocorrer primeiro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Delegação e representação](delegation-and-impersonation.md)
</dt> <dt>

[Fazendo uma chamada assíncrona](making-an-asynchronous-call.md)
</dt> </dl>

 

 