---
title: Monikers de ponteiro
description: Um moniker de ponteiro identifica um objeto que pode existir somente no estado ativo ou em execução. Isso difere de outras classes de monikers, que identificam objetos que podem existir no estado passivo ou ativo.
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcdf96497751b3f777c292c56d35b2c04432da84b352e20c4dd8b0917dedb16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047894"
---
# <a name="pointer-monikers"></a>Monikers de ponteiro

Um *moniker de ponteiro* identifica um objeto que pode existir somente no estado ativo ou em execução. Isso difere de outras classes de monikers, que identificam objetos que podem existir no estado passivo ou ativo.

Suponha, por exemplo, que um aplicativo tenha um objeto que não tenha nenhuma representação persistente. Normalmente, se um cliente do seu aplicativo precisar de acesso a esse objeto, você poderá simplesmente passar o cliente um ponteiro para o objeto. No entanto, suponha que o cliente esteja esperando um moniker. Não é possível identificar o objeto com um moniker de arquivo, pois ele não está armazenado em um arquivo nem com um moniker de item, pois ele não está contido em outro objeto.

Em vez disso, seu aplicativo pode criar um moniker de ponteiro, que é um moniker que simplesmente contém um ponteiro internamente, e passá-lo para o cliente. O cliente pode tratar esse moniker como qualquer outro. No entanto, quando o cliente chama [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) no moniker do ponteiro, o código do moniker não verifica a tabela de objetos em execução (corrompidos) ou carrega qualquer coisa do armazenamento. Em vez disso, o código do moniker simplesmente chama [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro armazenado dentro do moniker.

Os monikers de ponteiro permitem que os objetos existentes somente no estado ativo ou em execução participem de operações de moniker e sejam usados por clientes de moniker. Uma diferença importante entre os monikers do ponteiro e outras classes de moniker é que os monikers do ponteiro não podem ser salvos no armazenamento persistente. Se você fizer isso, chamar o método [**IMoniker:: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) retornará um erro. Isso significa que os monikers de ponteiro são úteis apenas em situações especializadas. Você pode usar a função [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) se precisar usar um moniker de ponteiro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Anti-moniker](anti-monikers.md)
</dt> <dt>

[Monikers de classe](class-monikers.md)
</dt> <dt>

[Monikers compostos](composite-monikers.md)
</dt> <dt>

[Monikers de arquivo](file-monikers.md)
</dt> <dt>

[Monikers de item](item-monikers.md)
</dt> </dl>

 

 




