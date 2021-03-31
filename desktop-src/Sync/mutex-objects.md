---
description: Um objeto mutex é um objeto de sincronização cujo estado é definido como sinalizado quando ele não pertence a nenhum thread e não é sinalizado quando ele é proprietário.
ms.assetid: eca0795a-1fd0-4034-9d61-9416670919cf
title: Objetos mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e84c17ba3e99e888f7d1e9137a7f24a4d78ce2d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829138"
---
# <a name="mutex-objects"></a>Objetos mutex

Um *objeto mutex* é um objeto de sincronização cujo estado é definido como sinalizado quando ele não pertence a nenhum thread e não é sinalizado quando ele é proprietário. Somente um thread por vez pode ter um objeto mutex, cujo nome vem do fato de ser útil para coordenar o acesso mutuamente exclusivo a um recurso compartilhado. Por exemplo, para impedir que dois threads gravem na memória compartilhada ao mesmo tempo, cada thread aguarda a propriedade de um objeto mutex antes de executar o código que acessa a memória. Depois de gravar na memória compartilhada, o thread libera o objeto mutex.

Um thread usa a função [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) ou [**CreateMutexEx**](/windows/win32/api/synchapi/nf-synchapi-createmutexexa) para criar um objeto mutex. O thread de criação pode solicitar a propriedade imediata do objeto mutex e também pode especificar um nome para o objeto mutex. Ele também pode criar um mutex sem nome. Para obter informações adicionais sobre nomes de mutex, evento, semáforo e objetos de temporizador, consulte [sincronização entre processos](interprocess-synchronization.md).

Threads em outros processos podem abrir um identificador para um objeto de mutex nomeado existente especificando seu nome em uma chamada para a função [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) . Para passar um identificador para um mutex sem nome para outro processo, use a função [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) ou a herança de identificador pai-filho.

Qualquer thread com um identificador para um objeto mutex pode usar uma das [funções Wait](wait-functions.md) para solicitar a propriedade do objeto mutex. Se o objeto mutex pertencer a outro thread, a função Wait bloqueará o thread solicitante até que o thread proprietário libere o objeto mutex usando a função [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) . O valor de retorno da função Wait indica se a função retornou por algum motivo que não seja o estado do mutex que está sendo definido para sinalizado.

Se mais de um thread estiver aguardando um mutex, um thread em espera será selecionado. Não assuma uma ordem FIFO (primeiro a entrar, primeiro a sair). Eventos externos, como APCs de modo kernel, podem alterar a ordem de espera.

Depois que um thread obtém a propriedade de um mutex, ele pode especificar o mesmo mutex em chamadas repetidas para as [funções de espera](wait-functions.md) sem bloquear sua execução. Isso impede que um thread seja bloqueado enquanto aguarda um mutex que ele já possui. Para liberar sua propriedade em tais circunstâncias, o thread deve chamar [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) uma vez para cada vez que o mutex satisfez as condições de uma função de espera.

Se um thread for encerrado sem liberar sua propriedade de um objeto mutex, o objeto mutex será considerado abandonado. Um thread em espera pode adquirir a propriedade de um objeto mutex abandonado, mas a função Wait retornará **Wait \_ abandonado** para indicar que o objeto mutex é abandonado. Um objeto mutex abandonado indica que ocorreu um erro e que qualquer recurso compartilhado protegido pelo objeto mutex está em um estado indefinido. Se o thread continuar como se o objeto mutex não tivesse sido abandonado, ele não será mais considerado abandonado depois que o thread liberar sua propriedade. Isso restaura o comportamento normal se um identificador para o objeto mutex for especificado em seguida em uma função Wait.

Observe que os [objetos de seção crítica](critical-section-objects.md) fornecem sincronização semelhante à fornecida por objetos mutex, exceto que os objetos de seção críticos podem ser usados somente pelos threads de um único processo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando objetos mutex](using-mutex-objects.md)
</dt> </dl>

 

 
