---
description: Há muitos aplicativos que criam threads que gastam muito tempo no estado em espera pela ocorrência de um evento.
ms.assetid: a5e52080-35d4-47f5-9050-90889e3bf2f8
title: Pooling de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c581e416952e6bac14dbf12a8f87202925a5254879b7e220c7cb2d780699f9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081276"
---
# <a name="thread-pooling"></a>Pooling de thread

Há muitos aplicativos que criam threads que gastam muito tempo no estado em espera pela ocorrência de um evento. Outros threads podem entrar em um estado de pertação apenas para serem organizados periodicamente para sondar uma alteração ou atualizar informações de status. *O pooling de* threads permite que você use threads com mais eficiência fornecendo ao seu aplicativo um pool de threads de trabalho gerenciados pelo sistema. Pelo menos um thread monitora o status de todas as operações de espera na fila para o pool de threads. Quando uma operação de espera é concluída, um thread de trabalho do pool de threads executa a função de retorno de chamada correspondente.

Este tópico descreve a API do pool de threads original. A API do pool de threads introduzida no Windows Vista é mais simples, mais confiável, tem melhor desempenho e fornece mais flexibilidade para desenvolvedores. Para obter informações sobre a API do pool de threads atual, consulte [Pools de threads](thread-pools.md).

Você também pode enfilar itens de trabalho que não estão relacionados a uma operação de espera para o pool de threads. Para solicitar que um item de trabalho seja manipulado por um thread no pool de threads, chame a [**função QueueUserWorkItem.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) Essa função leva um parâmetro para a função que será chamada pelo thread selecionado no pool de threads. Não é possível cancelar um item de trabalho depois que ele tiver sido en fila.

[Temporizadores de fila de temporizador](../sync/timer-queues.md) e operações de espera [registradas](../sync/wait-functions.md) também usam o pool de threads. Suas funções de retorno de chamada são en filas para o pool de threads. Você também pode usar a [**função BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback) para postar operações de E/S assíncronas. Após a conclusão da E/S, o retorno de chamada é executado por um thread do pool de threads.

O pool de threads é criado na primeira vez que você chama [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) ou [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback)ou quando um temporizador de fila de temporizador ou operação de espera registrada enfiltra uma função de retorno de chamada. Por padrão, o número de threads que podem ser criados no pool de threads é de cerca de 500. Cada thread usa o tamanho padrão da pilha e é executado na prioridade padrão.

Há dois tipos de threads de trabalho no pool de threads: E/S e não E/S. Um *thread de trabalho de E/S* é um thread que aguarda em um estado de espera alertável. Os itens de trabalho são na fila para threads de trabalho de E/S como chamadas de procedimento assíncrono (APC). Você deve enfilar um item de trabalho em um thread de trabalho de E/S se ele deve ser executado em um thread que aguarda em um estado alertável.

Um thread de trabalho que não é *de E/S* aguarda nas portas de conclusão de E/S. Usar threads de trabalho que não são de E/S é mais eficiente do que usar threads de trabalho de E/S. Portanto, você deve usar threads de trabalho que não são de E/S sempre que possível. Os threads de trabalho de E/S e não de E/S não sairão se houver solicitações de E/S assíncronas pendentes. Ambos os tipos de threads podem ser usados por itens de trabalho que iniciam solicitações de conclusão de E/S assíncronas. No entanto, evite postar solicitações de conclusão de E/S assíncronas em threads de trabalho que não são de E/S se puderem levar muito tempo para ser concluídas.

Para usar o pool de threads, os itens de trabalho e todas as funções que eles chamam devem ser seguros do pool de threads. Uma função segura não pressu que o thread em execução é um thread dedicado ou persistente. Em geral, você deve evitar usar o [armazenamento local](thread-local-storage.md) do thread ou fazer uma chamada assíncrona que requer um thread persistente, como a [**função RegNotifyChangeKeyValue.**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) No entanto, essas funções podem ser chamadas em um thread dedicado (criado pelo aplicativo) ou enfileiradas em um thread de trabalho persistente (usando [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) com a opção WT \_ EXECUTEINPERSISTENTTHREAD).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[E/S alertável](../fileio/alertable-i-o.md)
</dt> <dt>

[Chamadas de procedimento assíncrono](../sync/asynchronous-procedure-calls.md)
</dt> <dt>

[Portas de conclusão de E/S](../fileio/i-o-completion-ports.md)
</dt> <dt>

[Pools de Threads](thread-pools.md)
</dt> </dl>

 

 
