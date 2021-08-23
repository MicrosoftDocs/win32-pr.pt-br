---
title: Fazendo uma chamada assíncrona
description: O procedimento para fazer uma chamada síncrona é simples. o cliente obtém um ponteiro de interface no objeto de servidor e chama métodos por meio desse ponteiro. A chamada assíncrona envolve um objeto de chamada, portanto, ele envolve algumas etapas.
ms.assetid: ab65d38d-836a-48d4-87c1-8812cbc8ff92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384a153b826e570920fca2a92f5b53ed2079c561cbcda899b793cef1f39473bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755986"
---
# <a name="making-an-asynchronous-call"></a>Fazendo uma chamada assíncrona

O procedimento para fazer uma chamada síncrona é simples: o cliente obtém um ponteiro de interface no objeto de servidor e chama métodos por meio desse ponteiro. A chamada assíncrona envolve um objeto de chamada, portanto, ele envolve algumas etapas.

Para cada método em uma interface síncrona, a interface assíncrona correspondente implementa dois métodos. Esses métodos anexam os prefixos Begin \_ e Finish \_ ao nome do método síncrono. Por exemplo, se uma interface chamada ISimpleStream tiver um método Read, a interface AsyncISimpleStream terá um método Begin \_ Read e Finish \_ Read. Para iniciar uma chamada assíncrona, o cliente chama o \_ método Begin.

**Para iniciar uma chamada assíncrona**

1.  Consulte o objeto Server para a interface [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) . Se [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) retornar e \_ nointerface, o objeto Server não oferecerá suporte à chamada assíncrona.

2.  Chame [**ICallFactory:: createcall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) para criar um objeto de chamada correspondente à interface que você deseja e, em seguida, solte o ponteiro para [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory).

3.  Se você não solicitou um ponteiro para a interface assíncrona da chamada para [**createcall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall), consulte o objeto de chamada para a interface assíncrona.

4.  Chame o método Begin apropriado \_ .

O objeto de servidor agora está processando a chamada assíncrona e o cliente está livre para realizar outro trabalho até que ele precise dos resultados da chamada.

Um objeto de chamada pode processar apenas uma chamada assíncrona por vez. Se o mesmo ou um segundo cliente chamar um \_ método Begin antes de uma chamada assíncrona pendente ser concluída, o \_ método Begin retornará RPC \_ E \_ chamada \_ pendente.

Se o cliente não precisar dos resultados do \_ método Begin, ele poderá liberar o objeto de chamada no final deste procedimento. COM detecta essa condição e limpa a chamada. O \_ método Finish não é chamado e o cliente não obtém nenhum parâmetro de saída ou um valor de retorno.

Quando o objeto de servidor está pronto para retornar do \_ método Begin, ele sinaliza o objeto de chamada que ele está pronto. Quando o cliente estiver pronto, ele verificará se o objeto de chamada foi sinalizado. Nesse caso, o cliente pode concluir a chamada assíncrona.

O mecanismo para essa sinalização e verificação entre o cliente e o servidor é a interface [**ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) no objeto de chamada. Normalmente, o objeto de chamada implementa essa interface agregando um objeto de sincronização fornecido pelo sistema. O objeto de sincronização encapsula um identificador de evento, que o servidor sinaliza pouco antes de retornar do \_ método Begin chamando [**ISynchronize:: Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal).

**Para concluir uma chamada assíncrona**

1.  Consulte o objeto de chamada para a interface [**ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) .

2.  Chamar [**ISynchronize:: Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait).

3.  Se [**Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) retornar RPC \_ E \_ timeout, o \_ método Begin não terminará o processamento. O cliente pode continuar com outro trabalho e chamar **aguardar** novamente mais tarde. Ele não pode chamar o \_ método Finish até que **Wait** retorne S \_ OK.

    Se [**Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) retornar S \_ OK, o método Begin retornará \_ . Chame o método de conclusão apropriado \_ .

O \_ método Finish passa os parâmetros de saída do cliente. O comportamento dos métodos assíncronos, incluindo o valor de retorno do \_ método Finish, deve corresponder exatamente ao método síncrono correspondente.

O cliente pode liberar o objeto de chamada assim que o \_ método Finish retorna ou pode conter um ponteiro para o objeto de chamada para fazer chamadas adicionais. Em ambos os casos, o cliente é responsável por liberar o objeto de chamada quando o objeto não é mais necessário.

Se você chamar um \_ método Finish quando nenhuma chamada estiver em andamento, o método retornará RPC \_ E \_ chamada \_ concluída.

> [!Note]  
> Se os objetos de cliente e de servidor estiverem no mesmo apartamento, as chamadas para [**ICallFactory:: createcall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) não têm garantia de sucesso. Se o objeto de servidor não oferecer suporte à chamada assíncrona em uma interface específica, a tentativa de criar um objeto de chamada falhará e o cliente deverá usar a interface síncrona.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cancelando uma chamada assíncrona](canceling-an-asynchronous-call.md)
</dt> <dt>

[Client Security durante uma chamada assíncrona](client-security-during-an-asynchronous-call.md)
</dt> <dt>

[Representação e chamadas assíncronas](impersonation-and-asynchronous-calls.md)
</dt> </dl>

 

 