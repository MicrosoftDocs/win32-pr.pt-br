---
description: Geralmente, a sincronização não é necessária quando você tem um STA (single-threaded apartment) porque o apartamento fornece a sincronização para você.
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: Conceitos de sincronização COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaca81050e67c76e3de6ad4845543b9230d2a24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646494"
---
# <a name="com-synchronization-concepts"></a>Conceitos de sincronização COM+

Geralmente, a sincronização não é necessária quando você tem um STA (single-threaded apartment) porque o apartamento fornece a sincronização para você. A sincronização se torna importante quando você tem um MTA (multithreaded apartment) e um objeto de thread livre. No passado, os objetos de thread livre tinham que lidar com o bloqueio. Você pode eliminar a necessidade de usar o bloqueio definindo o atributo de sincronização para um componente.

A sincronização tem as seguintes propriedades:

-   Permite que um chamador insira o componente por vez.
-   Proíbe o fluxo no processo ou no computador.
-   Flui de componente para componente dentro de um processo.
-   Permite a reentrância do mesmo chamador.

Ao contrário de Apartments, as atividades abrangem contextos de vários processos e hosts. A sincronização determina qual atividade conterá um objeto. Os objetos podem residir em qualquer uma das seguintes atividades:

-   Atividade do criador
-   Nova atividade
-   Nenhuma atividade

O COM+ garante a simultaneidade por uma série de bloqueios para cada atividade. Se um chamador tentar inserir um componente sincronizado COM+ que já está sendo usado por outro chamador, a chamada será bloqueada até que o bloqueio seja liberado. Esse comportamento de bloqueio não atingirá o tempo limite e não poderá ser configurado para atingir o tempo limite. Se o bloqueio não estiver em uso, o bloqueio será adquirido e a chamada será processada. Após a conclusão, o bloqueio será liberado para o próximo chamador. Para evitar o deadlock, o COM+ gerencia o acesso a todos os objetos entre as atividades por uma série aninhada de chamadas encadeadas em toda a rede.

O COM+ fornece as seguintes configurações de sincronização:

-   Desabilitado
-   Sem suporte
-   Com suporte
-   Obrigatório
-   Requer novo

> [!Note]  
> Algumas configurações de sincronização funcionam em conjunto com outras configurações de componente COM+. Por exemplo, a sincronização será necessária se o serviço de [ativação JIT (just-in-time) do com+](com--just-in-time-activation.md) estiver habilitado. O JIT é necessário se você habilitar transações; Portanto, o [processamento de transações](com--transactions.md) com+ também requer sincronização. Portanto, as classes com a configuração de JIT = true também devem ter a configuração de Synchronization = Required ou Synchronization = RequiresNew.

 

Para obter instruções sobre como definir as opções de sincronização usando a ferramenta administrativa serviços de componentes, consulte [definindo o atributo de sincronização](setting-the-synchronization-attribute.md).

Para obter mais informações sobre como usar a biblioteca de administração do COM+ para definir opções de sincronização, consulte [automatizando a administração do com+](automating-com--administration.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas de sincronização COM+](com--synchronization-tasks.md)
</dt> </dl>

 

 



