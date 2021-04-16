---
description: Um objeto de seção crítica fornece sincronização semelhante à fornecida por um objeto mutex, exceto que uma seção crítica pode ser usada somente pelos threads de um único processo.
ms.assetid: 2ec11a42-3d12-4d60-9dd7-dc38926d56e1
title: Objetos de seção crítica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbcada1f2ddbc6d370445f36a3dbd51c5c9f54bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751062"
---
# <a name="critical-section-objects"></a>Objetos de seção crítica

Um *objeto de seção crítica* fornece sincronização semelhante à fornecida por um objeto mutex, exceto que uma seção crítica pode ser usada somente pelos threads de um único processo. Os objetos de seção crítica não podem ser compartilhados entre processos.

Objetos de evento, mutex e Semaphore também podem ser usados em um aplicativo de processo único, mas os objetos de seção crítica fornecem um mecanismo um pouco mais rápido e eficiente para sincronização de exclusão mútua (um teste específico do processador e uma instrução SET). Como um objeto mutex, um objeto section crítico pode pertencer a apenas um thread por vez, o que o torna útil para proteger um recurso compartilhado do acesso simultâneo. Ao contrário de um objeto mutex, não há como dizer se uma seção crítica foi abandonada.

A partir do Windows Server 2003 com Service Pack 1 (SP1), os threads que esperam em uma seção crítica não adquirem a seção crítica de acordo com uma primeira e mais servem. Essa alteração aumenta significativamente o desempenho para a maioria dos códigos. No entanto, alguns aplicativos dependem da ordenação PEPS (primeiro a entrar, primeiro a sair) e podem funcionar de forma ruim ou não em versões atuais do Windows (por exemplo, aplicativos que usam seções críticas como um limitador de taxa). Para garantir que o código continue a funcionar corretamente, talvez seja necessário adicionar um nível adicional de sincronização. Por exemplo, suponha que você tenha um thread de produtor e um thread de consumidor que estão usando um objeto de seção crítica para sincronizar seu trabalho. Crie dois objetos de evento, um para cada thread a ser usado para sinalizar que ele está pronto para o outro thread continuar. O thread do consumidor aguardará que o produtor sinalize seu evento antes de entrar na seção crítica, e o thread do produtor aguardará o thread do consumidor para sinalizar seu evento antes de entrar na seção crítica. Depois que cada thread deixa a seção crítica, ele sinaliza seu evento para liberar o outro thread.

**Windows Server 2003 e Windows XP:** Os threads que estão esperando em uma seção crítica são adicionados a uma fila de espera; Eles são ativados e geralmente adquirem a seção crítica na ordem em que foram adicionados à fila. No entanto, se os threads forem adicionados a essa fila a uma taxa rápida o suficiente, o desempenho poderá ser degradado devido ao tempo necessário para despertar cada thread em espera.

O processo é responsável por alocar a memória usada por uma seção crítica. Normalmente, isso é feito simplesmente declarando uma variável do **tipo \_ seção crítica**. Antes que os threads do processo possam usá-lo, inicialize a seção crítica usando a função [**InitializeCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsection) ou [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) .

Um thread usa a função [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) ou [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) para solicitar a propriedade de uma seção crítica. Ele usa a função [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) para liberar a propriedade de uma seção crítica. Se o objeto de seção crítica estiver pertencente a outro thread, o **EnterCriticalSection** aguardará indefinidamente a propriedade. Por outro lado, quando um objeto mutex é usado para exclusão mútua, as [funções Wait](wait-functions.md) aceitam um intervalo de tempo limite especificado. A função **TryEnterCriticalSection** tenta inserir uma seção crítica sem bloquear o thread de chamada.

Quando um thread possui uma seção crítica, ele pode fazer chamadas adicionais para [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) ou [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) sem bloquear sua execução. Isso impede que um thread seja bloqueado enquanto aguarda uma seção crítica que ele já possui. Para liberar sua propriedade, o thread deve chamar [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) uma vez para cada vez que ele inseriu a seção crítica. Não há nenhuma garantia sobre a ordem na qual os threads em espera adquirirão a propriedade da seção crítica.

Um thread usa a função [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) ou [**SetCriticalSectionSpinCount**](/windows/win32/api/synchapi/nf-synchapi-setcriticalsectionspincount) para especificar uma contagem de rotação para o objeto de seção crítica. A rotação significa que, quando um thread tenta adquirir uma seção crítica bloqueada, o thread entra em um loop, verifica se o bloqueio foi liberado e, se o bloqueio não for liberado, o thread vai para o modo de suspensão. Em sistemas de processador único, a contagem de rotação é ignorada e a contagem de rotação de seção crítica é definida como 0 (zero). Em sistemas multiprocessadores, se a seção crítica não estiver disponível, o thread de chamada girará *dwSpinCount* vezes antes de executar uma operação de espera em um semáforo associado à seção crítica. Se a seção crítica for liberada durante a operação de rotação, o thread de chamada evitará a operação de espera.

Qualquer thread do processo pode usar a função [**DeleteCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-deletecriticalsection) para liberar os recursos do sistema que são alocados quando o objeto da seção crítica é inicializado. Depois que essa função é chamada, o objeto de seção crítica não pode ser usado para sincronização.

Quando um objeto de seção crítica é de propriedade, os únicos outros threads afetados são os threads que estão aguardando a propriedade em uma chamada para [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection). Os threads que não estão aguardando são livres para continuar em execução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos mutex](mutex-objects.md)
</dt> <dt>

[Usando objetos de seção crítica](using-critical-section-objects.md)
</dt> </dl>

 

 
