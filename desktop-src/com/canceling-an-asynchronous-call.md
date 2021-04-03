---
title: Cancelando uma chamada assíncrona
description: Um cliente pode cancelar uma chamada assíncrona que está em andamento se o objeto de chamada implementa a interface ICancelMethodCalls.
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775b187f1abd3fca43ba907d92f6eabd926e4608
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084935"
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

 

 