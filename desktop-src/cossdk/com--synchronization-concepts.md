---
description: Em geral, a sincronização não é necessária quando você tem um STA (single-threaded apartment) porque o apartment fornece a sincronização para você.
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: Conceitos de sincronização COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4153c02a5fcd9a0990459e360d239396e7de30cff22316da70f73002e73d6e0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128998"
---
# <a name="com-synchronization-concepts"></a>Conceitos de sincronização COM+

Em geral, a sincronização não é necessária quando você tem um STA (single-threaded apartment) porque o apartment fornece a sincronização para você. A sincronização se torna importante quando você tem um MTA (apartment multithread) e um objeto de thread livre. No passado, objetos de thread livre tinham que lidar com o bloqueio. Você pode eliminar a necessidade de usar o bloqueio definindo o atributo de sincronização para um componente.

A sincronização tem as seguintes propriedades:

-   Permite que um chamador insira o componente por vez.
-   Proíbe o fluxo entre o processo ou o computador.
-   Flui do componente para o componente dentro de um processo.
-   Permite a reentração do mesmo chamador.

Ao contrário dos apartments, as atividades abrangem contextos de vários processos e hosts. A sincronização determina qual atividade conterá um objeto . Os objetos podem residir em qualquer uma das seguintes atividades:

-   Atividade do criador
-   Nova atividade
-   Nenhuma atividade

O COM+ garante a concurreência por uma série de bloqueios para cada atividade. Se um chamador tentar inserir um componente sincronizado COM+ que já está sendo usado por outro chamador, a chamada será bloqueada até que o bloqueio seja liberado. Esse comportamento de bloqueio não passará do tempo e não poderá ser configurado para o tempo de vida. Se o bloqueio não estiver em uso, o bloqueio será adquirido e a chamada será processada. Após a conclusão, o bloqueio é liberado para o próximo chamador. Para evitar deadlock, o COM+ gerencia o acesso a todos os objetos entre atividades por uma série aninhada de chamadas encadeadas em toda a rede.

O COM+ fornece as seguintes configurações de sincronização:

-   Desabilitado
-   Sem suporte
-   Com suporte
-   Obrigatório
-   Requer novo

> [!Note]  
> Algumas configurações de sincronização funcionam em conjunto com outras configurações de componente COM+. Por exemplo, a sincronização será necessária se o serviço de ativação [JIT (Just-In-Time) COM+](com--just-in-time-activation.md) estiver habilitado. O JIT será necessário se você habilitar transações; portanto, o processamento [de transações](com--transactions.md) COM+ também requer sincronização. Portanto, as classes com a configuração de JIT=True também devem ter a configuração de Synchronization=Required ou Synchronization=RequiresNew.

 

Para obter instruções sobre como definir opções de sincronização usando a ferramenta administrativa serviços de componentes, consulte [Configurando o atributo de sincronização](setting-the-synchronization-attribute.md).

Para obter mais informações sobre como usar a Biblioteca de Administração COM+ para definir opções de sincronização, consulte [Automating COM+ Administration](automating-com--administration.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas de sincronização COM+](com--synchronization-tasks.md)
</dt> </dl>

 

 



