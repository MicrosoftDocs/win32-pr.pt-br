---
title: Cancelando uma chamada assíncrona
description: Um cliente pode cancelar uma chamada assíncrona que está em andamento se o objeto de chamada implementa a interface ICancelMethodCalls.
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d2751400d631c62c19f68f2cab841c0845b432df676abe60befed1f231e103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737110"
---
# <a name="canceling-an-asynchronous-call"></a>Cancelando uma chamada assíncrona

Um cliente pode cancelar uma chamada assíncrona que está em andamento se o objeto de chamada implementa a interface [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) . Para objetos que usam marshaling padrão, **ICancelMethodCalls** está sempre disponível para chamadas com marshaling. Para objetos que usam marshaling personalizado ou para chamadas para objetos de servidor dentro do mesmo apartamento, essa funcionalidade estará disponível somente se o objeto de chamada implementar **ICancelMethodCalls**.

O cliente pode cancelar a chamada a qualquer momento, de quando o \_ método Begin é chamado até que o \_ método Finish retorne. Se o cliente cancelar a chamada antes de chamar o \_ método Finish, ele deverá chamar o \_ método Finish para limpar o estado do objeto de chamada. Até que o cliente tenha feito isso, qualquer chamada para qualquer \_ método Begin no objeto de chamada retornará RPC \_ E \_ Call \_ pendente.

**Para cancelar uma chamada assíncrona**

1.  Consulte o objeto de chamada para [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).

2.  Chame [**ICancelMethodCalls:: Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel)e, em seguida, chame [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar o ponteiro obtido pela chamada [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) na etapa 1.

3.  Se o cliente ainda não tiver chamado o \_ método Finish, chame-o agora.

Não há nenhuma garantia de que o servidor realmente interrompeu a execução da chamada. Se o trabalho adicional do cliente depende de algum estado de servidor que a chamada pode ou não ter mudado, o cliente deve determinar esse estado antes de continuar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fazendo uma chamada assíncrona](making-an-asynchronous-call.md)
</dt> </dl>

 

 